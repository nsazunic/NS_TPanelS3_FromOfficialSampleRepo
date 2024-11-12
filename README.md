<!--
 * @Description: None
 * @Author: LILYGO_L
 * @Date: 2023-09-11 16:13:14
 * @LastEditTime: 2024-11-12 15:54:40
 * @License: GPL 3.0
-->
<h1 align = "center">T-Panel</h1>

<p align="center" width="100%">
    <img src="image/13.jpg" alt="">
</p>

## **English | [中文](./README_CN.md)**

## Version iteration:
| Version     | Update date       |Update description|
| :----------------: | :---------------: |:---------------: |
| T-Panel_V1.0-V1.1     | 2023-11-23    |Original version      |
| T-Panel_V1.2       | 2023-12-11          |Modify the RS485 module to be replaceable with either an RS485 or CAN module|
| T-Panel_V1.3       | 2024-05-08          |Modify the structure|

## PurchaseLink

| Product                     | SOC           |  FLASH  |  PSRAM   | Link                   |
| :------------------------: | :-----------: |:-------: | :---------: | :------------------: |
| T-Panel_V1.0-V1.1   | ESP32S3 |   16M   | 8M  |  [LILYGO Mall](https://www.lilygo.cc/products/t-panel-s3?_pos=1&_sid=f6ce2c79c&_ss=r)  |
| T-Panel_V1.2   | ESP32S3 |   16M   | 8M  |  [LILYGO Mall](https://www.lilygo.cc/products/t-panel-s3?_pos=1&_sid=f6ce2c79c&_ss=r)  |
| T-Panel_V1.3   | ESP32S3 |   16M   | 8M  |  [LILYGO Mall](https://www.lilygo.cc/products/t-panel-s3?_pos=1&_sid=f6ce2c79c&_ss=r)  |

## Directory
- [Describe](#describe)
- [Preview](#preview)
- [Module](#module)
- [QuickStart](#quickstart)
- [PinOverview](#pinoverview)
- [FAQ](#faq)
- [Project](#project)
- [Information](#information)
- [DependentLibraries](#dependentlibraries)

## Describe

 T-Panel is an intelligent home product featuring a 480x480 RGB pixel large screen. It is controlled by the high-performance ESP32S3 chip onboard, which can communicate and exchange data with ESP32H2. The product also incorporates an RS485 chip for long-distance transmission of other devices, and its wide voltage input enhances compatibility.The screen of the T-Panel version is touch-enabled.

## Preview

### Actual Product Image

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

## Module

### 1.MCU

* MCU1: ESP32-S3
* PSRAM: 8MB
* FLASH: 16MB
* Others: For more information, please visit[Espressif Official ESP32-S3datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_cn.pdf)

* MCU2: ESP32-H2-MINI-1
* FLASH: 4MB
* Others: For more information, please visit[Espressif Official ESP32­-MINI-1datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-h2-mini-1_mini-1u_datasheet_cn.pdf)

### 2. Screen

* Screen Model: YDP395BT001
* Size: 3.95-inch
* Resolution Ratio: 480x480px
* Screen Type: IPS
* Driver Chip: ST7701S
* Using Bus Communication Protocol: Standard SPI+RGB
* Other: Use XL95x5 IO expansion chip for Standard SPI transmission, initialize the screen, and use RGB protocol for screen color drawing

### 3. SD Card Slot

### 4. IO Expansion

* Chip: XL9535
* Using bus communication protocol: IIC communication
* Other: Mainly used to initialize RGB screens

### 5. Telecommunication

* Chip: RS485 
* Using Bus Communication Protocol: uart communication

> #### T-Panel_V1.2-V1.3
> * Using Bus Communication Protocol: CAN
> * Using Bus Communication Protocol : TWAI

### 6. Touch
* Chip: CST3240
* Using Bus Communication Protocol: IIC

## QuickStart

### Examples Support

### Attention: Currently, ESP32H2 can only be programmed using the Arduino IDE

#### ESP32-S3
| Example | Support IDE And Version| Description | Picture |
| ------  | ------  | ------ | ------ | 
| [GFX_CST3240_Image_Rotation](./examples/GFX_CST3240_Image_Rotation) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [GFX_PDQ](./examples/GFX_PDQ) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [RS485](./examples/RS485) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [IIC_Scan_2](./examples/IIC_Scan_2) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [SD](./examples/SD) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [ESP32S3_ESP32H2_Uart](./examples/ESP32S3_ESP32H2_Uart) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [T-Panel_Test_V1_0-V1_1](./examples/T-Panel_Test_V1_0-V1_1) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` | Out-of-factory original test file|  |
| [T-Panel_Test_V1_2](./examples/T-Panel_Test_V1_2) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` | Out-of-factory original test file|  |
| [Wifi](./examples/Wifi) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [XL95x5](./examples/XL95x5) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [Lvgl](./examples/Lvgl) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [Lvgl_benchmark](./examples/Lvgl_benchmark) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |
| [CAN](./examples/CAN) | `[Platformio IDE][espressif32-v6.5.0]`<br />`[Arduino IDE][esp32_v2.0.14]` |  |  |

| Firmware | Description | Picture |
| ------  | ------  | ------ |
| [T-Panel_Test_V1_0-V1_1](./firmware/[ESP32S3][T-Panel_V1.0-V1.1][T-Panel_Test_V1_0-V1_1]_firmware_V1.0.4.bin) | Out-of-factory original test file |  |
| [T-Panel_Test_V1_2(RS485)](./firmware/[ESP32S3][T-Panel_V1.2][T-Panel_Test_V1_2]_firmware_V1.0.2(RS485).bin) | Out-of-factory original test file | |
| [T-Panel_Test_V1_2(CAN)](./firmware/[ESP32S3][T-Panel_V1.2][T-Panel_Test_V1_2]_firmware_V1.0.2(CAN).bin) | Out-of-factory original test file | |

#### ESP32-H2
| Example | Support IDE And Version| Description | Picture |
| ------  | ------  | ------ | ------ | 
| [ESP32H2_Uart_Callback](./examples/ESP32H2_Uart_Callback) |`[Arduino IDE][esp32-libs_V3.0.2]` | The factory initial raw files are used with the ESP32-S3 main chip in conjunction with the T-Panel_Test_V1.0-V1.1 version |  |
| [ESP32H2_BLE_Test](./examples/ESP32H2_BLE_Test) |`[Arduino IDE][esp32-libs_V3.0.2]` | The factory initial raw files are used with the ESP32-S3 main chip in conjunction with the T-Panel_Test_V1.2 version |  |

| Firmware | Description | Picture |
| ------  | ------  | ------ |
| [ESP32H2_Uart_Callback](./firmware/[ESP32H2][T-Panel_V1.0-V1.1][ESP32H2_Uart_Callback]_firmware_V1.0.2.bin) | The factory initial raw files are used with the ESP32-S3 main chip in conjunction with the T-Panel_Test_V1.0-V1.1 version |  |
| [ESP32H2_BLE_Test](./firmware/[ESP32H2][T-Panel_V1.2][ESP32H2_BLE_Test]_firmware_V1.0.2.bin) | The factory initial raw files are used with the ESP32-S3 main chip in conjunction with the T-Panel_Test_V1.2 version |  |

### PlatformIO
1. Install[VisualStudioCode](https://code.visualstudio.com/Download),Choose installation based on your system type.

2. Open the "Extension" section of the Visual Studio Code software sidebar(Alternatively, use "<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd>" to open the extension),Search for the "PlatformIO IDE" extension and download it.

3. During the installation of the extension, you can go to GitHub to download the program. You can download the main branch by clicking on the "<> Code" with green text, or you can download the program versions from the "Releases" section in the sidebar.

4. After the installation of the extension is completed, open the Explorer in the sidebar(Alternatively, use "<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>E</kbd>" go open it),Click on "Open Folder," locate the project code you just downloaded (the entire folder), and click "Add." At this point, the project files will be added to your workspace.

5. Open the "platformio.ini" file in the project folder (PlatformIO will automatically open the "platformio.ini" file corresponding to the added folder). Under the "[platformio]" section, uncomment and select the example program you want to burn (it should start with "default_envs = xxx") Then click "<kbd>[√](image/4.png)</kbd>" in the bottom left corner to compile,If the compilation is correct, connect the microcontroller to the computer and click "<kbd>[→](image/5.png)</kbd>" in the bottom left corner to download the program.

### Arduino
1. Install[Arduino](https://www.arduino.cc/en/software),Choose installation based on your system type.

2. Open the "example" directory within the project folder, select the example project folder, and open the file ending with ".ino" to open the Arduino IDE project workspace.

3. Open the "Tools" menu at the top right -> Select "Board" -> "Board Manager." Find or search for "esp32" and download the board files from the author named "Espressif Systems." Then, go back to the "Board" menu and select the development board type under "ESP32 Arduino." The selected development board type should match the one specified in the "platformio.ini" file under the [env] section with the header "board = xxx." If there is no corresponding development board, you may need to manually add the development board from the "board" directory within your project folder.

4. Open menu bar "[File](image/6.png)" -> "[Preferences](image/6.png)" ,Find "[Sketchbook location](image/7.png)"  here,copy and paste all library files and folders from the "libraries" folder in the project directory into the "libraries" folder in this directory.

5. Select the correct settings in the Tools menu, as shown in the table below.

#### ESP32-S3
| Setting                               | Value                                 |
| :-------------------------------: | :-------------------------------: |
| Board                                | ESP32S3 Dev Module           |
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

6. Select the correct port.

7. Click "<kbd>[√](image/8.png)</kbd>" in the upper right corner to compile,If the compilation is correct, connect the microcontroller to the computer,Click "<kbd>[→](image/9.png)</kbd>" in the upper right corner to download.

### firmware download
1. Open the project file "tools" and locate the ESP32 burning tool. Open it.

2. Select the correct burning chip and burning method, then click "OK." As shown in the picture, follow steps 1->2->3->4->5 to burn the program. If the burning is not successful, press and hold the "BOOT-0" button and then download and burn again.

3. Burn the file in the root directory of the project file "[firmware](./firmware/)" file,There is a description of the firmware file version inside, just choose the appropriate version to download.

<p align="center" width="100%">
    <img src="image/10.png" alt="example">
    <img src="image/11.png" alt="example">
</p>


## PinOverview

| Display Pin       | ESP32S3 Pin|XL95X5 Pin    |
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

| Display Screen Touch Pin       | ESP32S3 Pin|XL95X5 Pin      |
| :------------------: | :------------------:| :------------------:|
| INT         | ESP32S3_IO21                 |       NULL         |
| RST         |         NULL         |       XL95X5_IO4         |
| SDA         |         ESP32S3_IO17       |       NULL         |
| SCL         |         ESP32S3_IO18       |       NULL         |

| SD Pin           | ESP32S3 Pin      |
| :------------------: | :------------------:|
| CS                     | IO38                  |
| SCLK                  | IO36                    |
| MOSI                  | IO35                  |
| MISO                  | IO37                    |

> #### T-Panel_V1.0-V1.1
> | RS485 pin    | ESP32S3 pin      |XL95x5 pin     |
> | :------------------: | :------------------:| :------------------:|
> | TX                     | ESP32S3_IO15                  |NULL           |
> | RX                     | ESP32S3_IO16                  |NULL           |
> | CON                  |          NULL           | XL95x5_IO7        |

> #### T-Panel_V1.2
> | RS485 and CAN share pins    | ESP32S3 pin      |
> | :------------------: | :------------------:| 
> | TX                     | ESP32S3_IO16     |
> | RX                     | ESP32S3_IO15      |

| Function     | ESP32H2 Pin     | ESP32S3 Pin      | XL95X5 Pin      |
| :-------: | :----------: |  :------------------:|:------------------:|
| Activate The BOOT Mode Of ESP32H2  | ESP32H2_IO9     | ESP32S3_IO33      |        NULL         |
| Reset ESP32H2              | ESP32H2_Pin Number 8      | ESP32S3_IO34     |        NULL         |
| Uart  | ESP32H2_TX_IO24     | ESP32S3_RX_IO48     |        NULL         |
| Uart  | ESP32H2_RX_IO23        | ESP32S3_TX_IO47   |        NULL         |
| IO  | ESP32H2_IO12                   |      NULL         |        XL95X5_IO1         |
| IO  | ESP32H2_IO4                     |       NULL        |        XL95X5_IO2         |
| IO  | ESP32H2_IO5                     |        NULL       |        XL95X5_IO3         |

## FAQ

* Q. After reading the above tutorials, I still don't know how to build a programming environment. What should I do?
* A. If you still don't understand how to build an environment after reading the above tutorials, you can refer to the [LilyGo-Document](https://github.com/Xinyuan-LilyGO/LilyGo-Document) document instructions to build it.

<br />

* Q. Why does Arduino IDE prompt me to update library files when I open it? Should I update them or not?
* A. Choose not to update library files. Different versions of library files may not be mutually compatible, so it is not recommended to update library files.

<br />

* Q. Why is there no serial data output on the "Uart" interface on my board? Is it defective and unusable?
* A. The default project configuration uses the USB interface as Uart0 serial output for debugging purposes. The "Uart" interface is connected to Uart0, so it won't output any data without configuration.<br />For PlatformIO users, please open the project file "platformio.ini" and modify the option under "build_flags = xxx" from "-D ARDUINO_USB_CDC_ON_BOOT=true" to "-D ARDUINO_USB_CDC_ON_BOOT=false" to enable external "Uart" interface.<br />For Arduino users, open the "Tools" menu and select "USB CDC On Boot: Disabled" to enable the external "Uart" interface.

<br />

* Q. Why can't I find the ESP32H2 chip library on Arduino?
* A. The ESP32H2 chip library for Arduino is currently in the testing phase. You can download the "package_esp32_dev_index.json" file from the [arduino-esp32](https://github.com/espressif/arduino-esp32) GitHub repository for versions 3.0.0 and above, and import it into the Arduino IDE to see the ESP32H2 chip library.

<br />

* Q. Why is my board continuously failing to download the program?
* A. Please hold down the "BOOT-0" button and try downloading the program again.

## Project
* [T-Panel_V1.2](./project/T-Panel_V1.2.pdf)

## Information
* [Espressif](https://www.espressif.com/en/support/documents/technical-documents)
* [XL9535](./information/XL9535.pdf)
* [YDP395BT001-V2](./information/YDP395BT001-V2.pdf)
* [HYNITRON-CST3240_V1.0](./information/HYNITRON-CST3240_V1.0.pdf)
* [EBYTE-RSM485MT5V](./information/EBYTE-RSM485MT5V.pdf)
* [ST7701S_SPEC_V1.4](./information/ST7701S_SPEC_V1.4.pdf)
* [TD501MCANFD_MORNSUN](./information/TD501MCANFD_MORNSUN.pdf)

## DependentLibraries
* [Arduino_GFX-1.4.6](https://github.com/moononournation/Arduino_GFX)
* [TouchLib](https://github.com/mmMicky/TouchLib)
* [lvgl-8.3.5](https://github.com/lvgl/lvgl)
* [ESP32_USB_Stream-0.0.1](https://github.com/esp-arduino-libs/ESP32_USB_Stream)
* [JPEGDEC-1.2.8](https://github.com/bitbank2/JPEGDEC)
* [MiniTV](https://github.com/moononournation/MiniTV)
