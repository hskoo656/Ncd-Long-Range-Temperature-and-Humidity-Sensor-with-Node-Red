# Ncd-Long-Range-Temperature-and-Pressure-Sensor-with-Node-Red

We will be using a Temperature/Humidity Sensor for this case, but the steps remain basically the same for any of the product line, so if you have different Ncd Wireless Sensors, feel free to follow along anyway. By the end of this article you should have a solid understanding of how to set up the sensors, configure node-red, and visualize the data on a dashboard like the one pictured here.
![alt tag](https://github.com/rjrajbir/Ncd-Long-range-Temperature-and-Humidity-sensor/blob/master/IoT-Wireless-Temperature-Humidity-600x400.png)
# IoT Long Range Wireless Temperature and Humidity  Sensor
Introducing NCD’s long-range wireless temperature humidity sensor, boasting up to a 28 Mile range using a wireless mesh networking architecture.  Incorporating the Honeywell HIH9130 temperature humidity sensor, transmits highly accurate temperature and humidity samples at user-defined intervals.

The on-board temperature sensor is rated for -25°C to 85°C or -13°F to 185°F and the humidity sensor is rated for 0 to 100% RH.  Powered by just 2 AA batteries and an operational lifetime of 500,000 wireless transmissions, a 10 years battery life can be expected depending on environmental conditions and the data transmission interval.  Optionally, this sensor may be externally powered.

With an open communication protocol this IoT wireless temperature humidity product can be integrated with just about any control system or gateway.  Data can be transmitted to a PC, a Raspberry Pi, to Microsoft Azure® IoT, or Arduino. Sensor parameters and wireless transmission settings can be changed on the go using the open communication protocol providing maximum configurability depending on the intended application.

The long range, price, accuracy, battery life and security features of Long Range Wireless Temperature Humidity Sensor makes it an affordable choice which exceeds the requirements for most of the industrial as well as consumer market applications.

![alt tag](https://github.com/rjrajbir/Ncd-Long-range-Temperature-and-Humidity-sensor/blob/master/Zigmo_1-600x400.png)
# ZigBee Coordinator Long Range Wireless Mesh Modem with USB Interface
- **ZigBee Wireless Communication**
Mesh Networking is simply the hottest wireless technology of our time. Period. It’s fast, it’s very easy to use, highly reliable, and self healing. Three components are required for the ZigBee Mesh Network, the Coordinator (C), the Router (R) and the Endpoint (E). Your computer can speak to a ZigBee Mesh Network using a Coordinator. Think of the Coordinator as the interface to a ZigBee Mesh Network. NCD Coordinators are equipped with a USB Interface. This ZigBee Coordinator mounts as a Serial Port on your computer, and you will develop software that sends Serial commands at 115.2K Baud. The primary job of a router is to bridge the wireless gap between your computer (the Coordinator) and the device (Endpoint). If the Coordinator cannot speak to the Endpoint device because it is out of range, a Router can be used to bridge the two devices together. Endpoints are simply devices. With regard to NCD products, Endpoints can be relay controllers, data collection devices, PWM devices, and much more.

- **USB ZigBee Coordinator**
Your computer can speaks to a ZB ZigBee Network using a Coordinator.  Think of the Coordinator as the interface to a ZB ZigBee Network.  NCD ZigBee Coordinators are equipped with a USB Interface.  USB Coordinators mount as a Serial Port on your computer, and you will develop software that sends Serial commands at 115.2K Baud.  Only ONE Coordinator should be installed within a wireless ZB ZigBee Network.  Two types of Coordinators are available.  AT and API.  Normally, AT coordinators are used.  AT coordinators use Terminal-like AT commands to speak to a ZB ZigBee Network.  They are easier to use than an API coordinator.  An API coordinator uses a string of carefully chosen bytes and checksums to communicate data to a ZigBee networking.  API coordinators are harder to use, but can communicate and switch between devices much faster.  This page will introduce you to AT coordinators.  You can choose between AT and API firmware at checkout.
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/ESP32_1.png)

# Steps to send data to labview Temperature and Humidity platform using IoT Long Range Wireless Temperature and Humidity Sensor and ZigBee Coordinator Long Range Wireless Mesh Modem with USB Interface-

Industrial-Wireless-IoT-Temperature-Humidity-Sensor
Wireless Temperature Humidity Sensor Long range wireless IoT temperature humidity sensor can be found over here https://store.ncd.io/product/industrial-long-range-wireless-temperature-humidity-sensor/

https://ncd.io/long-range-wireless-temperature-humidity-sensor/ Labview Driver for ncd.io wireless temperature humidity sensor

this Labview software will work with ncd.io wireless temperature humidity sesnor only

To use this Labview Utility You will need a Wireless to USB router, whihc can be found over here https://store.ncd.io/product/900hp-s3b-long-range-wireless-mesh-modem-with-usb-interface/

To use this UI, you will need to install following drivers Install run time engine from here 64bit http://www.ni.com/download/labview-run-time-engine-2017/6821/en/

32 bit http://www.ni.com/download/labview-run-time-engine-2017/6822/en/

Install NI Visa Driver -- http://www.ni.com/download/ni-visa-run-time-engine/6647/en/

Install Labview Run time serial driver http://www.ni.com/download/ni-serial-17.0/6613/en/ http://www.ni.com/download/labview-run-time-engine-2017-sp1/7191/en/

Getting strated guide for this product can be found over here https://ncd.io/long-range-iot-wireless-temperature-humidity-sensor-getting-started/

complete product manual for this product can be found over here https://ncd.io/long-range-iot-wireless-temperature-humidity-sensor-product-manual/


## Serial monitor output.
![alt tag](https://github.com/rjrajbir/Ncd-Long-range-Temperature-and-Humidity-sensor/blob/master/comoutput.PNG)

## Making the Ubidot work:
- **Create the account on [Ubidot](https://ubidots.com/).**
- **Go to my profile and note down the token key which is a unique key for every account and paste it to your ESP32 code before uploading.**
- **Add a new device to your ubidot dashboard name esp32.**
  
![alt tag](https://github.com/mjScientech/Esp32-And-SHT30/blob/master/device234.JPG)

                       Click on devices and select devices in ubidot.

![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/Device.JPG)

     Now you should see the published data in your Ubidots account, inside the device called "ESP32".

- **Inside device create new variable name sensor in which your temperature reading will be shown.**
![alt tag](https://github.com/mjScientech/ESP32-AND-SI7021/blob/master/variable.JPG)
                  
         
![alt tag](https://github.com/mjScientech/https-github.com-mjScientech-ESP32-AND-SI7021/blob/master/variableout.JPG)

     
- **Create dashboard in ubidots**
![alt tag](https://github.com/mjScientech/https-github.com-mjScientech-ESP32-AND-SI7021/blob/master/dashboard1.JPG)
       
          Go to data select dashboard and inside dashboard create different widgets and add new widget 
          to your dashboard screen.
# OUTPUT
- **Now as the temperature and humidity increases and decreases new data available inside the various variable.**
![alt tag](https://github.com/rjrajbir/Ncd-Long-range-Temperature-and-Humidity-sensor/blob/master/temp_and_humidity.PNG)

