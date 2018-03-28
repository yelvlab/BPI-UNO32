# BPI:UNO32

本目录下是BPI：uno32板子基础功能测试代码工程。编译环境采用`PlatformIO for Atom/VSCode `

#### 使用方法：
- 编译：
终端内执行`platformio run`

- 烧录:
终端内执行`platformio run --target upload`

（需要提前预装`Atom/VSCode`软件，安装`PlatformIO`扩展，并且在`PlatformIO`里面下载`ESP32`平台）本段代码可以用于`Arduino`编译，但需要安装平台支持与库扩展等等。[安装教程](/programing/Arduino_IDE)

#### 主要测试功能介绍：

- RGB三色LED循环渐变控制测试

- 6条ADC_channel的AD采集测试

- WiFi扫描测试

- 蜂鸣器渐变控制测试

This directory is under the BPI: uno32 board basic functional test code project. Compiler environment using `PlatformIO for Atom/VSCode`

#### How to use：

- Complie：
Terminal input`platformio run`

- Programing:
Terminal input`platformio run --target upload`

(You need to pre-install the `Atom/VSCode` software, install the `PlatformIO` extension, and download the `ESP32` platform in `PlatformIO`). This code can be used for `Arduino` compilation, but requires platform support and library extensions.[Installation tutorial](/programing/Arduino_IDE)

#### Main test function introduction：

- RGB tri-color LED cycle gradient control test

- 6 ADC_channel AD acquisition test

- WiFi scan test

- Buzzer Gradient Control Test
