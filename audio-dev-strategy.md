[<< Back to main page](/../..) ```Blender Audio Research - uriel Deveaud @2022 ```

---

## Development Strategy and Methodology

### Objectives:

:one: Review of the complete Audio system within Blender

:two: Explore New **Audio system Preferences** and **Eco-system**

:three: Add New system preferences, **Output Channels**, (Channels, Device outputs)

:four: Add New Scene Properties, **Mix Bus Channels** (user setting)

:five: Add New Sequencer Audio **Strip Properties** (Mix Bus), add Sound strip Preview

:six: Add **Sound Mixer** Area (Default setups)

:seven: Add **Audio Clip Editor** Area (type Video Clip Editor), add Fx/Filters modifiers

:eight: Add sound **Visualizations** (real time), e.g. Vu-meter

:nine: Explore New **Sound features** (Record, Surround Fx, Sub-Mix, Generators)


```diff
+ Keeping in mind that we are NOT making Blender looking like a Digital Audio workstation (DAW), 
+ we want to focus on the most relevant audio processing implementation to support future developments.
```

My approach is to look at the fundamental audio settings and preferences before going further. At this very beginning stage, a more **advanced preferences panel** is necessary. I also consider any changes from the user´s point of view. **A discrete implementation for the users is required**. As long as the user doesn´t look for Audio mixing features, the default audio setup will apply (Stereo channel, 1 Stereo Mix Bus, 2 outputs channels)

**3 focused developments agendas:**
- [Preferences and Default Sound Mixer Setup (from 1 to 16 output channels)]()
- [Sequencer Sound Strip Properties and Operators (Mix Bus and Modifiers)]()
- [Advanced Mixer Setup within a new Editor space (Complex routing/Processing)]()

Changes are:
- **Audio system Preferences** (regarding the channels model, add device outputs connection selection)
- **Audio File/Project Settings** (Number of buses)
- **Export Mixdown** (optional multi files, e.g. ToMono output single files)
- **Audio Nodes Window area** (Inputs, Buses Inputs, Output Files, Device Outputs
- **Audio Clip editor** (Add audio type and previews)

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio-basic_redesign2.jpg)

> By DEFAULT, Number of SubMix Buses = Number of Device Outputs and Channels Configuration!
> 
> User can Add an Audio Mix Bus in the Audio Nodes window area

---

### :speaker: Multiplex Audio Routing

### :speaker: Basic to Complex

### :speaker: Soundcards and Drivers

### :speaker: Audio Channels and Outputs

### :speaker: Mixer Component

### :speaker: Bus Component

### :speaker: Audaspace existing features 

Audspace is a strong C++ Audio library, it includes a wide variety of Audio procesing features (See Audaspace Modules and Classes). We can identify thoses modules in different categories:
- Device
- Generators
- Inputs/Outputs
- Effects
- Mixer
- ...
