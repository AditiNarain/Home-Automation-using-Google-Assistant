# Home-Automation-using-Google-Assistant
## Abstract:
With advance technology developing nowadays we are mostly using smart appliances. So sitting at any place using our voice command as input we can controll the lights, fans or anything.In this IOT project we will be controlling our home appliance using the google assistant according to the message we have done coding and decoding in microcontroller and in google assistant.
## Components:
1.	Nodemcu 8266
2.	Relay
3.	Led( prototype so in place of bulb or fan)


### About Component:
   • Nodemcu 8266:
Node MCU (open-source, Interactive, Programmable, Low cost, Simple, Smart, WI-FI enabled)
1.	The development board equips the ESP-12E module containing ESP8266 chip having Tensilica Xtensa® 32-bit LX106 RISC microprocessor.
2.	 Operates at 80 to 160 MHz adjustable clock frequency 
3.	Supports RTOS.
4.	128kB internal RAM
5.	4MB external flash
6.	802.11b/g/n Wi-Fi transceiver
7.	The operating voltage range of Node MCU is 2.5V to 3.6V (LDO voltage regulator to keep the voltage steady at 3.3V)
8.	20 µA during Sleep Mode and 80 µA operating current.
9.	Operating Temperature: -40ºC to +125 ºC
10.	 CP2102 USB-to-UART converter
11.	 4.5 Mbps communication speed
12.	 Flow Control support

![image](https://user-images.githubusercontent.com/73650233/106279795-fadc7100-6262-11eb-8fa5-3af2a1813ff0.png)

   • Relay :
>  Relays are the advance switch which is controlled by electronic signal using electromagnet and optocouplers (electromechanical relay).

> In electromechanical relay, a flexible movable part connects (make) or disconnect (break) the circuit when it receives the signal.High power devices are easily controlled by low power signal (220V devices are controlled by 5V). Relay handles the ac as well as dc current. The signal receives from on side controls the other side.

![image](https://user-images.githubusercontent.com/73650233/106279739-e6987400-6262-11eb-95c8-6ca14c70bcc9.png)

### Circuit Diagram:

![image](https://user-images.githubusercontent.com/73650233/106279925-39722b80-6263-11eb-829b-29ee72d7e8e0.png)

### Working:
Do all the connection firmly as shown in Circuit Diagram.

Download the blynk app from play store and create a new project and fill all the details like device, connection type. Then it will send a token to that gmail account from which you have signin to the app.

Download the zip file of blink library and do programming by opening : examples -> Blynk -> Boards_WiFi -> ESP8266_Standalone.
Set the ssid password of your hotspot and the code which you got in your gmail by blynk app write in in the auth code.

_Now you module is connected with the blunk app._

Now open the page ifttt.com and signup with the same mail at your blynk app.Then fill what will happen if we say turn on the light or turn off the light(any input which we want to put).
  
In the next part we will select then that and select webhooks(it allows us to send request to blynk app), make a web request.

Next it will ask for the url 188.20….is the server of blynk app it will remain the same, after that we will write the auth code

Fill rest of the detail as 
• Method - put 
• Content type – application json 
• Body – [“0”] according to the desired data you want to send.

All the steps are explain in detail here -> https://github.com/AditiNarain/Home-Automation-using-Google-Assistant/blob/master/Document.md

NOW SAY TURN ON THE LIGHT, LED WILL TURN ON.

If says turn off the light led will go off.
