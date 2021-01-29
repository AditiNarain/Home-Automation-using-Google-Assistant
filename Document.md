HEY GOOGLE TURN ON THE LIGHTS
This project deals with the controlling the electronic or electrical appliances with the appliance using google assistant.
This can be done in three steps:
1.	Connecting the module with blynk app.
2.	Connect google assistant and blynk app via third party IFTTT. 

1.	Connecting the module with blynk app.
•	Make the circuit connection; connect led to the D2 pin of Node MCU (esp8266).
•	Download the blynk app from play store.
1.	Create new project.
2.	Give name to the project.
3.	Choose the device as NodeMCU.
4.	Set connection type as Wi-Fi.
5.	Create the new project. 
6.	Then the Token was send on the specified email address.










7.	Now select the button  by clicking on             and place it on
 the screen.
8.	Click on the button name that button, select the pin as digital
Pin and choose D2 .











•	Now open the Arduino IDE: Goto Tools      Board       Board Manager       search esp8688 and install it. Then select the board. 
•	Download the blynk library from its github page. Unzip the folder where all the arduino’s  library are stored.Paste the libraries in library folder and tools in the toolfolder of IDE.

 



•	Now select  examples       Blynk        Boards_WiFi      ESP8266_Standalone   
•	Now Copy and paste the auth code send on the Gmail, to the  blynk code
 char auth [] =‘‘----’’.
•	Set the ssid [] as your hostpot name and pass [] as your ssid password.










•	Compile the program and do uploading (Check the correct port being is selected).

2.	 Connect google assistant and blynk app via third party IFTTT.
1.	Open the page ifttt.com and signup with the same mail at your blynk app.
2.	Then create new applet in the my applet.
3.	Then page will come if this then that, select if this.
4.	After that search for the google assistant, then choose simple phrase option.
5.	Then fill the details accordingly and create trigger.

 
6.	Now in the next part we will select then that  and select webhooks(allows us to send request to blynk app),make a web request.
7.	In the next page it will ask for the url 188.20….is the server of blynk app it will remain the same after that we will write the auth code which came up in the mail message by blynk app server.
https://188.166.206.43/xxxxxxxxxxx/update/D4, then Most importantly we have used D2 pin number for our led and Corresponding to D2 pin we are having GPIO04 that’s why we have written D4.

If we were using D4 pin then we will
write D2 over there as it is
corresponding to GPIO2.
8.	Now fill rest of the detail as shown 
In the picture below
Method - put
Content type – application json
Body – [“0”] according to yhe desired
Data you want to send.














All the step done same way creates another applet for turn on the light google.
NOW SAY TURN ON THE LIGHT, LED WILL TURN ON.
