## Indrotuction ##
A basic library that permits controlling an arduino through the firmata protocol. The current version is developed and tested with the arduino ver0021 software.

The purpose of this library is to make it easy to LabVIEW developers to connect their code to the real world using the arduino hardware.

My goal is to use this subvi of library through labview to make arduino as a cheap DAQ device. If anyone also interested in contributing towards this direction let me know.


## developer guide ##
### 1. Setup Environment ###
-download the arduino software form official webiste (http://arduino.cc/en/Main/Software)

-unzip arduino-0022.zip file and copy to local drive C:\arduino-0022

-download the labviewduino file from google project code website
(http://code.google.com/p/labviewduino/downloads/list)

-unzip labviewduino-v1.0.0.127.zip and copy to local drive C:\labviewduino-v1.0.0.127

-connect the usb cable from board to desktop PC

-install FTDI driver to desktop PC ( please ignore if you are using Arduino UNO board)installer file available at C:\arduino-0022\drivers\FTDI USB Drivers

-check the serial port status of Device Manager>>Ports(COM & LPT) >>USB Serial Port (COM2)

-default baud rate setting is 57600 N-8-1.


### 2. Load sketch to Arduino board ###

-startup the program from C:\arduino-0022\arduino.exe

-see welcome logo at screen, it shows the latest version 0022

-select the board type.

>> Tools>>Board>>Arduino Duemilanove (for my case)

-select the COM port.

>>Tools>>Serial Port>>COM2 (for my case)

-load the firmata sketch file

>>File >>Open...>>C:\labviewduino-v1.0.0.127\sketch\_firmata\_analog\_input\sketch\_firmata\_analog\_input.pde

-verify the sketch. see the "Done compiling" message

>>Sketch>>Verify / Compile

-upload the sketch to arduino.see the "Done uploading" message

>>File>>Upload to I/O Board

### 3. Run LabVIEW Program ###

-open C:\labviewduino-v1.0.0.127\Firmata-example-AI.vi

-check the VISA resource setting for your own setting (ie:COM2)

-run the labview vi

-see the measurement result from arduino , output as the voltage array (E0 for Pin0 , E1 for Pin1....)


## Screen Shots ##
https://docs.google.com/leaf?id=0B7pVN2q5KmjwNjdmMWI2NDEtYWFiNi00OTZiLWJmNjAtZWVmZWVkMTZjODNi&hl=zh_TW