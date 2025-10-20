---
layout: default
title: 5 - Motion Sensor Message - BROKEN
nav_order: 6
parent: Workshop Activities
---

# Motion Sensor to Send a Message (Facebook, Twitter, Email)

<br>**Materials Needed**

-   1 Adafruit Feather Huzzah (a type of Arduino board)
-   1 PIR motion detector <br><img src="images/act-5/1-motion.png" alt="resistor" style="float:center;width:120px;">
-   1 breadboard
-   1 LED light
-   2 red  wires, 2 black wires, 1 other coloured wire
-   1 10K ohm resistor (brown - black - orange - gold) <br><img src="images/act-5/1-res.png" alt="resistor" style="float:center;width:120px;">

**Please Note:** The DSC also has smaller PIR motion detectors than the one pictured here. These need to be connected without the 10K ohm resistor tying the OUT pin to ground.
    
<br>**Hardware Setup**

1.  Connect parts as in the diagram (Note: double check the pins on your motion sensor, as they may differ from the one used in the example here):
    - Place the Feather Huzzah on the far left of the bread board as you can see below
    - Place the PIR sensor somewhere to the right of the Feather
    - Connect the GND pins of the Feather and the sensor together
    - Connect the VCC pin of the sensor (VDD on the smaller ones) to the USB (5V) pin of the Feather
    - Connect the OUT pin of the sensor to IO pin 4 (SDA) of the Feather
    - Tie the OUT pin of the sensor to GND using the 10k ohm resistor as a "pull-down" resistor
    - Place the LED with the long pin (anode) connected to IO pin 13 of the Feather and the short pin (cathode) connected to GND
    
    <!---
    -   The **PIR motion sensor** should be connected facing out in **J1** to **J3** on the breadboard
    -   The long leg of the **LED** should be placed in the same row as **pin 13** on the adafruit board and the other leg into a **“-”** hole on the edge
    -   A **black wire** should connect to the hole next to the **GND** pin, and then to a **“-”** on the edge of the board as shown above
    -   A second **black wire** should connect a hole in line with the outside prong of the **PIR** (labeled **GND** on the back of the **PIR**), and the other end in a **“-”** hole on the edge of the board
    -   A **red wire** should connect to the hole next to the **USB** pin, and then to a **“+”** pin on the edge of the board as shown above
    -   A second **red wire** should connect a hold in line with the inside prong of the **PIR** (labeled **OUT** on the back of the **PIR**), and the other end in a **“+”** hole on the edge of the board
    -   A **wire** (any colour, but yellow above) should connect to the hole next to the **SCL** pin, and the other end should connect a hole in line with the middle prong of the **PIR** (labeled **VCC**)
    -   A **10K ohm resistor** should be connected to a hole in line with the **SCL** pin, and the other end in a **“-”** hole on the edge of the board
    -->
    
    <img src="images/act-5/1-diagram.png" alt="resistor" style="width:720px;">
    
    <img src="images/act-5/1-breadboard.png" alt="resistor" style="width:720px;">
    
2.  Download & open the following file in your Arduino editor, then save it: [https://bit.ly/2JPqHTO](https://bit.ly/2JPqHTO){:target="_blank"}
3.  Plug your USB cable into your computer.  Go to **Tools -> Port** and select the port your Feather Huzzah is on
    -   Now compile and upload code, and wave your hand in front of the PIR motion sensor and watch the LED light up!
    -   **Note:** you may need to adjust the orange sensitivity & delay dials with a phillips screwdriver

<br>**Triggering an Action Online: Create an Adafruit IO Web Feed**

4.  Exit out of all of your Arduino IDE windows, and shutdown the program
5.  Download & open the following new file in your Arduino code editor, and then save it: [https://bit.ly/2JSBlMY](https://bit.ly/2JSBlMY){:target="_blank"}
    -   Edit the code to add your **IO_Username**, **IO_Key**, along with the **wifi username** and **password**. You can find your Adafruit IO credentials at [https://io.adafruit.com](https://io.adafruit.com){:target="_blank"} by clicking on the yellow **My Key** button in the top menu bar
    -   Edit the code so that the input receive is from the motion sensor.  Hint: You may need to change the input pin in the default code.
    -   Now compile and upload code by clicking the **Upload** arrow on the top navigation bar
    -   After the code is loaded, go into Adafruit IO. Click **Feeds** and then **view all** and open your command feed
    -   Activate the motion sensor, and you’ll see the graph on the Adafruit IO website update. Great job!

<br>**Connecting to an IFTTT Applet**<br>
<img src="images/act-5/5-applet.png" alt="resistor" style="float:right;width:480px;margin-left:10px;margin-top:10px;">

6.  Go to [https://ifttt.com/](https://ifttt.com/){:target="_blank"} and log in or setup an account if you haven’t already. Create a new applet on IFTTT by clicking **My Applets** & then the **Get more** button
7.  In the search bar (underneath the **Explore** text) search for “Adafruit”
    -   Select the **Adafruit** service
    -   Click the **Create** option
    -   Click the **Add** button next to the "If This" text
    -   Search for Adafruit again and select it
    -   Select **Monitor a feed on Adafruit IO**
    -   Select the **command** feed from the "Feed" dropdown box, select **equal to** from the "Relationship" dropdown box, and in the value field enter "1". Now press **Create Trigger**
8.  Click on the **Add** button next to the "Then That" text to select an output service
    -   Search for and click on email (or another output device to your liking: email, twitter, facebook, etc.)
    -   You will be asked if you want to connect to the service. Click **Connect**, and then **Accept**
    -   Click through to customize the message if you want to, and click on **Create action**
    -   **A warning on IFTTT states that the applet can take up to an hour to apply. It may not work for workshop attendees right away**
9.  Click Finish. Now every time you activate the motion sensor, you should receive a text, email, message, or call (depending on how you’ve configured it!)

<br>[NEXT STEP: Weasley Whereabout Clock](act-6.html){: .btn .btn-blue }
