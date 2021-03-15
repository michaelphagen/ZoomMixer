# ZoomMixer
A Mixer for Zoom, built in MaxMSP, and intended to be used with Loopback or Soundflower

As of Version 1.2 The ZoomMixer assumes that it will receive input from a virtual device called "To Mixer" and will send its output to another virtual device called from mixer. While built with [Rogue Amoeba's Loopback](https://rogueamoeba.com/loopback/) in mind, a free solution can be accomplished using [Matt Ingalls' Soundflower](https://github.com/mattingalls/Soundflower) and renaming the 64 Channel instance to "To Mixer" and the 2 Channel Instance to "From Mixer" using Aggregate Devices in Audio Midi Setup.

The "To Mixer" Device should consist of Microphone followed by Loopback/Soundflower device, as a 4 channel virtual audio device. Input 1 and 2 are the Microphone, and 3&4 are the Loopback/Soundflower Device.

The "From Mixer" Device should just be a loopback/soundflower device, as a 2 channel virtual audio device
