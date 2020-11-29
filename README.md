# TinyML-Words-Classifier
[Embedded Machine Learning (TinyML) ](https://docs.edgeimpulse.com/docs/what-is-embedded-machine-learning-anyway) on [Arduino Nano 33 BLE Sense](https://store.arduino.cc/usa/nano-33-ble-sense) using Edge Impulse. [Edge Impulse](https://www.edgeimpulse.com/our-story) is the leading development platform for machine learning on edge devices, free for developers and trusted by enterprises.

You will build a ML model in Edge Impulse Studio and deploy it to your microcontroller device to develop a single word speech recognition system.

In able to do this, you will need to do the following steps. For more details click [this](https://docs.edgeimpulse.com/docs/arduino-nano-33-ble-sense).
1. Create your [Edge Impulse](https://www.edgeimpulse.com/#:~:text=Edge%20Impulse%20is%20the%20leading,developers%20and%20trusted%20by%20enterprises.) account.
2. Setup the required software on your computer.
   You will need to install the following software:
   -  [Node.js v12.xx](https://nodejs.org/en/download/) or higher.
   -  [Arduino CLI](https://arduino.github.io/arduino-cli/installation/). This is how you [install Arduino CLI](https://www.youtube.com/watch?v=1jMWsFER-Bc) on Windows 10.
   -  Install the [Edge Impulse CLI](https://docs.edgeimpulse.com/docs/cli-installation) by opening a command prompt or terminal and run
      ```
                      npm install -g edge-impulse-cli
      ```
3. Prepapre youe datasets, download the [prebuilt dataset](https://docs.edgeimpulse.com/docs/keyword-spotting) Keyword spotting from Edge Impulse documentation, and [Speech Commands Dataset](http://download.tensorflow.org/data/speech_commands_v0.01.tar.gz) from Google AI.
