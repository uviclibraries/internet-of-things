---
layout: default
title: 2 - Setup
nav_order: 2
parent: Workshop Activities
---

<!---   <img src="images/act-1/logo.png" alt="" style="float:right;width:180px;">   -->

# Setting Up The Feather Huzzah

Before we start working on the IOT projects, let’s install all the necessary software and drivers on your laptop. Many people find it helpful to also use the digital version of this document to click on URL’s: https://richmccue.github.io/internet-of-things/act-1.html

## Configuring Arduino IDE
1.  Go to [goo.gl/eEXD4e](goo.gl/eEXD4e){:target="_blank"} and install the appropriate driver for your laptop
2.  If you haven't already installed the Arduino IDE, go to [http://bit.ly/2LIKN2A](http://bit.ly/2LIKN2A){:target="_blank"}
    -   Download and install the software. **Note:** The software is in a zip file, so it may take a few steps before you are asked for your password during the install process. If you haven’t entered your password, you’re not done yet
    -   **REBOOT your computer now!** This is Very Important to do!
3.  In the Arduino IDE you just installed go to **Sketch menu -> Include Library -> Manage Libraries**
    -   Now search for "Adafruit IO Arduino" and click **Install**
    -   Search for "Adafruit MQTT" and click **Install**
    -   Search for "ArduinoHttpClient" and click **Install**
4.  Open the following URL in your web browser: [https://bit.ly/1QeAVwh](https://bit.ly/1QeAVwh){:target="_blank"}
    -   Copy the full URL of the web page as you’ll need it in the next step (the full URL is: http://arduino.esp8266.com/stable/package_esp8266com_index.json)
    -   In your Arduino IDE, go to the **File** menu **-> Preferences** (on a Mac **Arduino** menu **-> Preferences**). A window will pop up. Under the **Settings** tab, go to **Additional Board Manager URLs** and copy/paste the above link in the field beside it
    -   Click **OK**
5.  Go to **Tools -> Board -> Board Manager**. In the pop-up window, search for the esp8266 package. Click on the result and an install button will show up in the bottom right corner. Click it
6.  Double-check you have the right settings under **Tools**
    -   Select: **Tools -> Board -> Adafruit Feather HUZZAH ESP8266**
    -   Select: **Tools -> CPU Frequency -> 80 MHz**
    -   Select: **Tools -> Upload Speed -> 115200 baud**
7.  Connect the Feather Huzzah to your laptop. Go to **Tools -> Port ->** (select the right COM port)
    -   On a Mac, the port is labelled "SLAB_USBtoUART"
    -   (Note: you may have to reselect port when you unplug and replug the cable into your computer)
8.  In your web browser, go to [io.adafruit.com](io.adafruit.com){:target="_blank"} and create an account
    -   After you’ve logged in, look at the left menu and click on **AIO Key**
    -   Copy the **Active Key** to your clipboard as you’ll need this in step #10 of the setup (your key should be in this format “2cf0197e930f406eb1f9374be6c87cf4”, but different of course)
9.  In Arduino IDE, go to **File -> Examples -> Adafruit IO Arduino -> adafruitio_00_publish** (this is near the bottom of the menu). A window should pop up with some code in it
10.  Click on the **config.h** tab. Fill in the first four lines of code with the following required information:
11.  Replace the highlighted sections with the following, taking care to **keep the quotation marks**:

     ```
     #define IO_USERNAME: [Your Adafruit IO username]
     #define IO_KEY: [Your Adafruit IO key]
     #define WIFI_SSID: “DSC iPhone”
     #define WIFI_PASS: “dscdsc123”
     ```

**Please Note:** You will have to do this for every new project sketch you open in Arduino

**Extra:** Click **Upload** (top-left corner of the window). When it’s done uploading, wait a few seconds and then click on the **Serial Monitor** (magnifying glass in top-right corner). In the bottom right corner, make sure you select **115200 baud**. You should see the Feather printing data to the screen!

**Extra Extra:** If you want to see the same information through the Adafruit IO interface, go to [bit.ly/2RAo4c0](bit.ly/2RAo4c0){:target="_blank"} and follow the instructions there.

[NEXT STEP: Reading Light from a Sensor](act-2.html){: .btn .btn-blue }
