# Main Project Concepts

Based on Blender Audio Specifications and Audaspace Implementation: [Audio in Blender](blender-related-specs.md)

## Objectives

The main objective is to **revise the blender´s audio system, in order to allow the development of new functionalities in the field of sound edition**. **The goal is not for Blender to look like a DAW**, but to include basic audio editing functions to be available to the user in the context of video editing.

- Review of the complete Audio system within Blender
- Explore New **Audio system Preferences**
- Explore New **Audio features** (Record, Edit, Mix Buses)
- Add system preferences data, Channels data, Bus mixer
- Add Audio Editor Area (type NodeGroups)
- Add Vu-meters, Add Fx/Filters, Add Generators

## Suggested Structural Update

- **Audio system Preferences** (regarding the channels model, add device outputs connection selection
- **Audio File/Project Settings** (Number of buses)
- **Export Mixdown** (optional multi files, e.g. ToMono output single files)
- **Audio Nodes Window area** (Inputs, Buses Inputs, Output Files, Device Outputs
- **Audio Clip editor** (Add audio type and previews)

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio-basic_redesign.jpg)

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


