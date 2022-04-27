# Main Project Concepts

Based on Blender Audio Specifications and Audaspace Implementation: [Audio in Blender](blender-related-specs.md)
This is a Research pool for that project. Once the concepts is written and code analysis is done, the documentation section will be moved to the proposal section, available from the [homepage](https://github.com/KoreTeknology/Blender-3x-Audio-Research#development-strategy-and-gsoc-proposal
).

## Objectives

The main objective is to **revise the blender´s audio system, in order to allow the development of new functionalities in the field of sound edition**. **The goal is not for Blender to look like a DAW**, but to include basic audio editing functions to be available to the user in the context of video editing, VR/AR Production and Surround Video Clip Creation.

- Review of the complete Audio system within Blender
- Explore New **Audio system Preferences**
- Explore New **Audio features** (Record, Edit, Mix Buses)
- Add system preferences data, Channels data, Bus mixer
- Add Audio Editor Area (type NodeGroups)
- Add Vu-meters, Add Fx/Filters, Add Generators

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio-basic_redesign2.jpg)

## Suggested Structural Update

- **Audio system Preferences** (regarding the channels model, add device outputs connection selection
- **Audio File/Project Settings** (Number of buses)
- **Export Mixdown** (optional multi files, e.g. ToMono output single files)
- **Audio Nodes Window area** (Inputs, Buses Inputs, Output Files, Device Outputs
- **Audio Clip editor** (Add audio type and previews)

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio-basic_redesign.jpg)

> By DEFAULT, Number of SubMix Buses = Number of Device Outputs and Channels Configuration!
> 
> User can Add an Audio Mix Bus in the Audio Nodes window area

---

## New Concept I: Mix Buses and Effects

### Main audio unit
- The unit used for audio level (inputs/outputs) is expressed in decibel dB.
- The reference range is -60 <> 0dB
- the steps can be linear or dynamic (optional)

### Audio Routing
This option includes a Mix Buses routing interface between the audio strips and the Master-to-Devices outputs.
- Preferences Settings are: **Number of Buses** (1,2,4,8) and **Device Output Channels**
- Options are: **Audio Strip Bus** (depends on preferences)
- Default connections: **Bus ST 1 > Output 1+2** ...

![Mixbuses](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/mixbuses_concept.jpg)

**Notes:** The user actions on sounds is limited in sequencer view, alternative view for edit.
IF Audio Fx is placed between the mix buses and the Master Output buses, 
  Audio nodes system is permited.



---


