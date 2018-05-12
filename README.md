RAK Wireless RAK815 nRF52832 Breakout
========================================

[[RAK Wireless RAK815 nRF52832 Breakout]](https://www.aliexpress.com/item/RAK815-Hybrid-Location-Tracker-LoRa-Bluetooth-5-0-Beacon-GPS-Sensors-LCD-LoRaWAN-1-0-2/32849717052.html)

The nRF52832 is [Nordic Semiconductor's](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF52832) latest multiprotocol radio system-on-chip (SoC). It's half microcontroller, with a list of features including 32 configurable I/O pins, SPI, I<sup>2</sup>C, UART, PWM, ADC's, 512kB flash, and 64kB RAM. And, it's half 2.4GHz multiprotocol radio, supporting **Bluetooth low energy** (BLE), **ANT**, and Nordic's proprietary 2.4GHz ultra low-power wireless communication -- it even features on-chip NFC tag support.

RAK815(RAK813 BreakBoard) is a wireless remote solution based on the RAK813 +
GPS + MEMS + HT+LCD design. It integrates the latest LoRaWAN 1.0.2 protocol and the
latest Bluetooth 5.0 protocol, supports LoRaWAN working mode, supports Bluetooth
transparent transmission, Bluetooth up to 300 meters away..

RAK815(RAK813 BreakBoard) built-in GPS, acceleration, temperature and humidity
sensors, expanded I2C LCD interface. We provide case applications that can configure
LoRaWAN parameters using Bluetooth, display sensor data using LCD, and upload
sensor data to the LoRaWAN network. And all the code open source. Users can find all
the open source code in github. We also designed three customizable buttons and two
customizable LED lights for our users, allowing users to implement they idea with
open-source code.

RAK815(RAK813 BreakBoard) is also a support for battery-powered products.
Greatly expanded product application scenarios. We also designed the function to enter
the low power mode when the device is detected to be stationary to ensure battery life.
The device also supports RAK831 + Ri3 gateway to use, you can graphically display the
various data of the sensor in the Cayenne platform, but also support the real-time
observation of sensor data on the phone.


Repository Contents
-------------------
* **/Firmware** - Serial bootloader source and hex files

Documentation
--------------
* **[Arduino Hardware Definitions](https://github.com/sparkfun/Arduino_Boards/)** - Arduino cores and tools for the nRF52.

Download and Install the Board Package
-------------
The nRF52 Arduino cores are based on the great work by sandeepmistry. Sparkfun has added nRF52832 Breakout Board compatibility to his board files, and added an extra tool to enable serial bootloading.

Since the RAK wireless RAK815 is just having a few extra LEDs and Buttons that the Sparkfun board, it was easy to port the bootloader functionality.

* To install support for the nRF52 board in Arduino, begin by opening your Arduino preferences (File > Preferences). Then copy and paste the URL below into the “Additional Board Manager URLs” text box.

https://raw.githubusercontent.com/sparkfun/Arduino_Boards/nrf5/IDE_Board_Manager/package_sparkfun_index.json

* Then hit OK, and navigate to the Tools > Board > Boards Manager… tool. A search for “nRF52” should turn up a SparkFun nRF52 Boards result. Select that and click install.
* The install may take a few minutes – the package includes arm-gcc and a few other tools totaling around 100 MB. Once the installation is complete, go to Tools > Board and select “SparkFun nRF52832 Breakout” under the “Nordic Semiconductor nRF5 Boards” section.
* You can now create Sketches using the BLEPeripheral library as well and compile them for the RAK815 board.

Install the RAKWireless RAK815 Board variant
--------------------
It is easy to install the RAkWireless Board variant into the IDE (For ubuntu/other linux users)

* Copy the Boards.txt into .arduino15/packages/SparkFun/hardware/nRF5/0.2.3/boards.txt
* Copy the RAK815_nrf52832_Breakout folder in the variants folder in the path .arduino15/packages/SparkFun/hardware/nRF5/0.2.3

For Windows users, just search for the path that has the packages/Sparkfun folder :)

* Next, restart Arduino IDE, you should be able to see an entry for the RAK Wireless RAK815 board. Now you can flash as you normally do




Build and use the bootloader
-------------------
To build the bootloader follow the steps below

* Clone the Repository
* cd to nRF52832_Breakout folder and do make clean
* Then, execute the command "make sfe_nrf52832_dfu"
* Once the program successfully builds, just connect your RAK815 over SWD interface using your JLink module
* execute the command "./flash_bootloader.sh"

Board Hardware details
-------------------
* SW3 is the board reset switch
* SW1 is the board bootloader switch
* LED6 is the bootloader time-bomb LED (currently not working, fix on the way)

How to enter Serial-Bootloader mode
-------------
When you want to enter bootloader mode, keep SW1 pressed, then press SW3 and release SW3 after a second and then release SW1.


Product Versions
----------------
* [RAK Wireless RAK815 nRF52832 (RAK815)](https://www.aliexpress.com/item/RAK815-Hybrid-Location-Tracker-LoRa-Bluetooth-5-0-Beacon-GPS-Sensors-LCD-LoRaWAN-1-0-2/32849717052.html)- Initial release of the RAK Wireless RAK815 nRF52832 Breakout

Version History
---------------
* v1.0 Support for the RAK815 board. LED indicator for bootloader is not working. fix on the way !!

License Information
-------------------
This product is completely _**open source**_! Please fork and provide your valuable feedback.

Special Thanks !!!!!
-------------------
THANKS a bunch to the awesome guys at Sparkfun for their original serial bootloader that i have reused for this board.

Their git repo is here:
https://github.com/sparkfun/nRF52832_Breakout
