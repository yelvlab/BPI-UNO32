·# BPI:uno32开发板

板子外形设计完全兼容Arduino

本目录下是BPI：uno32板子基础功能测试代码工程。编译环境采用`PlatformIO for Atom/VSCode `

#### 使用方法：

在`Atom/VSCode`终端内执行`platformio run --target upload`编译并上传，或者点击软件框内的快捷操作按钮。（需要提前预装`Atom/VSCode`软件，安装`PlatformIO`扩展，并且在`PlatformIO`里面下载`ESP32`平台）本段代码可以用于`Arduino`编译，但需要自行安装平台支持与库扩展等等。

#### 主要测试功能介绍：

- RGB三色LED循环渐变控制测试

- 6条ADC_channel1的AD采集测试

- WiFi扫描测试

- 蜂鸣器渐变控制测试
