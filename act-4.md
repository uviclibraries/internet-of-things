---
layout: default
title: 4 - Press a Button to Send a Message
nav_order: 5
parent: Workshop Activities
---

# Press a Button to Send a Message (Facebook, Twitter, Email)

<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Materials Needed**

-   1 Adafruit Feather Huzzah (a type of Arduino board)
-   1 pushbutton
-   1 breadboard
-   1 LED

    <img src="images/act-4/1-breadboard.png" alt="breadboard" style="float:right;width:360px;">

<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Hardware Setup**

1.  Connect parts as in the diagram:
    -   The long leg of the LED should be placed with the long leg in the same row as 13 on the adafruit board and the short leg grounded
    -   The push button should be connected to ground on one side and pin 4 on the adafruit on the other side
2.  Go to [https://bit.ly/2SOyZjC](https://bit.ly/2SOyZjC){:target="_blank"} and copy/paste the code into Arduino
3.  Plug your USB cable into your computer.  Go to **Tools -> Port** and select the port your Feather Huzzah is on. Now compile and upload code and watch the light turn on as you press the button!

    <br>
    **Triggering an Action: Create an Adafruit IO Web Feed CHANGED X4**
    <img src="images/act-4/3-serial.png" alt="serial monitor" style="float:right;width:480px;margin-left:10px;">
    
4.  Click the magnifying glass in the top-right corner to open the serial monitor. The serial (named for serial communication) monitor shows you the values that the Feather is reading from the button. Now press the button and watch the output change!
5.  Exit out of all of your Arduino IDE windows, and shutdown the program
6.  Go to [http://bit.ly/2JSBlMY](http://bit.ly/2JSBlMY){:target="_blank"}. A download of an Arduino program (called a “sketch”) will automatically start. In your Arduino code editor, go to **File > Open** and select the file. Save it
    
    <img src="images/act-4/6-view.png" alt="view" style="float:right;width:360px;margin-left:10px;">
    
    -   Edit the code to add your **IO_Username**, **IO_Key**, along with the **wifi username** and **password**. You can find your IO credentials at [https://io.adafruit.com](https://io.adafruit.com){:target="_blank"} by clicking on the **View AIO Key** button
    -   Now compile and upload code by clicking the **Upload** arrow on the top navigation bar
    -   After the code is loaded, go to in Adafruit IO. Click **Feeds** and open your command feed
    -   Click on the button on your Feather Huzzah, and you’ll see the graph on the Adafruit IO website update. Great job!

<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Connecting to an IFTTT Applet CHANGED**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="images/act-4/7-applet.png" alt="applet" style="float:right;width:480px;">
    
7.  Go to [ifttt.com](https://ifttt.com/){:target="_blank"} and log in or setup an account if you haven’t already. Create a new applet on IFTTT by clicking **My Applets** and then **New Applet**
8.  Click on the big blue **+this** button to open service options, and search for “Adafruit”
    -   Select the **Adafruit** service
    -   Press the **Connect** button. A popup window will appear; press the **AUTHORIZE** button at the bottom
    -   Select **Monitor a feed on Adafruit IO**
    -   Select **command** from the drop down box, select **equal to** from the Relationship drop down, and in the value field, enter **1**. Now press **Create Trigger**
9.  Click on big blue **+that** button to select an output service

    <img src="images/act-4/12-review.png" alt="resistor" style="float:right;width:360px;">

10.  Click on an output device to your liking (e.g. text, twitter, facebook, etc.).  Some ideas:
     -   Spotify - save a track, or add track to playlist
     -   Facebook messenger / sms - receive a text
     -   Email/Gmail
     -   Twitter/facebook - make a status update
     -   The list goes on! Browse around until you find something to your liking
11.  You will be asked if you want to connect to the service. Click **Connect**, and then **Accept**
12.  Click through to customize the message, and click on **Create action**
13.  Click **Finish**. Now every time you press the button, you should receive a text, email, message, or call (depending on how you’ve configured it!)

<img src="images/act-4/12-send.png" alt="resistor" style="width:360px;">

Great job!

[NEXT STEP: Motion Sensor to Send a Message](act-5.html){: .btn .btn-blue }
