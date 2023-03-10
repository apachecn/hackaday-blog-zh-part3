# 我的家是技术之家

> 原文：<https://hackaday.com/2017/09/07/me-casa-es-techno-casa/>

“贾维斯，给我做个三明治”还不是现实。虽然现在有很多家庭自动化产品，但是商业解决方案并不适合那些自尊的极客。所以[马蒂亚斯]带着他的 [La CasaC 家庭自动化项目](https://cat101.bitbucket.io/en/#!index.md)走了 DIY 路线，实现了他所追求的功能。

【Matias’】项目是我们近年来看到的最精细、最大规模的 DIY 家庭自动化项目之一。这个项目有 200 多个节点，计划和执行了好几年。设计的核心是一直流行的运行 OpenHAB 的 Raspberry Pi，以减轻定制和与各种协议集成的痛苦。为了进一步简化庞大的任务，设计使用 RS485 在主设备和从设备之间进行通信。

每个墙节点由附近的 Arduino 管理，Arduino 反过来与中央 Arduino Mega 对话。OpenHab 负责更高级的功能，如 UI、与现有硬件的集成，如太阳能加热器、媒体中心控制、RFID 和键盘控制。传感器数据聚合和构建管理集中完成，数据汇集到单独的 NAS 系统作为长期存储。

让这个项目令人敬畏的是，[马蒂亚斯]没有在他的房子里集成一个树莓派，没有！他实际上围绕这个系统整合了他的整个房子，因为这个构建也包括了房子的建造。看一看[这个谷歌照片库](https://photos.google.com/share/AF1QipMVpyD9IpdOijPzEqzFrY6pBF0_ATepbgJTrt7zaXbkGsIlps9JllDcPN1VOfUX4A?key=ZFFiTk5zMDBzeTlHczVLMnoyZTMxSVl2LTdRdEln)来看看建造的照片进度。太神奇了。

代码和片段可以在 GitHub 上找到，供你浏览，尽管这看起来很简单。如果这启发了你，那么如果你想在完全投入之前尝试一下，也可以看看姜饼屋的[树莓派家庭自动化](https://hackaday.com/2017/01/13/raspberry-pi-home-automation-for-the-holidays/)。