Arduino Support files
======

This folder contains the Arduino IDE support files:

Contents
------
* **/libraries**: folder containing additional libraries for the nrf52 core
* **/RAK815_nrf52832_Breakout**: folder containing the RAK815 variant files
* **boards.txt**: file containing the RAK815 board details

Install the RAKWireless RAK815 Board variant
--------------------
It is easy to install the RAkWireless Board variant into the IDE (For ubuntu/other linux users)

* Copy the **boards.txt** into .arduino15/packages/SparkFun/hardware/nRF5/0.2.3/boards.txt
* Copy the **RAK815_nrf52832_Breakout** folder in the variants folder in the path .arduino15/packages/SparkFun/hardware/nRF5/0.2.3
* copy the **libraries** folder content into .arduino15/packages/SparkFun/hardware/nRF5/0.2.3/libraries

For Windows users, just search for the path that has the packages/Sparkfun folder :)

* Next, restart Arduino IDE, you should be able to see an entry for the RAK Wireless RAK815 board. Now you can flash as you normally do
