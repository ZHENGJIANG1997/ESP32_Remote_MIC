# ESP32_Remote_MIC
ESP32 as Remote MIC
本项目是参考 https://github.com/paranerd/simplecam 项目的ESP32版本移植，原项目的技术点是可以用网页直接访问终端监听图像和声音.目前只移植了部分声音相关的功能. 视频功能ESP32-CAM自身有带例子，如果视频声音一起传输性能不够，就没有一块移植上.

功能：<br/>
利用本程序，可以使esp32成为远程麦克风,树莓派运行Python连接此麦克风可监听到esp32的实时录音

硬件:<br/>
1.ESP32+ INMP441(I2S麦克风模块)<br/>
/* ESP32+INMP441(I2S麦克风模块) 接线定义见I2S.h <br/>
SCK IO14<br/>
WS  IO27<br/>
SD  IO2<br/>
L/R GND<br/>
*/<br/>
2.树莓派<br/>

使用场景：<br/>
单元楼大门声音对话，监听防盗等

使用方法：<br/>
1.esp32_remote_mic 用arduino工具烧录到esp32<br/>
  esp32_remote_mic2 这个版本开发失败，原开发目标是支持浏览器直接监听麦克风， 说明对项目simplecam的技术原理理解不够深入，目前听不到声音，原因不明。<br/>
2.rasberry 下两个py文件分别是监听声音文件直接输出到扬声器，输出到wav文件两个版本。<br/>
两个程序都需要连接路由器，注意修改路由器连接密码以及IP地址

