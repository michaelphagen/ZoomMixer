# ZoomMixer
A Mixer for Zoom, built in MaxMSP, and intended to be used with Loopback or Soundflower.

Currently development is only for MacOS (though feel free to try it on other platforms!)

[Looking for the download? Click here](https://github.com/michaelphagen/ZoomMixer/releases)

## Relies on:
 [Jeremy Bernstein's Shell External MAX/MSP Object](https://github.com/jeremybernstein/shell) (if building from source)
and either [Rogue Amoeba's Loopback](https://rogueamoeba.com/loopback/) or [Matt Ingalls' Soundflower](https://github.com/mattingalls/Soundflower)

## Setup
To use the application, audio must be routed digitally through the computer. To accomplish this, Loopback/Soundflower/any other virtual audio device must be used. For this example setup, Soundflower will be used.

First, [Install Soundflower](https://github.com/mattingalls/Soundflower/releases), following the instructions on the releases page.

Next, open Audio Midi setup on your computer
![Image of Audio Midi Setup](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Audio%20Midi%20Setup.png)

Click the + button at the bottom of the screen and Select "Multi-Output Device"
![Image showing the "Multi-Output Device" option](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Creating%20Mixer%20%26%20Monitoring%20Device.png)

Name the Device "Mixer & Monitoring", and select both "Soundflower (64ch)" and the normal device that you use to listen to audio on your system. In this example, I use the Built-In Output on my Mac so I have chosen "Built-in Output"

![Image showing the "Mixer & Monitoring Device"](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Mixer%20%26%20Monitoring%20Device.png)

This device is where you will route audio from your computer to send it to the Zoom Mixer. This includes Pro Tools, Logic Pro X, Ableton, and the Normal Computer's output. All of these should be set to use the "Mixer & Monitoring" device as the audio output.

Next Click the + button again but this time choose "Aggregate Device".
![Image showing the "Mixer & Monitoring Device" and clicking the + button for Aggregate Device](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Creating%20To%20Mixer%20Device.png)

Name the Device "To Mixer" and select the device that you normally use for microphone input, followed by "Soundflower (64ch)". In the window above the checkboxes, the first subdevice must be the microphone, and the second subdevice must be Soundflower/ **!!THE ORDER MATTERS!!**

![Image showing the "To Mixer" Device](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/To%20Mixer%20Device.png)

Finally, click the + button one last time and select "Multi-Output Device" again.
![Image showing the "To Mixer" Device and clicking on "Multi-Output Device"](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Creating%20From%20Mixer%20Device.png)

Here, just choose "Soundflower (2ch)"

![Image showing the "From Mixer" Device](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/From%20Mixer%20Device.png)

Download the latest version of the Zoom Mixer from [the releases page](https://github.com/michaelphagen/ZoomMixer/releases), unzip it, and put the application in your applications folder.

Now you can open the Zoom Mixer, and it will automatically set itself up. Any Audio that you want to send to your videoconferencing platform must be sent to the "Mixer & Monitoring" Device (since you want to send it to the mixer and also monitor it). For example, You should set your system audio output to "Mixer & Monitoring" to send audio from applications like Safari, Powerpoint, and Google Chrome to your videoconferencing application.

![Image showing the System Output window](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/System%20Output.png). 

In applications where you can set a separate audio output device (Such as Logic Pro X), you must set the device to "Mixer & Monitoring" as well. 

![Image Showing Logic's Audio Setting window](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Logic%20Output.png).

In your videoconferencing application, you should set the Microphone to "Soundflower (2ch)" and the Speaker to whatever you want the other videoconferencing participant's audio to come out of. ![Image Showing the options set for videoconferencing I/O](https://github.com/michaelphagen/ZoomMixer/blob/master/Docs/Images/Videoconferencing%20Input.png)

Enjoy!
