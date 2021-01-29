# HEY GOOGLE TURN ON THE LIGHTS ![image](https://user-images.githubusercontent.com/73650233/106239700-0ca12280-6229-11eb-9614-6ba07d96c2b1.png)

This project deals with the controlling the electronic or electrical appliances using google assistant.
#### Hey Google Turn on the Led

### This can be done in two steps:
 1.	Connecting the module with blynk app.
 2.	Connect google assistant and blynk app via third party IFTTT. 

## 1.	Connecting the module with blynk app.
• 	Make the circuit connection ; connect led to the D2 pin of Node MCU (esp8266).

• 	Download the blynk app from play store.

1.	Create new project.
2.	Give name to the project.
3.	Choose the device as NodeMCU.
4.	Set connection type as Wi-Fi.
5.	Create the new project. 
6.	Then the Token was send on the specified email address.


![image](https://user-images.githubusercontent.com/73650233/106239838-47a35600-6229-11eb-986c-6b82fbb7ad63.png)                  ![image](https://user-images.githubusercontent.com/73650233/106239855-4e31cd80-6229-11eb-83a5-aeca5e87ea64.png)

7.	Now select the button  by clicking on  ![image](https://user-images.githubusercontent.com/73650233/106239946-71f51380-6229-11eb-9fb1-484959b05e4f.png)  and place it on
 the screen.
8.	Click on the button, name it as button then click on yhe button and select the pin as digital Pin and choose D2 .

 ![image](https://user-images.githubusercontent.com/73650233/106240037-9a7d0d80-6229-11eb-928d-dad71c82fddc.png)                          ![image](https://user-images.githubusercontent.com/73650233/106240099-aff23780-6229-11eb-8fa7-a7f92941be4e.png)

•	Now open the Arduino IDE: Goto Tools ->  Board -> Board Manager -> search esp8266 and install it. Then select the board. 

![image](https://user-images.githubusercontent.com/73650233/106240205-df08a900-6229-11eb-9bad-8ff2e2f149e6.png)

•	Download the blynk library from its github page. Unzip the folder where all the arduino’s library are stored.Paste the libraries in library folder and tools in the toolfolder   of IDE.

 ![image](https://user-images.githubusercontent.com/73650233/106240296-0e1f1a80-622a-11eb-958f-78dfb632c49b.png)

 ![image](https://user-images.githubusercontent.com/73650233/106240364-2858f880-622a-11eb-8b26-9282c6a0027e.png)

•	Now select  examples -> Blynk -> Boards_WiFi -> ESP8266_Standalone 

![image](https://user-images.githubusercontent.com/73650233/106240392-3575e780-622a-11eb-8d5e-651fca57eeb8.png)

•	Now Copy and paste the auth code which is send on the Gmail, from blynk app. 

  _code char auth [] =‘‘----’’._
  
•	Set the ssid [] as your hostpot name and pass [] as your ssid password.

![image](https://user-images.githubusercontent.com/73650233/106240492-5d654b00-622a-11eb-8234-7c3f0adf6428.png)

•	Compile the program and do uploading (Check the correct port being is selected).

## 2.	 Connect google assistant and blynk app via third party IFTTT. ![image](https://user-images.githubusercontent.com/73650233/106240599-8ab1f900-622a-11eb-82c3-ae5cc584cd17.png)

1.	Open the page ifttt.com and signup with the same mail at your blynk app.
2.	Then create new applet in the my applet.
3.	Then page will come if this then that, select _if this_.
4.	After that search for the google assistant, then choose simple phrase option.
5.	Then fill the details accordingly and create trigger.

*![image](https://user-images.githubusercontent.com/73650233/106240649-a61d0400-622a-11eb-8b54-a86e3513548d.png)*
 
6.	Now in the next part we will select _then that_  and select webhooks(it allows us to send request to blynk app), make a web request.
7.	In the next page it will ask for the url 188.20….is the server of blynk app it will remain the same, after that we will write the auth code which came up in the mail message      by blynk app server.https://188.166.206.43/xxxxxxxxxxx/update/D4, then most importantly we have used D2 pin number for our led and corresponding to D2 pin we are having          GPIO04 that’s why we have written D4. If we were using D4 pin then we will write D2 over there as it is corresponding to GPIO2.
     So pin number will be witten the number of gpio pin because we are using arduino ide for programming ESP.

 ![image](https://user-images.githubusercontent.com/73650233/106240702-bc2ac480-622a-11eb-9efc-621a80d87c18.png)

8.	Now fill rest of the detail as shown in the picture below
    • Method - put
    • Content type – application json
    • Body – [“0”] according to the desired data you want to send.

![image](https://user-images.githubusercontent.com/73650233/106240809-eda39000-622a-11eb-9f2a-de5a4f0b5070.png)


All the step done same way creates another applet for turn on the light google.
## NOW SAY TURN ON THE LIGHT, LED WILL TURN ON.
