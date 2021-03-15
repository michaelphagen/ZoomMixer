# ZoomMixer
A Mixer for Zoom, built in MaxMSP, and intended to be used with Loopback or Soundflower.

Currently development is only for MacOS (though feel free to try it on other platforms!)

## Relies on:
 [Jeremy Bernstein's Shell External MAX/MSP Object](https://github.com/jeremybernstein/shell) (FOR BUILDING FROM SOURCE ONLY)
and either [Rogue Amoeba's Loopback](https://rogueamoeba.com/loopback/) or [Matt Ingalls' Soundflower](https://github.com/mattingalls/Soundflower)

## A note about Virtual Devices
As of Version 1.2 The ZoomMixer assumes that it will receive input from a virtual device called "To Mixer" and will send its output to another virtual device called from mixer. While built with [Rogue Amoeba's Loopback](https://rogueamoeba.com/loopback/) in mind, a free solution can be accomplished using [Matt Ingalls' Soundflower](https://github.com/mattingalls/Soundflower) by creating a Multi Output device including the 2 channel instance of soundflower and the computer's normal audio output device, then creating an aggregate device using this multi-output device and the computer's normal microphone device. Input 1&2 shoud be the multi-output device and inputs 3&4 should be the computer's microphone input device. This Aggregate Device should then be named "To Mixer". A second aggregate/multi-output device(it doesn't matter which) must be created using the 64 channel instance of soundflower by itself and must be named "From Mixer".

## Setup
To use the application, audio must be routed digitally through the computer. To accomplish this, Loopback/Soundflower/any other virtual audio device must be used. The mapping is below:

The "To Mixer" Device should consist of Microphone followed by Loopback/Soundflower device, as a 4 channel virtual audio device. Input 1 and 2 are the Loopback/Soundflower Device, and 3&4 are the Microphone.

The "From Mixer" Device should just be a loopback/soundflower device, as a 2 channel virtual audio device

Application/System audio
