# TinyML-Words-Classifier
[Embedded Machine Learning (TinyML) ](https://docs.edgeimpulse.com/docs/what-is-embedded-machine-learning-anyway) on [Arduino Nano 33 BLE Sense](https://store.arduino.cc/usa/nano-33-ble-sense) using Edge Impulse.
[Edge Impulse](https://www.edgeimpulse.com/our-story) is the leading development platform for machine learning on edge devices, free for developers and trusted by enterprises.

You will learn how to build a ML model for motion or gesture recognition system that runs on a microcontroller.

In able to do that, you will need to do the following steps. For more details click [this](https://docs.edgeimpulse.com/docs/arduino-nano-33-ble-sense).
1. Create your [Edge Impulse](https://www.edgeimpulse.com/#:~:text=Edge%20Impulse%20is%20the%20leading,developers%20and%20trusted%20by%20enterprises.) account.
2. Setup the required software on your computer.
   You will need to install the following software:
   -  [Node.js v12.xx](https://nodejs.org/en/download/) or higher.
   -  [Arduino CLI](https://arduino.github.io/arduino-cli/installation/). This is how you [install Arduino CLI](https://www.youtube.com/watch?v=1jMWsFER-Bc) on Windows 10.
   -  Install the [Edge Impulse CLI](https://docs.edgeimpulse.com/docs/cli-installation) by opening a command prompt or terminal and run
      ```
                      npm install -g edge-impulse-cli
      ```
3.  Setup your Arduino device in Edge Impulse. 
    - Connect your Arduino Nano 33 BLE Sense on your computer then double press on the *reset push button* quickly to launch the bootloader. The on-board LED should start          pulsating to indicate this.
    
      ![alt tag](https://files.readme.io/b302301-out.gif) 
    
    - Download the latest [Edge Impulse firmware](https://cdn.edgeimpulse.com/firmware/arduino-nano-33-ble-sense.zip), and unzip the file. Open the flash script according to your operating system. For Windows 10, run the *flash_windows.bat* to flash the firmware to your Arduino device.
    - Then open a command prompt or terminal and run
      ```
                      edge-impulse-daemon
      ```
    - Then input your Edge Impulse account credentials. To veryfy to Arduino Device is connected, in your [edge impulse project](https://docs.edgeimpulse.com/docs/arduino-nano-33-ble-sense), click **Devices** tab. The device will be listed here.
    
    ![alt tag](https://files.readme.io/b5b9f02-arduino03.png) 
