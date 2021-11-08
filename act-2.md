---
layout: default
title: 3 - Reading Light from a Sensor
nav_order: 3
parent: Workshop Activities
---

# Reading Light from a Sensor

_Adapted from [Adafruit IO: Basics - AnalogIn](https://learn.adafruit.com/adafruit-io-basics-analog-input){:target="_blank"} by Todd Treece_

In this tutorial, you will learn how to detect light with a sensor and relay that info to Adafruit IO. If you or your group have any questions, or get stuck as you work through this in-class exercise, please ask the instructor for assistance.  Have fun!

## List of Materials

-   Adafruit Feather HUZZAH board, breadboard, USB cable
-   Photoresistor or light sensor (below)
-   3 jumper wires
-   1 k-ohm resistor in order for this to work (brown - black - red - gold)

## Instructions

1.  Log into [io.adafruit.com](io.adafruit.com){:target="_blank"} (if you haven’t created an account yet, you can do that now). Along the left sidebar, click **Feeds** and then **Actions -> Create a New Feed**. Name your feed “analog”
    -   Analog in this case refers to the type of input the computer receives -- that is, analog input rather than digital input. Analog input can give you a range of values (0‒1024 in Adafruit IO) whereas digital input can only give you 2 values (0 or 1)
    
2.  Go to Dashboards on the left sidebar and then click **Actions > Create a New Dashboard**. Name the new dashboard “Light Sensor”. Once created, the new dashboard will appear on the page. Click on the name of your new dashboard
3.  For now, the dashboard is blank
    -   Add a block by clicking the **blue plus sign**
    -   Select the **gauge**, and then click on the **analog** checkbox, and click on **Next step**
    -   Change the **Max Value** to **1024**, and click on the blue **Create Block** button
4.  We can also include a line graph to track the changes in light level
    -   Click the **blue plus button** on the top right navigation, and then select the **Line Chart** option
    -   Click on the **analog** checkbox, and click on **Next step**
    -   Under **Show History**, click on the drop down menu and select **8 hours**
    -   Change the **Decimal Places** value to “0”, and click on **Create Block**
5.  Unplug the Feather from your laptop. Now we’ll wire the circuit. Remember that everything on the same row (A-E or F-J) is connected. Connect the circuit as shown on the next page. (There are also written instructions.)
    -   Place the Feather Huzzah on the far left of the bread board as you can see above
    -   The **Red** wire is plugged into **J29** (3V) and **J11**
    -   The **Black** wire is plugged into **J27** (GND) and **J1**
    -   The **Yellow** wire is plugged into **J26** (ADC) and **J6**
    -   The **1K ohm resistor** is plugged into **I6** and **I1**
    -   Lastly the **light sensor** is plugged into **H11** and **H6**
6.  Open the Arduino software. Make sure you have the correct libraries installed (if not, ask an instructor). Go to **File -> Examples -> Adafruit IO Arduino -> adafruitio_08_analogin**. A new sketch should pop up. A sketch is a program or batch of instructions for our Feather HUZZAH
7.  Click on the **config.h** tab near the top. Fill in the 4 lines of info as we did at the start of the workshop
8.  Connect Feather to your laptop and **make sure the right Board and Port settings are selected**. Click the **upload** arrow (the right arrow icon in the top left corner of the window)
9.  Cover the light sensor with a finger and watch the value of the gauge decrease. Then slowly lift your finger further and further away and watch it change!

[NEXT STEP: Make Your Own Weather Station](act-3.html){: .btn .btn-blue }