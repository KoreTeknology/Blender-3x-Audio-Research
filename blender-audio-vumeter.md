# Vu Meter

This UI tools gives visual information about the audio volume. 

## The problem
In most video editing, animations, lips-sync, we actualy don´t have any data regarding the level or the gain of the audio files used in the scene. To avoid saturated audio outputs or underleveled audio strips, we would need both Main outputs level meter AND individual strip level indicators.
First, we need to place the level meters in the GUI. The audio section is linked to the VSE, that offers preview window and sequencer view (and both). These window areas ave an option panel (N Key).

## The options

### Option 1: Audio Vu-meters in the VSE per-channel

At the Gui level, let´s look at the possible implementation. In the VSE, Blender offers a channel header [See Devlog: change D13836](https://developer.blender.org/D13836), and this area can be used to add several infos or tools.

![image](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio_vse_channels.jpg)

In these exemples, we can see the audio level for each "channels". An other option exists and offers a "per-strip" audio level meter.
We also have a "mute audio" button to control channels mixing. Apart from these basic features, an audios equencer must include: Solo button, Mute button, level value slider, and level monitor control. All those GUI elements can be shown optionaly using the view menu entries

### Option 2: Audio Vu-meter in the "Preview window" tool panel (N)


### Option 3: Audio Vu-meter in the "Sequencer window" tool panel (N)


### Option 4: A master channels in the "Sequencer window"

## The solutions


TO EDIT
