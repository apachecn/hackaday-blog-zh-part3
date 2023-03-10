# 将深度学习算法引入您的安全摄像头

> 原文：<https://hackaday.com/2018/03/21/bring-deep-learning-algorithms-to-your-security-cameras/>

人工智能正在迅速革新安全摄像机行业。几家制造商出售使用深度学习来检测汽车、人和其他事件的相机。与“笨”相机相比，这些智能相机通常很贵。[【Martin】能够将这些检测功能带到一个带有树莓派的标准相机上，还有点独创性](https://harizanov.com/2018/03/enhancing-my-ordinary-security-cameras-with-ai/)。

[马丁]的目标是捕捉感兴趣的事件，比如屏幕上的人，或者车道上的车。然后，事件的数据将被发布到一个 [MQTT](https://hackaday.com/2016/06/02/minimal-mqtt-power-and-privacy/) 主题，同时发布的还有一些元数据，比如置信度。OpenCV 通常是这些管道的开始，但[马丁的]相机不会像 OpenCV 要求的那样通过 TCP 发送 RTSP 图像，只能通过 UDP 发送 RTSP。为了解决这个问题，Martin 使用 FFmpeg 捕获视频流。深度学习 AI 魔法由[暗流库](https://github.com/thtrieu/darkflow)处理，该库本身基于谷歌的 Tensorflow。

马丁用一些便宜的中国 PTZ 相机测试了他的识别系统，并在远程树莓 Pi 上运行处理。到目前为止，结果还不错。该系统能够识别在车道上行驶的人、动物和汽车。如果你想亲自尝试一下，可以在 GitHub 上找到他的代码。