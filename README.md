# SmartRC-CC1101-Driver-Lib_V2.5.1 ----For STM32-Bluepill 
 
Now testting

---------------------------------------------
Foreword:
---------------------------------------------
First of all, thanks to Elechouse ,LSatan
that I can make the modified library accessible to everyone.

Link: https://github.com/LSatan/CC1101-Debug-Service-Tool
Link: https://github.com/LSatan/Simu_Remote_CC1101
Link: http://www.elechouse.com/elechouse/

for ESP32,ESp8266,UNO.....Link here:https://github.com/LSatan/SmartRC-CC1101-Driver-Lib

---------------------------------------------
Containing examples:
---------------------------------------------
1.Elechouse CC1101:
-
Description: CC1101 Internal send / receive examples. Supported modulations 2-FSK, GFSK, ASK/OOK, 4-FSK, MSK.

---------------------------------------------
Instructions / Description:
---------------------------------------------

The most important functions at a glance:

ELECHOUSE_cc1101.Init();		//Initialize the cc1101. Must be set first!

ELECHOUSE_cc1101.setPA(PA);		//Set transmission power.

ELECHOUSE_cc1101.setMHZ(MHZ);		//Set the basic frequency.

ELECHOUSE_cc1101.SetTx();		//Set transmit on. 

ELECHOUSE_cc1101.SetTx(MHZ);		//Sets transmit on and changes the frequency.

ELECHOUSE_cc1101.SetRX();		//Set receive on.

ELECHOUSE_cc1101.SetRx(MHZ);		//Sets receive on and changes the frequency.

ELECHOUSE_cc1101.setRxBW(RXBW);		//Set Receive filter bandwidth		

ELECHOUSE_cc1101.setGDO(GDO0, GDO2); 	//Put the Gdo pins. For libraries that address the gdo pins directly.

ELECHOUSE_cc1101.setSpiPin(SCK, MISO, MOSI, CSN); //custom SPI pins. Set your own Spi Pins.Or to switch between multiple cc1101. Must be set before init and before changing the cc1101.

ELECHOUSE_cc1101.setChannel(chnl); 	//Set Channel from 0 to 255. default = 0(basic frequency).

ELECHOUSE_cc1101.setClb(fband, cal1, cal2); //Optionally enter Offset Callibration. Requirements: Sketch Calibrate_frequency.ino below [CC1101-Debug-Service-Tool](https://github.com/LSatan/CC1101-Debug-Service-Tool/tree/master/Calibrate_frequency).A SDR receiver and SDR software.


