# Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red

We are able to be using a temperature/humidity sensor for this example, but the steps stay the equal for any of the **ncd** product, so if you have exclusive ncd wireless sensors, experience free to observe alongside besides. By means of the stop of this text, you need to have a stable understanding of how to set up the sensors, configure node-crimson, and spot the facts on a dashboard like the one pictured right here.

![alt tag](https://github.com/rjrajbir/Ncd-Long-range-Temperature-and-Humidity-sensor/blob/master/IoT-Wireless-Temperature-Humidity-600x400.png)
# IoT Long Range Wireless Temperature and Humidity  Sensor
Introducing NCD’s long-range wireless temperature humidity sensor, boasting up to a 28 Mile range using a wireless mesh networking architecture.  Incorporating the Honeywell HIH9130 temperature humidity sensor, transmits highly accurate temperature and humidity samples at user-defined intervals.

The on-board temperature sensor is rated for -25°C to 85°C or -13°F to 185°F and the humidity sensor is rated for 0 to 100% RH. It can be powered by just 2 AA batteries and an operational lifetime of 500,000 wireless transmissions.Battery life can be extended upto 10 years depending on environmental conditions and the data transmission interval.  Optionally, this sensor may be externally powered.

With an open communication protocol this IoT wireless temperature humidity product can be integrated with just about any control system or gateway.  Data can be transmitted to a PC, a Raspberry Pi, to Microsoft Azure® IoT, or Arduino. Sensor parameters and wireless transmission settings can be changed on the go using the open communication protocol providing maximum configurability depending on the intended application.

The long range, price, accuracy, battery life and security features of Long Range Wireless Temperature Humidity Sensor makes it an affordable choice which exceeds the requirements for most of the industrial as well as consumer market applications.

![alt tag](https://github.com/rjrajbir/Ncd-Long-range-Temperature-and-Humidity-sensor/blob/master/Zigmo_1-600x400.png)
# Long Range Wireless Mesh Modem with USB Interface
- **Zigmo Wireless Communication**
Mesh Networking is simply the hottest wireless technology of our time. Period. It’s fast, it’s very easy to use, highly reliable, and self healing. Three components are required for the ZigBee Mesh Network, the Coordinator (C), the Router (R) and the Endpoint (E). Your computer can speak to a ZigBee Mesh Network using a Coordinator. Think of the Coordinator as the interface to a Wireless Mesh Network. NCD Coordinators are equipped with a USB Interface. This Zigmo mounts as a Serial Port on your computer, and you will develop software that sends Serial commands at 115.2K Baud. The primary job of a router is to bridge the wireless gap between your computer (the Coordinator) and the device (Endpoint). If the Coordinator cannot speak to the Endpoint device because it is out of range, a Router can be used to bridge the two devices together. Endpoints are simply devices. With regard to NCD products, Endpoints can be relay controllers, data collection devices, PWM devices, and much more.

# Setting up Node-Red.
The sensor and Zigmo/Router come pre-programmed and work out of the box. In this section we will setup a sensor and Zigmo link and start receiving data on our PC.

**Resources Required**
- [IoT Long Range Wireless Temperature Humidity Sensor](https://store.ncd.io/product/industrial-long-range-wireless-temperature-humidity-sensor/) with power source Battery Or External DC.
- [Zigmo/Router for PC](https://store.ncd.io/product/900hp-s3b-long-range-wireless-mesh-modem-with-usb-interface/)
- PC/Laptop with an OS installed or Any IoT Embedded Device
# Steps to install NODE-RED
Now that you have sensors running, we need a way to do something useful with that data.
- First of all you'll have to install [Node-RED](https://nodered.org/docs/getting-started/installation). 
- Once that’s done, you’ll need to enter your command line, or Power Shell for Windows users, navigate to the directory Node-RED is installed in.
- Now type **“npm i ncd-red-wireless node-red-dashboard“**. This will install the nodes required to receive data from your wireless sensors and you can start Node-RED once this is done.
- To start node server write **node-red** in the command prompt or terminal and press enter.

# Setting up the nodes
![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/final%20flow.JPG)

Now, start building the flow in the image above to proceed… Just kidding! And don’t worry… I have given all the steps to build it. The packages you installed provide a few different pieces of functionality, as detailed here, but you can learn more about each by adding one of the nodes it provides to a flow and viewing its info tab. Assuming at this point you’ve started up Node-RED, you should be able to open a browser and navigate to http://localhost:1880, this will open up the flow builder that is the heart of the Node-RED experience.

**Steps to build the flow**

- **At this point you’ll be viewing a large blank flow with a long list of nodes on the left hand side, this sidebar is called the palette.**

![alt tag](https://github.com/rjrajbir/Ncd-Long-Range-Temperature-and-Pressure-Sensor-with-Node-Red/blob/master/blankpage.JPG)

- **Go ahead and drag a Wireless Gateway node over to your flow canvas to get started.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gateway%20step1.JPG)

- **ncd-red-wireless**
Provides the nodes that manage the serial connection, parse incoming sensor data, filter it by specific parameters, and allow you to configure the wireless sensors.

# Finding your wireless sensors
Once you’ve added the node you’ll be able to view the info tab, which contains information about the node’s functionality, this tab is well populated for most node-red packages and contains valuable information, many times you will not need to view any other documentation outside of the info tab, so keep it in mind while you are building your flows if you have a question about how a node works. The next thing we need to do is configure the node, when you first add it you’ll notice that there is a small triangle on the top right corner next to a blue dot, the triangle indicates that the node needs additional configuration, the blue dot indicates that the node has not yet been deployed as part of the flow.

- **Double click on the node to open up the configuration options.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gateway%20step2.JPG)

- **Click on the pencil icon next to the Serial Device field to configure your USB router, this will open a second configuration panel that only has a few options.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gateway%20step3.JPG)

- **Click on the magnifying glass next to the Serial Port field and select the port that corresponds with your router, then click the “Add” button on top. The Serial Device field will now be populated based on that selection, and you can click “Done”, you now have direct access to your wireless sensors! To view the data coming in.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gateway%20step4.JPG)

- **Now go back to your palette and type “debug” into the search field at the top, grab one of these nodes and drag it to the right of your Wireless Gateway**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/debug%20step1.JPG)

- **Double click on it and change “msg.” to “complete msg object” click done**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/debug%20step2.JPG)

- **Now draw a line between the two nodes, and click “Deploy” on the top right of the window..**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/deploy.JPG)

# Working with the data
Now out of your wireless sensors data is gathered and it is output to the “debug” tab, this "debug tab" is placed within the right sidebar subsequent to the information tab. To see the information are available in to hit the reset button. In node-red records is surpassed among nodes in a json packet. When the msg object comes into the debug tab you may make bigger it to view the overall list of information that comes with it. This is extraordinarily useful in case you need to quickly see which sensors are checking in. The other issue this node gives is a easy way to interchange your router to the network identity that devices in configuration mode document on, simply hit the button on the left of the node and the tool will switch to the configuration network, hit it once more to return it to listening mode. Once we get the wi-fi tool nodes set up, they may be set to routinely configure a sensor whilst it enters configuration mode, so it’s always available to maintain such a gateway nodes present at the flow for speedy configuring a device.

![alt tag](https://github.com/rjrajbir/Ncd-Long-Range-Temperature-and-Pressure-Sensor-with-Node-Red/blob/master/GatewayJson.png)

# Adding the wireless sensors
Now we need to separate wireless sensor statistics regionally so that we are able to show it, we could use a transfer node to cut up out the messages from the gateway based totally on the mac address or sensor kind, however as i noted, the wireless nodes simply contain extra functionality for configuring the sensors, so we’ll begin with them to present you a greater entire picture of how those structures can paintings. If you haven’t already seen packets coming in from both of your sensors, cross ahead and hit the reset button on the only that hasn’t said. While a sensor exams in thru any serial device configuration node, the mac deal with and type of sensor is cached in a pool so we are able to speedy discover it at some stage in this next step.

- **Grab a Wireless Node from the palette and drag it onto the flow, double click on it to get it configured**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/wirelessdevice%20step1.JPG)

- **select the serial device from the drop down that you used for the Wireless Gateway, now click the magnifying glass next to “Mac Address” and select one of the available options.**

- ![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/wirelessdevice%20step2.JPG)

- ![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/wirelessdevice%20step3.JPG)

You’ll notice this automatically sets the sensor type for you, you can also give it a name to make it easier to identify. As noted in the info tab, the Serial Device for Config field is optional, and we won’t worry about it right now. The node you have just added effectively works as a filter on incoming sensor data, only passing through data for the mac address, or sensor type if no mac address is present.
# Displaying up the Temperature/Humidity

These nodes for the wireless sensors output a msg object with all of the same information as the Wireless Gateway node, just in a slightly different format, the Sensor Data itself is sent in the msg.payload, which is what most nodes use to interact with the msg itself. 

- **Grab a “split” node from the palette, and place it to the right of the Temp/Hum node.**
![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/split%20step1.JPG)

- **double click and check the box under Object that says “Copy key to”, this will split the msg into multiple objects, one for each property in the payload, and set the topics for those new msgs to the property names.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/split%20step2.JPG)

- **Now add a “switch” node, this will allow us to send each msg to a specific part of the flow, one to handle temperature, and one humidity. In the first field change “payload” to “topic”, next to the “==”, type “temperature”.**
![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/switch%20step1.JPG)

- **then click the “+add” button at the bottom left, in the new field type “humidity”. As you can see each of these has a unique number to the right, this number indicates which output the msg will be sent to when it matches the condition.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/switch%20step2.JPG)

- **Next let’s add a “gauge” from the palette**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gauge%20step1.JPG)

- **set the Label to “Temperature”, and the Value format to “{{value | number:2}}”, and the Units to “Celsius” you can alter the range to the minimum and maximum expected temperature, I’m using 0 and 50.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gauge%20step2.JPG)

Another really cool feature of the flow builder is copy+paste, click on the gauge you just added and click ctrl+c (cmd+c on mac), then cntl+v, now you have a second gauge, double click on it to change the Label to Humidity, the Units to RH, and the range to 20 and 80.

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/gauge%20step3.JPG)

- **Now draw wires from the Temperature/Humidity node to the split node, from the split node to the switch node, and from the switch node’s first (top) output to the temperature gauge node, and from the switch node’s second output to the humidity gauge.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/final%20flow.JPG)

Once that’s done click deploy. 

# NODE-RED DASHBOARD
Provides the ability to create a UI using the flow builder, provides charts, graphs, and a number of other visual elements we can use to display data, along with nodes to trigger a flow using user input. We will use some of these nodes to display the telemetry from your wireless sensors.

- **let’s check it out! There is a tab on the top right that says “Dashboard”**
![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/final%20flow.JPG)

- **on the top right of that tab is the little “new window” icon, click on it to view your UI.**

![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/Dashboard%20step2.JPG)

It is likely that the gauges aren’t displaying any information, because no sensor data has been reported since you deployed the flow, click the reset button on your temperature/humidity sensor to force it to check in and your gauges should jump up. You should now have real time data displaying!

# NODE-RED DASHBOARD OUTPUT
- **Now as the temperature and humidity increases and decreases new data available inside the various variable.**
![alt tag](https://github.com/ncdcommunity/Ncd-Long-Range-Temperature-and-Humidity-Sensor-with-Node-Red/blob/master/Dashboard%20output.JPG)

