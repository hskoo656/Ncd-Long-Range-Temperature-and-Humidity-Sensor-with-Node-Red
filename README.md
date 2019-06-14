# Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red

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


## Setting up Node-Red.
The sensor and Zigmo/Router come pre-programmed and work out of the box. In this section we will setup a sensor and Zigmo link and start receiving data on our PC.
**Resources Required**
- [IoT Long Range Wireless Temperature Humidity Sensor](https://store.ncd.io/product/industrial-long-range-wireless-temperature-humidity-sensor/) with power source Battery Or External DC.
- [Zigmo/Router for PC](https://store.ncd.io/product/900hp-s3b-long-range-wireless-mesh-modem-with-usb-interface/)
- PC/Laptop with an OS installed or Any IoT Embedded Device
Now that you have sensors running, we need a way to do something useful with that data. In the past your options tended to be either A) Hire a developer, or B) Use some proprietary software that probably costs additional money on top of the hardware you’ve already purchased. Our dislike of these options is largely what led us to start building for Node-RED. If you’ve never used it before, I have great news! It’s free, open source, and simple. It works on Windows, Linux and Mac, and is constantly being developed and improved. Seeing no need to reinvent the wheel, I’ll point you to the excellent documentation already available for [Installing Node-RED](https://nodered.org/docs/getting-started/installation). Once that’s done, you’ll need to enter your command line, or Power Shell for Windows users, navigate to the directory Node-RED is installed in, and type “npm i ncd-red-wireless node-red-dashboard“. This will install the nodes required to receive data from your wireless sensors and you can start Node-RED once this is done.
##Setting up the nodes
![alt tag](https://github.com/rjrajbir/Ncd-Long-Range-Temperature-and-Pressure-Sensor-with-Node-Red/blob/master/wnode.JPG)

Now, build the flow in the image above to proceed… Just kidding! And don’t worry… this isn’t as bad as it looks. The packages you installed provide a few different pieces of functionality, as detailed here, but you can learn more about each by adding one of the nodes it provides to a flow and viewing its info tab. Assuming at this point you’ve started up Node-RED, you should be able to open a browser and navigate to http://localhost:1880, this will open up the flow builder that is the heart of the Node-RED experience. At this point you’ll be viewing a large blank flow with a long list of nodes on the left hand side, this sidebar is called the palette. At the top of the palette is a search box, if you type “ncd”, the nodes available will be filtered down to those we provided through the ncd-red-wireless package. Go ahead and drag a Wireless Gateway node over to your flow canvas to get started.
##Finding your wireless sensors
Once you’ve added the node you’ll be able to view the info tab, which contains information about the node’s functionality, this tab is well populated for most node-red packages I have used, and contains valuable information, many times you will not need to view any other documentation outside of the info tab, so keep it in mind while you are building your flows if you have a question about how a node works. The next thing we need to do is configure the node, when you first add it you’ll notice that there is a small triangle on the top right corner next to a blue dot, the triangle indicates that the node needs additional configuration, the blue dot indicates that the node has not yet been deployed as part of the flow.

#NODE-RED DASHBOARD OUTPUT
- **Now as the temperature and humidity increases and decreases new data available inside the various variable.**
![alt tag](https://github.com/rjrajbir/Ncd-Long-Range-Temperature-and-Pressure-Sensor-with-Node-Red/blob/master/Dashboard.JPG)

