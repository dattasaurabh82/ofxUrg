##ofxURG
A Fork with updates from [Yusuke Tomoto's](https://github.com/yusuketomoto) [ofxURG](https://github.com/yusuketomoto/ofxUrg)

This includes a tracker from [Kyle McDonald's](https://github.com/kylemcdonald) [ofxSick](https://github.com/ZigelbaumCoelho/ofxSick)

###OSC Sender
![Image of Sender](https://raw.githubusercontent.com/danthemellowman/ofxUrg/master/images/sender.png)


###OSC Receiver
![Image of Receiver](https://raw.githubusercontent.com/danthemellowman/ofxUrg/master/images/receiver.png)

![Image of device](https://raw.githubusercontent.com/danthemellowman/ofxUrg/master/images/device.JPG)
### Setup
1. Add the contents of this repo to the "addons" folder of Open Frameworks.
2. Unzip ofxUrg>releases>"Sender.zip"
3. Plug the Urg scanner into a powered USB hub. Plug the powered USB hub into the computer. NOTE: The Urg scanner can draw .8 amps on start-up. This is more than most computer USB ports can supply. The use of a powered USB hub is highly recommended.

![Image of device](https://raw.githubusercontent.com/danthemellowman/ofxUrg/master/images/physical_setup.JPG)

4. Open Terminal and type in "ls / dev/tty.*"
5. Copy the like that is returned. it will look something like "/dev/tty.usbmodem14521".
6. Open the ofxUrg>releases>Sender>data>"settings.xml".
7. Replace the centre part of the third line: "<Serial_Port>/dev/tty.usbmodem14521</Serial_Port>" with the text that you just copied.
8. Launch the "example.app"

### Usage
- The "maxClusterCount" and "maxStddev" define the number and sensitivity of the tracking points.
- "X", "Y", and "Search Region Size" define the area that will be searched for Clusters.
- Pressing "Use Auto Region" will display all the raw data at the time pressed.
- The "example.app" outputs the raw data and the cluster data over OSC at the IP adress and Port listed. These can be changed in the "settings.xml".
- Use the Receiver app as an example of how to read this OSC stream.


### General Notes
- The Urg scanner uses an infrared laser. Some materials reflect IR light better than others. This can make a large difference in the quality of readings.