<!--
 * @Description: None
 * @Author: LILYGO_L
 * @Date: 2023-09-11 16:13:14
 * @LastEditTime: 2024-11-12 15:54:07
 * @License: GPL 3.0
-->
<h1 align = "center">T-Panel</h1>

<p align="center" width="100%">
    <img src="image/13.jpg" alt="">
</p>

## **[English](./README.md) | 中文**

## 版本迭代:
| Version     | Update date       |Update description|
| :----------------: | :---------------: |:---------------: |
| T-Panel_V1.0-V1.1     | 2023-11-23    |初始版本      |
| T-Panel_V1.2       | 2023-12-11          |将RS485模块修改成可替换模块RS485和CAN|
| T-Panel_V1.3       | 2024-05-08          |修改结构|

## 购买链接
| Product                     | SOC           |  FLASH  |  PSRAM   | Link                   |
| :------------------------: | :-----------: |:-------: | :---------: | :------------------: |
| T-Panel_V1.0-V1.1   | ESP32S3 |   16M   | 8M  |  [LILYGO Mall](https://www.lilygo.cc/products/t-panel-s3?_pos=1&_sid=f6ce2c79c&_ss=r)  |
| T-Panel_V1.2   | ESP32S3 |   16M   | 8M  |  [LILYGO Mall](https://www.lilygo.cc/products/t-panel-s3?_pos=1&_sid=f6ce2c79c&_ss=r)  |
| T-Panel_V1.3   | ESP32S3 |   16M   | 8M  |  [LILYGO Mall](https://www.lilygo.cc/products/t-panel-s3?_pos=1&_sid=f6ce2c79c&_ss=r)  |

## 目录
- [描述](#描述)
- [预览](#预览)
- [模块](#模块)
- [快速开始](#快速开始)
- [引脚总览](#引脚总览)
- [常见问题](#常见问题)
- [项目](#项目)
- [资料](#资料)
- [依赖库](#依赖库)

## 描述

T-Panel是一款拥有480x480RGB像素大屏的智能家居产品。板载高性能ESP32S3芯片控制屏幕，可与ESP32H2相互通信交换数据。产品还搭载RS485芯片可实现对其他设备进行远距离传输，宽电压输入使得产品兼容性更高。T-Panel版本的屏幕是带触摸的。

## 预览

### 实物图

<p align="center" width="100%">
    <img src="image/12.jpg" alt="">
</p>

---

<p align="center" width="100%">
    <img src="image/13.jpg" alt="">
</p>

---

<p align="center" width="100%">
    <img src="image/14.jpg" alt="">
</p>

## 模块

### 1. MCU

* MCU1：ESP32-S3
* PSRAM：8MB
* FLASH：16MB
* 其他说明：更多资料请访问[乐鑫官方ESP32­-S3 数据手册](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_cn.pdf)

* MCU2：ESP32-H2-MINI-1
* FLASH：4MB
* 其他说明：更多资料请访问[乐鑫官方ESP32­-MINI-1数据手册](https://www.espressif.com/sites/default/files/documentation/esp32-h2-mini-1_mini-1u_datasheet_cn.pdf)

### 2. 屏幕

* 屏幕型号：YDP395BT001
* 尺寸：3.95英寸
* 分辨率：480x480px
* 屏幕类型：IPS
* 驱动芯片：ST7701S
* 使用总线通信协议：标准SPI+RGB
* 其他说明：使用XL95x5 IO扩展芯片进行标准SPI传输初始化屏幕后使用RGB协议进行屏幕色彩绘制

### 3. SD卡槽

### 4. IO扩展

* 芯片：XL9535
* 使用总线通信协议：IIC通信
* 其他说明：主要用于初始化RGB屏幕

### 5. 远距离通信

* 模块：RS485 
* 使用总线通信协议：UART通信

> #### T-Panel_V1.2-V1.3
> * 模块：CAN
> * 总线通信协议：TWAI通信

### 6. 屏幕触摸
* 芯片：CST3240
* 使用总线通信协议：IIC通信

## 快速开始

### 示例支持

### 注意事项：目前ESP32H2只能使用Arduino IDE进行编程

#### ESP32-S3
| Example | Support IDE And Version| Description | Picture |
| ------  | ------  | ------ | ------ | 
| [GFX_CST3240_Image_Rotation](./examples/GFX_CST3240_Image_Rotation) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [GFX_PDQ](./examples/GFX_PDQ) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [RS485](./examples/RS485) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [IIC_Scan_2](./examples/IIC_Scan_2) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [SD](./examples/SD) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [ESP32S3_ESP32H2_Uart](./examples/ESP32S3_ESP32H2_Uart) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [T-Panel_Test_V1_0-V1_1](./examples/T-Panel_Test_V1_0-V1_1) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` | 出厂初始测试文件|  |
| [T-Panel_Test_V1_2](./examples/T-Panel_Test_V1_2) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` | 出厂初始测试文件|  |
| [Wifi](./examples/Wifi) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [XL95x5](./examples/XL95x5) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [Lvgl](./examples/Lvgl) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [Lvgl_benchmark](./examples/Lvgl_benchmark) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [CAN](./examples/CAN) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |

| Firmware | Description | Picture |
| ------  | ------  | ------ |
| [T-Panel_Test_V1_0-V1_1](./firmware/[ESP32S3][T-Panel_V1.0-V1.1][T-Panel_Test_V1_0-V1_1]_firmware_V1.0.4.bin) | 出厂初始测试文件 |  |
| [T-Panel_Test_V1_2(RS485)](./firmware/[ESP32S3][T-Panel_V1.2][T-Panel_Test_V1_2]_firmware_V1.0.2(RS485).bin) | 出厂初始测试文件 | |
| [T-Panel_Test_V1_2(CAN)](./firmware/[ESP32S3][T-Panel_V1.2][T-Panel_Test_V1_2]_firmware_V1.0.2(CAN).bin) | 出厂初始测试文件 | |

#### ESP32-H2
| Example | Support IDE And Version| Description | Picture |
| ------  | ------  | ------ | ------ | 
| [ESP32H2_Uart_Callback](./examples/ESP32H2_Uart_Callback) |`[Arduino IDE][esp32-libs_V3.0.2]` | 出厂初始测试文件搭配T-Panel_Test_V1_0-V1_1版本的ESP32-S3主芯片使用 |  |
| [ESP32H2_BLE_Test](./examples/ESP32H2_BLE_Test) |`[Arduino IDE][esp32-libs_V3.0.2]` | 出厂初始测试文件搭配T-Panel_Test_V1_2版本的ESP32-S3的主芯片使用 |  |

| Firmware | Description | Picture |
| ------  | ------  | ------ |
| [ESP32H2_Uart_Callback](./firmware/[ESP32H2][T-Panel_V1.0-V1.1][ESP32H2_Uart_Callback]_firmware_V1.0.2.bin) | 出厂初始测试文件搭配T-Panel_Test_V1_0-V1_1版本的ESP32-S3主芯片使用 |  |
| [ESP32H2_BLE_Test](./firmware/[ESP32H2][T-Panel_V1.2][ESP32H2_BLE_Test]_firmware_V1.0.2.bin) | 出厂初始测试文件搭配T-Panel_Test_V1_2版本的ESP32-S3的主芯片使用 |  |

### PlatformIO
1. 安装[VisualStudioCode](https://code.visualstudio.com/Download)，根据你的系统类型选择安装。

2. 打开VisualStudioCode软件侧边栏的“扩展”（或者使用<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd>打开扩展），搜索“PlatformIO IDE”扩展并下载。

3. 在安装扩展的期间，你可以前往GitHub下载程序，你可以通过点击带绿色字样的“<> Code”下载主分支程序，也通过侧边栏下载“Releases”版本程序。

4. 扩展安装完成后，打开侧边栏的资源管理器（或者使用<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>E</kbd>打开），点击“打开文件夹”，找到刚刚你下载的项目代码（整个文件夹），点击“添加”，此时项目文件就添加到你的工作区了。

5. 打开项目文件中的“platformio.ini”（添加文件夹成功后PlatformIO会自动打开对应文件夹的“platformio.ini”）,在“[platformio]”目录下取消注释选择你需要烧录的示例程序（以“default_envs = xxx”为标头），然后点击左下角的“<kbd>[√](image/4.png)</kbd>”进行编译，如果编译无误，将单片机连接电脑，点击左下角“<kbd>[→](image/5.png)</kbd>”即可进行烧录。

### Arduino
1. 安装[Arduino](https://www.arduino.cc/en/software)，根据你的系统类型选择安装。

2. 打开项目文件夹的“example”目录，选择示例项目文件夹，打开以“.ino”结尾的文件即可打开Arduino IDE项目工作区。

3. 打开右上角“工具”菜单栏->选择“开发板”->“开发板管理器”，找到或者搜索“esp32”，下载作者名为“Espressif Systems”的开发板文件。接着返回“开发板”菜单栏，选择“ESP32 Arduino”开发板下的开发板类型，选择的开发板类型由“platformio.ini”文件中以[env]目录下的“board = xxx”标头为准，如果没有对应的开发板，则需要自己手动添加项目文件夹下“board”目录下的开发板。

4. 打开菜单栏“[文件](image/6.png)”->“[首选项](image/6.png)”，找到“[项目文件夹位置](image/7.png)”这一栏，将项目目录下的“libraries”文件夹里的所有库文件连带文件夹复制粘贴到这个目录下的“libraries”里边。

5. 在 "工具 "菜单中选择正确的设置，如下表所示。

#### ESP32-S3
| Setting                               | Value                                 |
| :-------------------------------: | :-------------------------------: |
| Board                                | ESP32S3 Dev Module            |
| Upload Speed                     | 921600                               |
| USB Mode                           | Hardware CDC and JTAG     |
| USB CDC On Boot                | Enabled                             |
| USB Firmware MSC On Boot | Disabled                             |
| USB DFU On Boot                | Disabled                             |
| CPU Frequency                   | 240MHz (WiFi)                    |
| Flash Mode                         | QIO 80MHz                         |
| Flash Size                           | 16MB (128Mb)                     |
| Core Debug Level                | None                                 |
| Partition Scheme                | 16M Flash (3MB APP/9.9MB FATFS) |
| PSRAM                                | QSPI PSRAM                         |
| Arduino Runs On                  | Core 1                               |
| Events Run On                     | Core 1                               |

#### ESP32-H2
| Setting                               | Value                                 |
| :-------------------------------: | :-------------------------------: |
| Board                                | ESP32H2 Dev Module          |
| Upload Speed                     | 921600                               |
| USB CDC On Boot                | Disabled                             |
| CPU Frequency                   | 64MHz                              |
| Flash Mode                         | QIO                                   |
| Flash Size                           | 4MB (32Mb)                     |
| Core Debug Level                | None                                 |

6. 选择正确的端口。

7. 点击右上角“<kbd>[√](image/8.png)</kbd>”进行编译，如果编译无误，将单片机连接电脑，点击右上角“<kbd>[→](image/9.png)</kbd>”即可进行烧录。

### firmware烧录
1. 打开项目文件“tools”找到ESP32烧录工具，打开。

2. 选择正确的烧录芯片以及烧录方式点击“OK”，如图所示根据步骤1->2->3->4->5即可烧录程序，如果烧录不成功，请按住“BOOT-0”键再下载烧录。

3. 烧录文件在项目文件根目录“[firmware](./firmware/)”文件下，里面有对firmware文件版本的说明，选择合适的版本下载即可。

<p align="center" width="100%">
    <img src="image/10.png" alt="example">
    <img src="image/11.png" alt="example">
</p>


## 引脚总览

| 显示屏引脚       | ESP32S3引脚|XL95X5引脚      |
| :------------------: | :------------------:| :------------------:|
| VSYNC              | ESP32S3_IO40                  |       NULL         |
| HSYNC              | ESP32S3_IO39                  |       NULL         |
| PCLK                | ESP32S3_IO41                  |       NULL         |
| B0                    | ESP32S3_IO1                   |       NULL         |
| B1                    | ESP32S3_IO2                  |       NULL         |
| B2                    | ESP32S3_IO3                  |       NULL         |
| B3                    | ESP32S3_IO4                  |       NULL         |
| B4                    | ESP32S3_IO5                  |       NULL         |
| G0                    | ESP32S3_IO6                  |       NULL         |
| G1                    | ESP32S3_IO7                  |       NULL         |
| G2                    | ESP32S3_IO8                  |       NULL         |
| G3                    | ESP32S3_IO9                  |       NULL         |
| G4                    | ESP32S3_IO10                 |       NULL         |
| G5                    | ESP32S3_IO11                 |       NULL         |
| R0                    | ESP32S3_IO12                 |       NULL         |
| R1                    | ESP32S3_IO13                 |       NULL         |
| R2                    | ESP32S3_IO42                 |       NULL         |
| R3                    | ESP32S3_IO46                 |       NULL         |
| R4                    |ESP32S3_ IO45                 |       NULL         |
| BL                    | ESP32S3_IO14                 |       NULL         |
| CS                    |        NULL         |  XL95X5_IO17                 |
| SCLK                |         NULL         | XL95X5_IO15                  | 
| MOSI                |         NULL         | XL95X5_IO16                  | 
| RST              |         NULL          |       XL95X5_IO5         |

| 显示屏触摸引脚       | ESP32S3引脚|XL95X5引脚      |
| :------------------: | :------------------:| :------------------:|
| INT         | ESP32S3_IO21                 |       NULL         |
| RST         |         NULL         |       XL95X5_IO4         |

| SD卡引脚           | ESP32S3引脚      |
| :------------------: | :------------------:|
| CS                     | IO38                  |
| SCLK                  | IO36                    |
| MOSI                  | IO35                  |
| MISO                  | IO37                    |

> #### T-Panel_V1.0-V1.1
> | RS485引脚    | ESP32S3引脚      |XL95x5引脚      |
> | :------------------: | :------------------:| :------------------:|
> | TX                     | ESP32S3_IO15                  |NULL           |
> | RX                     | ESP32S3_IO16                  |NULL           |
> | CON                  |          NULL           | XL95x5_IO7        |

> #### T-Panel_V1.2
> | RS485和CAN共用引脚    | ESP32S3引脚      |
> | :------------------: | :------------------:| 
> | TX                     | ESP32S3_IO16     |
> | RX                     | ESP32S3_IO15      |

| 功能     | ESP32H2引脚     | ESP32S3引脚      | XL95X5引脚      |
| :-------: | :----------: |  :------------------:|:------------------:|
| 启动ESP32H2的BOOT模式  | ESP32H2_IO9     | ESP32S3_IO33      |        NULL         |
| 复位ESP32H2              | ESP32H2_引脚序号8      | ESP32S3_IO34     |        NULL         |
| Uart  | ESP32H2_TX_IO24     | ESP32S3_RX_IO48     |        NULL         |
| Uart  | ESP32H2_RX_IO23        | ESP32S3_TX_IO47   |        NULL         |
| IO  | ESP32H2_IO12                   |      NULL         |        XL95X5_IO1         |
| IO  | ESP32H2_IO4                     |       NULL        |        XL95X5_IO2         |
| IO  | ESP32H2_IO5                     |        NULL       |        XL95X5_IO3         |

## 常见问题

* Q. 看了以上教程我还是不会搭建编程环境怎么办？
* A. 如果看了以上教程还不懂如何搭建环境的可以参考[LilyGo-Document](https://github.com/Xinyuan-LilyGO/LilyGo-Document)文档说明来搭建。

<br />

* Q. 为什么打开Arduino IDE时他会提醒我是否要升级库文件？我应该升级还是不升级？
* A. 选择不升级库文件，不同版本的库文件可能不会相互兼容所以不建议升级库文件。

<br />

* Q. 为什么我的板子上“Uart”接口没有输出串口数据，是不是坏了用不了啊？
* A. 因为项目文件默认配置将USB接口作为Uart0串口输出作为调试，“Uart”接口连接的是Uart0，不经配置自然是不会输出任何数据的。<br />PlatformIO用户请打开项目文件“platformio.ini”，将“build_flags = xxx”下的选项“-DARDUINO_USB_CDC_ON_BOOT=true”修改成“-DARDUINO_USB_CDC_ON_BOOT=false”即可正常使用外部“Uart”接口。<br />Arduino用户打开菜单“工具”栏，选择USB CDC On Boot: “Disabled”即可正常使用外部“Uart”接口。

<br />

* Q. 为什么我在Arduion上找不到ESP32H2这个芯片的库呢？
* A. 目前ESP32H2这款芯片的Arduino库正处于测试阶段，您可以去GitHub上的[arduino-esp32](https://github.com/espressif/arduino-esp32)下载3.0.0分支版本以上的
“package_esp32_dev_index.json”文件，导入Arduino IDE即可看到ESP32H2芯片库

<br />

* Q. 为什么我的板子一直烧录失败呢？
* A. 请按住“BOOT-0”按键重新下载程序。

## 项目
* [T-Panel_V1.2](./project/T-Panel_V1.2.pdf)

## 资料
* [Espressif](https://www.espressif.com/en/support/documents/technical-documents)
* [XL9535](./information/XL9535.pdf)
* [YDP395BT001-V2](./information/YDP395BT001-V2.pdf)
* [HYNITRON-CST3240_V1.0](./information/HYNITRON-CST3240_V1.0.pdf)
* [EBYTE-RSM485MT5V](./information/EBYTE-RSM485MT5V.pdf)
* [ST7701S_SPEC_V1.4](./information/ST7701S_SPEC_V1.4.pdf)
* [TD501MCANFD_MORNSUN](./information/TD501MCANFD_MORNSUN.pdf)

## 依赖库
* [Arduino_GFX-1.4.6](https://github.com/moononournation/Arduino_GFX)
* [TouchLib](https://github.com/mmMicky/TouchLib)
* [lvgl-8.3.5](https://github.com/lvgl/lvgl)
* [ESP32_USB_Stream-0.0.1](https://github.com/esp-arduino-libs/ESP32_USB_Stream)
* [JPEGDEC-1.2.8](https://github.com/bitbank2/JPEGDEC)
* [MiniTV](https://github.com/moononournation/MiniTV)
