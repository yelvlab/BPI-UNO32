# BPI:bit Webduino                        ![LOGO](/pic/logo.jpg)

[[官方英文论坛]](http://forum.banana-pi.org/c/BPI-Iot-module/BPI-Webduino) [[官方中文论坛]](https://forum.banana-pi.org.cn/c/bpi-webduino)

![](/pic/overview.jpg)

本产品采用ESP32作为核心进行设计。

> ESP-WROOM-32

> 448KB ROM

> 520KB RAM

> Wi-Fi&BLE


**BPI:UNO32**采用了与`Arduino UNO R3`类似的结构与布局，为广大Arduino用户提供无缝替换的使用体验，同时ESP32同样可以采用Arduino IDE进行编程。同时您也可以使用官方编译工具ESP-IDF或者开源编译插件PlatformIO for Atom/VS Code

## 目录导读

1. [`doc`](/doc)存放BPI:uno32板的原理图以及ESP-WROOM-32等各个部分的datesheet

2. [`pic`](/pic)存放BPI:uno32板的照片与各种示意图

3. [`Test_Code`](/Test_Code)存放BPI:uno32板基础功能测试代码

3. [`programing`](/programing)目录下面介绍了使用不同的软件烧录的方法。

## BPI-UNO32 Pin Define

<table>
   <tr>
      <td>GPIO Pin Name</td>
      <td>Function</td>
   </tr>
   <tr>
      <td>16</td>
      <td>GPIO16, HS1_DATA4, U2RXD, EMAC_CLK_OUT</td>
   </tr>
   <tr>
      <td>17</td>
      <td>GPIO17, HS1_DATA5, U2TXD, EMAC_CLK_OUT_180</td>
   </tr>
   <tr>
      <td>EN</td>
      <td>Chip-enable signal. Active high</td>
   </tr>
   <tr>
      <td>3V3</td>
      <td>3V3 DC Power Out</td>
   </tr>
   <tr>
      <td>5V</td>
      <td>5V DC Power Out</td>
   </tr>
   <tr>
      <td>GND</td>
      <td>Ground</td>
   </tr>
   <tr>
      <td>GND</td>
      <td>Ground</td>
   </tr>
   <tr>
      <td>VIN</td>
      <td>DC Power In</td>
   </tr>
   <tr>
      <td></td>
      <td></td>
   </tr>
   <tr>
      <td>36/A0</td>
      <td>GPIO36, SENSOR_VP, ADC_H, ADC1_CH0, RTC_GPIO0</td>
   </tr>
   <tr>
      <td>39/A3</td>
      <td>GPIO39, SENSOR_VN, ADC1_CH3, ADC_H, RTC_GPIO3</td>
   </tr>
   <tr>
      <td>32/A4</td>
      <td>GPIO32, XTAL_32K_P (32.768 kHz crystal oscillator input), ADC1_CH4,TOUCH9, RTC_GPIO9</td>
   </tr>
   <tr>
      <td>33/A5</td>
      <td>GPIO33, XTAL_32K_N (32.768 kHz crystal oscillator output), ADC1_CH5,TOUCH8, RTC_GPIO8</td>
   </tr>
   <tr>
      <td>34/A6</td>
      <td>GPIO34, ADC1_CH6, RTC_GPIO4</td>
   </tr>
   <tr>
      <td>35/A7</td>
      <td>GPIO35, ADC1_CH7, RTC_GPIO5</td>
   </tr>
   <tr>
      <td></td>
      <td></td>
   </tr>
   <tr>
      <td>22/SCL</td>
      <td>GPIO22, VSPIWP, U0RTS, EMAC_TXD1</td>
   </tr>
   <tr>
      <td>21/SDA</td>
      <td>GPIO21, VSPIHD, EMAC_TX_EN</td>
   </tr>
   <tr>
      <td>27</td>
      <td>GPIO27, ADC2_CH7, TOUCH7, RTC_GPIO17, EMAC_RX_DV</td>
   </tr>
   <tr>
      <td>GND</td>
      <td>Ground</td>
   </tr>
   <tr>
      <td>18/SCK</td>
      <td>GPIO18, VSPICLK, HS1_DATA7</td>
   </tr>
   <tr>
      <td>19/MISO</td>
      <td>GPIO19, VSPIQ, U0CTS, EMAC_TXD0</td>
   </tr>
   <tr>
      <td>23/MOSI</td>
      <td>GPIO23, VSPID, HS1_STROBE</td>
   </tr>
   <tr>
      <td>05/SS</td>
      <td>GPIO5, VSPICS0, HS1_DATA6, EMAC_RX_CLK</td>
   </tr>
   <tr>
      <td>26/DA2</td>
      <td>GPIO26, DAC_2, ADC2_CH9, RTC_GPIO7, EMAC_RXD1</td>
   </tr>
   <tr>
      <td>25/DA1</td>
      <td>GPIO25, DAC_1, ADC2_CH8, RTC_GPIO6, EMAC_RXD0</td>
   </tr>
   <tr>
      <td></td>
      <td></td>
   </tr>
   <tr>
      <td>14/SCK</td>
      <td>GPIO14, ADC2_CH6, TOUCH6, RTC_GPIO16, MTMS, HSPICLK,HS2_CLK, SD_CLK, EMAC_TXD2</td>
   </tr>
   <tr>
      <td>12/MISO</td>
      <td>GPIO12, ADC2_CH5, TOUCH5, RTC_GPIO15, MTDI, HSPIQ,HS2_DATA2, SD_DATA2, EMAC_TXD3</td>
   </tr>
   <tr>
      <td>13/MOSI</td>
      <td>GPIO13, ADC2_CH4, TOUCH4, RTC_GPIO14, MTCK, HSPID,HS2_DATA3, SD_DATA3, EMAC_RX_ER</td>
   </tr>
   <tr>
      <td>15/SS</td>
      <td>GPIO15, ADC2_CH3, TOUCH3, MTDO, HSPICS0, RTC_GPIO13,HS2_CMD, SD_CMD, EMAC_RXD3</td>
   </tr>
   <tr>
      <td>04</td>
      <td>GPIO4, ADC2_CH0, TOUCH0, RTC_GPIO10, HSPIHD, HS2_DATA1,SD_DATA1, EMAC_TX_ER</td>
   </tr>
   <tr>
      <td>02</td>
      <td>GPIO2, ADC2_CH2, TOUCH2, RTC_GPIO12, HSPIWP, HS2_DATA0,SD_DATA0</td>
   </tr>
   <tr>
      <td>01->TX</td>
      <td>GPIO1, U0TXD, CLK_OUT3, EMAC_RXD2</td>
   </tr>
   <tr>
      <td>03<-RX</td>
      <td>GPIO3, U0RXD, CLK_OUT2</td>
   </tr>
   <tr>
      <td></td>
      <td></td>
   </tr>
   <tr>
      <td>VCC</td>
      <td>3V3 DC Power Out</td>
   </tr>
   <tr>
      <td>GND</td>
      <td>Ground</td>
   </tr>
   <tr>
      <td>SCL</td>
      <td>GPIO22, VSPIWP, U0RTS, EMAC_TXD1</td>
   </tr>
   <tr>
      <td>SDA</td>
      <td>GPIO21, VSPIHD, EMAC_TX_EN</td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>

### 丝印图：

![](/pic/top.png)

![](/pic/bot.png)
