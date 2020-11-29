# TinyML-Words-Classifier
[Embedded Machine Learning (TinyML) ](https://docs.edgeimpulse.com/docs/what-is-embedded-machine-learning-anyway) on [Arduino Nano 33 BLE Sense](https://store.arduino.cc/usa/nano-33-ble-sense) using Edge Impulse. [Edge Impulse](https://www.edgeimpulse.com/our-story) is the leading development platform for machine learning on edge devices, free for developers and trusted by enterprises.

You will build a ML model in Edge Impulse Studio and deploy it to your microcontroller device to develop a single word speech recognition system. In this repo, it can recognized the words "Yes", "No", "On", and "Off".

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
3. Prepapre your datasets, download the [prebuilt dataset](https://docs.edgeimpulse.com/docs/keyword-spotting) Keyword spotting from Edge Impulse documentation, and [Speech Commands Dataset](http://download.tensorflow.org/data/speech_commands_v0.01.tar.gz) from Google AI. Extract the files on the folder.

4. Upload your single word voice or speech datasets to your Edge Impulse project. You are free to choose which words are going to use.
   -  Connect your local computer to Edge Impulse studio. Open your command prompt, and run
      ```
                      edge-impulse-daemon
      ```
      Input your account credentials and select a project, if you have a prevous project, switch the connection to your new project, clear the Edge Impulse daemon configuration the running the command
      ```
                      edge-impulse-daemon --clean
      ```
   -  Upload your existing datasets to your Edge Impulse project. There are two methods to [upload](https://docs.edgeimpulse.com/docs/cli-uploader) your datasets, first go to the **Data acquisition** and click the *upload* icon. You can select files in *.wav* file format, the *category* and the *label* directly from Edge Impulse Studio.
   
      ![alt tag](https://files.readme.io/3677848-Screenshot_2020-07-16_at_13.34.56.png) 
      
      The other method is uploading via command prompt. This method is reliable and faster of uploading a large number of datasets. If you want to use **Off** dataset, run the command
      ```
                      edge-impulse-uploader --label Off C:\Users\Path\to\a\file\Off\*.wav
      ```
     
     ![alt tag](https://github.com/TronixLab/TinyML-Words-Classifier/blob/main/results/UploadingFilesCMD.jpg?raw=true)

5. With the data set in place you can design an impulse. In the Studio, go to the **Create impulse tab**, add a Time series data, an Audio (MFCC) and a Neural Network (Keras) block. Leave the window size to 1 second (as that's the length of our audio samples in the dataset) and click Save Impulse. For more details, visit the [**Responsing to your voice**](https://docs.edgeimpulse.com/docs/responding-to-your-voice) tutorial.
   
      ![alt tag](https://files.readme.io/6556142-Screenshot_2020-11-19_at_22.39.24.png)

6. Before training your neural network model, we'll need to generate Mel Frequency Cepstral Coefficient (MFCC) blocks to extract the audio features and classify it. To do this, click the *Generate features* button at the top of the page, then click the **green Generate features** button. This will take a minute or so to complete. Afterwards you will see a 3D representation showing your complete dataset, with each data-item color-coded to its respective label. This is a usefull tool to find anomalies (an item that's in a wrong cluster), and to validate whether your dataset is suitable for ML (it should separate nicely).

      ![alt tag](https://github.com/TronixLab/TinyML-Words-Classifier/blob/main/results/DataClassificationGraph.jpg?raw=true)
      
      
      
