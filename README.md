# My First Watch


## Setup and installation

### Android Studio
Download Android studio here http://developer.android.com/sdk/index.html.
After having installed Android Studio, install also the SDK for android wear and the SDK samples package.
Tools->Android->SDK Manager

### Setting up Virtual Devices 
Set up virtual devices for handheld and android wear using Tools->Android->AVD Manager
Note that you can not run both Virtual handheld and wear devices at the same time, they wont sync with each other. This is not officially supported yet by Google. 

### Enable develop mode on handheld phone
Connect the real handheld phone using an usb cable, and install android wear on it.
Go to Settings->General-> About Device and click on the "build number" cell 7 times. This will enable develop mode in your handheld device. Go to the "Develop options" Menu and enable usb debugging mode. And click Allow to allow the computer to connect to your handheld.

#### Pairing android wear emulator with handheld

Start the Android wear device emulator in Android studio. 

In a terminal window run: 
> adb devices

You should see a list of devices attached both handheld and android wear emulator.

This will command will allow packets to be transferred between the handheld usb to android wear simulator
> adb -d forward tcp:5601 tcp:5601

Run Android wear app in the handheld device, you should now see that the android wear app is connected to android wear emulator. If not pair with emulator by clicking on the top right corner menu.

Turn on debug log for the Tag:
> adb -e shell setprop log.tag.AnalogWatchFaceService DEBUG










