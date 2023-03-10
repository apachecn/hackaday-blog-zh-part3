# 嵌入 Elliot:用循环缓冲区循环

> 原文：<https://hackaday.com/2015/10/29/embed-with-elliot-going-round-with-circular-buffers/>

为什么缓冲？因为缓冲器让你放松了一些。

不可避免地，在我们最近关于微控制器中断的[系列中，出现了如何处理实际串行数据的问题。在这些例子中，我们在中断服务程序(ISR)和代码主体之间一次传递一个字节。只要主例程能够及时处理传入的数据，这就很好，但是，正如许多人在评论中指出的，如果主例程花费的时间太长，单个字节可能会被新的字节覆盖。](http://hackaday.com/?s=embed+with+elliot%3A+interrupts)

解决办法？为多个字节腾出一些存储空间，以便它们可以堆积起来，直到您有时间处理它们。如果你把这个存储空间和一些简单的读写规则结合起来，你就有了一个[缓冲区](https://en.wikipedia.org/wiki/Data_buffer)。

所以请继续阅读，看看如何用 C 语言为微控制器(或者任何东西)实现一个简单、直接的*循环缓冲区*。缓冲区是您编程工具包中的一个非常方便的工具，如果您还不熟悉它们，那么您应该熟悉它们。

## 缓冲

一般来说，当两个进程异步地或者以不同的瞬时速率生成或处理数据时，您会希望在它们之间有一个缓冲区。如果数据以单个字节(如字母)的形式缓慢进入，但以更大的块(如单词)处理数据更方便，那么缓冲区正是您所需要的。相反，您可能希望一次将主例程中的一个字符串排队，并让串行发送例程将它拆分成字节，并在可能的时候将它们来回传送。

简而言之，缓冲区位于两个异步例程之间，确保它们中的任何一个都可以在需要时动作，而不会迫使另一个例程等待它。如果一个进程是缓慢而稳定的乌龟，而另一个进程是突发的兔子，需要频繁地休息来喘口气，那么缓冲区就是数据在此期间堆积的地方。

我们感兴趣的缓冲区系列是确保数据以相同的顺序进出的缓冲区。也就是说，我们将会看到先进先出(FIFO)缓冲器。对于一个简单的 FIFO，你可以将输入的数据存储在一个数组的最后一个空闲位置，并从该数组的开始读取数据，直到用完所有数据。

[![lin_buffer_anim](img/817076cabe0b3dea40625ecaf9cb5b28.png)](https://hackaday.com/wp-content/uploads/2015/10/lin_buffer_anim1.gif)

请注意这个最简单的缓冲区的伟大之处；一个进程可以从阵列前端读取数据，而另一个进程可以在阵列后端添加数据。它们不会相互覆盖，并且都可以轮流或成组地访问阵列。但是最终你会在数组的末尾用完空间，因为缓冲区只在第一个数组元素被完全读取后才把它的写入位置重置回第一个数组元素。

这种线性缓冲区非常适合您可能一次读取所有内容的情况，但是当读取和写入像这里所示的那样交错时，您可能会在它被清除之前用完数组中的空间，而与此同时，在数组的前面有已经被读取的“空”空间。

解决方案是一个[循环缓冲区](https://en.wikipedia.org/wiki/Circular_queue)，其中的数据可以再次绕回起点以用完额外的空间。循环缓冲区非常好，因为它们比线性缓冲区利用更多的分配内存，并且仍然保持 FIFO 的顺序。

[![buffer_anim](img/9405a96239676f68c93e40993be6e64f.png)](https://hackaday.com/wp-content/uploads/2015/10/buffer_anim.gif)

要创建一个循环缓冲区，我们需要跟踪缓冲区的开始(红色)和结束(绿色)，并制定一些简单的规则来处理环绕并防止我们覆盖现有的数据，但这就是它的要点。

### 循环缓冲器:空的还是满的？

有了线性缓冲区，很容易判断缓冲区是空的还是满的。如果最后一个可用的槽是数组中的最后一个字节，则它已满。如果是数组中的第一个槽，则为空。但是对于循环缓冲区来说，事情要稍微复杂一些，因为循环常常会使我们处于这样一种情况，即最新的数据被写入一个在数值上低于最老的数据的槽中。

因此，我们将创建两个额外的变量(索引)来跟踪最新和最老的数据元素在数组中的位置。当两个索引相同时，我们就说缓冲区是空的。每次我们向缓冲区添加数据时，我们将更新“最新的”数据索引，每次我们取出数据时，我们将更新“最老的”。

如果当两个索引相同时，缓冲区为空，那么它什么时候是满的？这变得很棘手，因为当数组完全填满时——每个槽都被填满——最旧的索引和最新的索引彼此相等，这正是我们想要用来测试它是否为空的条件。在我看来，处理这个问题最简单的方法就是始终留出一个空位。

再次观看动画，注意我们声明数组“已满”，而实际上在最新的(绿色)索引到达最老的(红色)索引之前，数组中还有一个空闲空间。也就是说，当最新的索引*加 1*等于最老的索引时，我们声明缓冲区已满，这使得它们永远不会重叠，除非缓冲区为空。我们失去了对缓冲区数组中一个槽的使用，但这使得满和空状态很容易区分。

有很多其他的方法来实现循环缓冲区。总之，除非你有非常紧迫的优化约束，否则任何一个都可以。我们将坚持使用“最新的索引/最老的索引”,因为我发现它是最直观的，但是你可以自己尝试所有的索引。让我们看看它的实际效果。

## 密码

下面是我们需要代码做的事情:

1.  留出一些内存(我们将使用数组)作为缓冲区
2.  跟踪缓冲区中数据的开始(最早的条目)和结束(最新的条目)
3.  提供从缓冲区存储和检索数据的功能:
    1.  最简单的方法使用字节访问
    2.  需要在读或写时更新缓冲区索引
    3.  如果试图写/读，在满/空时传递错误代码很好

我们走吧！首先，我们将设置数据。

```

#define BUFFER_SIZE  16
struct Buffer {
    uint8_t data[BUFFER_SIZE];
    uint8_t newest_index;
    uint8_t oldest_index;
};

```

如果对你来说是新的，不要烦恼。它们只是让我们能够将三个重要的数据位保存在一个容器中，并给这个容器起了个名字，“缓冲区”。在内部，我们有一个数组来存储数据，还有两个变量分别用于第一个和最后一个活动条目。除了将所有数据保存在一个漂亮、紧凑的包中的强迫性快乐之外，当我们稍后对代码进行一般化时，我们会看到这是值得的。

### 写作

现在让我们将一些数据写入缓冲区。为此，我们首先检查是否有空间容纳新条目:也就是说，我们确保`newest_index+1`不会碰到`oldest_index`。如果是这样，我们将返回一个缓冲区满的错误。否则，我们只是将数据存储在下一个槽中，并更新`newest_index`值。

```

enum BufferStatus bufferWrite(uint8_t byte){
    uint8_t next_index = (buffer.newest_index+1) % BUFFER_SIZE;

    if (next_index == buffer.oldest_index){
        return BUFFER_FULL;
    }
    buffer.data[buffer.newest_index] = byte;
    buffer.newest_index = next_index;
    return BUFFER_OK;
}

```

这里您将看到引用`struct`中元素的两种方法中的第一种，即`.`(“成员”)操作符。如果我们想引用我们的缓冲区`struct`中的`data`数组，我们只需写`buffer.data`等。

注意，当我们计算`next_index`时，我们用`BUFFER_SIZE`取模。这为我们做了“包装”。如果我们有一个 16 字节的缓冲区，我们在位置 15，加 1 得到 16，取模返回 0，我们回到开始。正如我们上面提到的，只要我们使用 2 的幂的缓冲长度，这个模实际上计算得非常快——甚至比一个`if`语句还要快。

好了，还有一个(风格上的)细节我已经扫到了地毯下面。我喜欢将来自缓冲区的返回代码作为一个`enum`来处理，这允许我们为返回条件指定可读的名称。使用一个`enum`最终不会改变编译后的代码，但是它使得遵循程序逻辑更加容易。

```

enum BufferStatus {BUFFER_OK, BUFFER_EMPTY, BUFFER_FULL};

```

在内部，编译器用 0 代替`BUFFER_OK`，用 1 代替`BUFFER_EMPTY`，用 2 代替`BUFFER_FULL`，但是我们的代码可以使用更长的文本名称。这使我们在返回 2 时，不会疯狂地试图记住我们指的是哪个返回码。

现在注意我们的`bufferWrite`函数的返回类型是什么:a `BufferStatus enum`。这提醒我们，无论何时调用该函数，我们都应该期待相同的`enum`——从基础数字到它们的文本符号的相同映射。不幸的是，GCC 不为我们检查枚举值的类型，所以你有义务做正确的事情。(其他编译器会抛出警告。)

### 阅读

`bufferRead`的功能也一样简单。首先，我们检查`newest_index`是否与`oldest_index`相同，这表示我们在缓冲区中没有任何数据。如果我们有数据，我们

```

enum BufferStatus bufferRead(uint8_t *byte){
    if (buffer.newest_index == buffer.oldest_index){
        return BUFFER_EMPTY;
    }
    *byte = buffer.data[buffer.oldest_index];
    buffer.oldest_index = (buffer.oldest_index+1) % BUFFER_SIZE;
    return BUFFER_OK;
}

```

这就引出了一个重要的 C 编程习语。我们希望从我们的`bufferRead`函数中获得两件东西:缓冲区中最老的字节和伴随它的返回代码。由于时间的原因，可能与史前 PDP-8 的高效编程有关，C 函数实际上只能返回一个值。如果你的函数想要返回多个值(就像我们在这里做的)，你必须变得狡猾。

我们还没有真正深入研究 Elliot 嵌入中的指针，但这里有另一个标准用例。(首先，请看我们在[基于指针的状态机](http://hackaday.com/2015/09/04/embed-with-elliot-practical-state-machines/)上的帖子)`bufferRead`函数返回一个状态码。那么它将从缓冲区中读取的数据存储在哪里呢？无论我们让它去哪里！

一个[指针](https://en.wikipedia.org/wiki/Pointer_(computer_programming))可以被认为是一个附加了类型的内存地址。当我们将指针`uint8_t *byte`传递给我们的函数时，我们传递的是我们希望函数存储新数据的内存地址。我们的主程序声明了一个变量，然后当我们调用`bufferRead`函数时，我们将该变量的地址传递给它，然后该函数将新数据存储到与`main`中的变量对应的内存地址中。

```

enum BufferStatus status;
uint8_t byte_from_buffer;
status = bufferRead(&amp;byte_from_buffer);
/* and now byte_from_buffer is modified */

```

这里唯一潜在的新东西是“address-of”操作符，`&`。例如，我们用主例程调用`byte_from_buffer`的内存位置调用`bufferRead`，函数将新字节写入内存位置。回到调用函数中，我们得到两个变量:显式传递的`status`值，以及从`bufferRead`函数内部直接写入内存的`byte_from_buffer`。

仅此而已。概括一下:我们使用一个`struct`将数组和它的两个索引组合成一个“变量”，主要是为了方便。然后我们定义了一个`enum`来处理来自 reader 和 writer 函数的三种可能的返回条件，并使返回值可读。最后，我们编写了一些简单的读取器和写入器函数，每次一个字节地从缓冲区存储或读取数据，并根据需要更新相关的索引变量。

## 提炼和概括

现在，我们将缓冲区存储为一个全局变量，这样我们的主例程和读写例程就可以访问它。因此，我们不能一次在多个缓冲区上重用我们的代码，这是很愚蠢的。例如，如果我们使用缓冲器进行 USART 串行通信，我们可能需要一个发送和接收缓冲器。一旦您习惯了缓冲区，您就会希望在任何异步代码段之间使用它们。所以我们需要对我们的函数进行一点一般化，这样我们就可以定义多个缓冲区来处理我们的 reader 和 writer 函数..

还好，很容易。两个简单的改变将允许我们在任意数量的不同缓冲区上重用我们的`bufferRead`和`bufferWrite`函数。

```

enum BufferStatus bufferWrite(volatile struct Buffer *buffer, uint8_t byte){
    uint8_t next_index = (((buffer-&gt;newest_index)+1) % BUFFER_SIZE);

    if (next_index == buffer-&gt;oldest_index){
        return BUFFER_FULL;
    }

    buffer-&gt;data[buffer-&gt;newest_index] = byte;
    buffer-&gt;newest_index = next_index;
        return BUFFER_OK;
}

enum BufferStatus bufferRead(volatile struct Buffer *buffer, uint8_t *byte){

    if (buffer-&gt;newest_index == buffer-&gt;oldest_index){
        return BUFFER_EMPTY;
    }

    *byte = buffer-&gt;data[buffer-&gt;oldest_index];
    buffer-&gt;oldest_index = ((buffer-&gt;oldest_index+1) % BUFFER_SIZE);
        return BUFFER_OK;
}

```

在这两个例子中，我们没有依赖全局名称空间中定义的`buffer`变量，而是将它作为参数传递给函数。或者，更准确地说，我们将一个指向`Buffer`结构的指针传递给函数。我们声明缓冲区`volatile`,因为我们希望稍后使用中断例程更新缓冲区。(如果你需要复习，请参见[我们关于易变性](http://hackaday.com/2015/08/18/embed-with-elliot-the-volatile-keyword/)的文章。)

另一个变化是我们如何引用缓冲区`struct`的元素。问题是我们不传递`struct`本身，而是传递一个指向那个`struct`的指针。所以我们需要的是首先获取(“解引用”)那个`struct`，然后访问其中的`data`元素。繁琐的方法是这样的:`(*buffer).data`，但是由于这种模式在 C 中经常出现，所以开发了一种快捷的符号:`buffer->data`。

### 接受

除了这两个变化，读写代码的逻辑是完全相同的。那么我们如何使用这些函数呢？很高兴你问了。让我们以设置 AVR 微控制器的接收和发送缓冲器为例，使用其内置硬件 USART 和[中断例程](http://hackaday.com/?s=embed+with+elliot+interrupts)将数据传入传出。一旦手头有了一个好的循环缓冲区，处理传入的串行数据就变得轻而易举了。

```

volatile struct Buffer rx_buffer = {{}, 0, 0};

ISR(USART_RX_vect){
    bufferWrite(&amp;rx_buffer, UDR0);
}

int main(void){
    uint8_t received_byte;  
    enum BufferStatus status;

    initUSART();
    initUSART_interrupts();

    while (1) {
        status = bufferRead(&amp;rx_buffer, &amp;received_byte);
        if (status == BUFFER_OK) {      /* we have data */
            do_something(received_byte);
        } 
    }
}

```

这不是一个完整的例子，但它触及了主要元素。该代码定义了一个中断服务例程(ISR ),当有任何东西通过串行线路进入时，它只是将接收到的字节存储到循环缓冲区中。请注意，`bufferWrite`函数非常短，所以我们不会在 ISR 上花太多时间，这正是我们想要的。中断和芯片的硬件串行外设的结合负责为我们填满缓冲区。在`main()`中剩下要做的就是尝试从缓冲区中读取一些数据，并检查返回代码，看看我们是否得到了新的东西。

因为缓冲区是在`main()`例程和 ISR 之间共享的，所以需要在全局名称空间中，在两个函数之外定义它。注意，由于我们从缓冲区的一端写入，从另一端读取，这里不太需要担心[竞争条件和原子性](http://hackaday.com/2015/10/02/embed-with-elliot-interrupts-the-ugly/)。只要 ISR 是唯一写入我们的缓冲区的例程，并且我们只从`main()`中的缓冲区读取，就没有冲突的可能。

也就是说，如果你想加倍确保你的共享 volatile 变量不会同时被访问两次，或者如果你正在编写一个更通用的循环缓冲例程，那么把访问共享变量的部分放在一个`ATOMIC_BLOCK`宏中也无妨。

### 发射

最后，在 AVR 平台上设置发送缓冲器稍微复杂一点，因为当发送缓冲器有数据或为空时，我们需要分别使能和禁用 USART 的数据就绪中断。定义几个方便的函数，并在中断例程中检查缓冲状态，就可以很容易地做到这一点:

```

static inline void enable_transmission(void){
    UCSR0B |= (1&lt;&lt;UDRIE0);
}

static inline void disable_transmission(void){
    UCSR0B &amp;= ~(1&lt;&lt;UDRIE0);
}

ISR(USART_UDRE_vect){	 	 
    uint8_t tempy;	 	 
    enum BufferStatus status_tx;	 	 
    status_tx = bufferRead(&amp;tx_buffer, &amp;tempy);	 	 
    if (status_tx == BUFFER_EMPTY){	 	 
        disable_transmission();	 	 
    } else {	 	 
        UDR0 = tempy; /* write it out to the hardware serial */	 	 
    }	 	 
}	 	 

```

每当 USART 数据寄存器为空(“DRE”)时，就会触发`UDRE`中断，这样 ISR 就可以尽快从发送缓冲区中取出一个新字符。您的调用代码只需将所有数据打包到发送缓冲区并启用中断一次，而无需等待实际的发送发生，相对于快速的 CPU 速度而言，这需要很长时间。这并非巧合，很像 Arduino 的“串行”库函数为你做的。

## 窥视缓冲区内部

最后，有一个非常常见的用例，我们还没有解决。通常情况下，您希望您的代码用多个字节组装数据。也许每个字节都是一个字母，您希望您的代码处理单词。在读取方面，您希望在缓冲区中堆积数据，直到一个空格字符到达。为此，使用一个函数查看最近添加的字符，但不改变任何一个索引变量是非常方便的。

我们将调用这个函数`bufferPeek()`,它的工作方式如下:

```

enum BufferStatus bufferPeek(volatile struct Buffer *buffer, uint8_t *byte){

    uint8_t last_index = ((BUFFER_SIZE + (buffer-&gt;newest_index) - 1) % BUFFER_SIZE);
    if (buffer-&gt;newest_index == buffer-&gt;oldest_index){
        return BUFFER_EMPTY;
    }
    *byte = buffer-&gt;data[last_index];
    return BUFFER_OK;
}

```

到目前为止，除了定义`last_index`的一个技巧之外，代码应该基本上是不言自明的。当缓冲器刚刚回绕时，`newest_index`可以等于零。在这种情况下，从中减去 1(返回到最后一个写入的字符)将得到一个负数。将另一个完整的`BUFFER_SIZE`添加到索引中可以防止该值变为负值，并且`BUFFER_SIZE`的额外因子无论如何都会被取模运算去掉。

一旦我们有了这个“窥视”功能，将字符组合成单词就是小菜一碟。例如，这段代码将等待传入数据缓冲区中的一个空间，然后尽快将该字排入输出缓冲区，完成后打开发送中断。

```

// Check if the last character typed was a space
status = bufferPeek(&amp;rx_buffer, &amp;input_byte);
if (status == BUFFER_OK &amp;&amp; input_byte == ' '){
    while(1) {  
        status = bufferRead(&amp;rx_buffer, &amp;input_byte);
        if (status == BUFFER_OK){
            bufferWrite(&amp;tx_buffer, input_byte);
        } else {
            break;
        }
    } 
    enable_transmission();
}

```

## 代码和结论

所有这些演示代码(以及更多！)可以在 GitHub 库中找到，供您阅读和调整。它可以在任何 AVR 平台上运行，但是唯一特别的是处理中断的机制和我的串行输入/输出库。循环缓冲区代码的核心应该可以在任何你可以用 C 编译的东西上工作。

有各种各样的方法来改善这里提出的缓冲区。循环缓冲器也有许多可能的实现方式。这篇文章太长了，很可能会比它长三倍！

但是不要太纠结于细节。循环缓冲区是处理异步数据创建和消费这一常见问题的通用工具，可以真正帮助分离复杂程序的不同部分。实现缓冲区也不是魔术，我希望这篇文章已经吊起了你的胃口。出去多看看几个实现，找到一个你喜欢的，然后把这些文件藏起来以备不时之需。你会很高兴你做了。

如果你有最喜欢的缓冲代码，或者来自战壕的恐怖故事，请随意在评论中发表。我们很想听听。