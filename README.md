# Blender 3x Audio Research

<img src="https://img.shields.io/badge/Blender-3.1+-green" /> <img src="https://img.shields.io/badge/Audaspace-C++-purple" /> <img src="https://img.shields.io/badge/Gsoc-2023-orange" />

THIS DOCUMENTATION IS PROVIDED BY ME (uriel Deveaud) "AS IS", <br>WITHOUT ANY WARRANTIES OR CONDITIONS OF ANY KIND, PLEASE, BE AWARE OF!

## Introduction

This current documentation is intended to demonstrate the requested audio features in the context of editing audio files within [Blender](https://www.blender.org/), the well known Free and Open Source 3D application. [Audaspace](https://audaspace.github.io/) is an Audio C++ Library built in Blender to process audio. It is mainly used in the **video sequencer editor (VSE)** as Audio strips and **3D Space** as 3D Speaker Objects.

Here, i want to present specific features which will make it possible to work on the audio data, including **routing, processing and visualizations**. For all users with basic needs in terms of **Audio Mixing**, this proposal focus on **Media Productivity, VR Art Experiments, Multiverse and Surround Contents creation, and more...**. 

The main goal is to build a new patch to present to the **Blender Fundation** and **GSoC** 2023. The development of this patch is encouraged by the Blender community members and it will be first tested by other Blender developpers, then it will be sent to the BF for final approval. I invite you to post in the "Pull Requests" section any comments or suggestions that you think it is important to consider. Thank you.

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_band.jpg)

---

## Ongoing works

- [x] **Main Development:** **[Concepts References](research-concepts-references.md)**
- [x] **Personal documentation:** [Blender](blender-related-specs.md) and [Audaspace](audaspace-related-specs.md) related specifications.
- [x] **Features Development:** [Visualization Tools](blender-audio-visualizations.md) and [Operators and Properties](blender-audio-operators.md)
- [x] Blender Fundation & Audaspace Library **Documentations:** [External Links](ext-references.md)
- [ ] **GSoc 2023** [Presentation](proposal-gsoc-presentation.md) (Video, 3D Avatar, Surround Audio)
- [ ] Extra: [Standard MIDI 2.0 implementation](blender-midi-implementation.md) for **USB External Control Devices**

---

## Development Strategy and GSoc Proposal

- **PART 1:  [New General Audio Features & System Preferences](proposal-audio-system.md)**
  - [Definition](), Classes, Properties, Operators, Device, Device_channels, Device_output_Name
  - [Codes Patch](), Notes, List
- **PART 2:  [New Sequencer & Clip Editor Features](proposal-audio-clip.md)**
  - [Definition](), Audio_strip, Strip_seq_channel, Strip_aud_bus, FilePath, Sound Modifiers
  - [Codes Patch](), Notes, List
- **PART 3:  [New 3D Objects Features](proposal-3d-object.md)**
  - [Definition](), Speakers, Channels Configuration, Direction, Distance
  - [Codes Patch](), Notes, List
- **PART 4:  [New Sound Mixer Features](proposal-sound-mixer.md)**
  - [Definition](), Audio Nodes, Signals, Effects 
  - [Codes Patch](), Notes, List

> This document is not a definitive version! I do add, remove and update many parts, "without announcement", to re-format the complete documentation. Stay tuned!

---

## History

> **2022 Abril** - First Dev Planning and ideas, [Tasks list](Tasks.md)
>
> **2016 March** - First Sequencer Script/Addon Development, Strips Management
> 
> **2014 February** - First Midi Script/Addon Development, Learning RTmidi C++ Lib
> 
> **2012 March** - First Movie Making workshop using the VSE (82 students over 3 years)
>
> **2010 January** - First Audio Script/Addon Development, Learning Audaspace C++ Lib
>
> **2009 October** - First Professional Video Editing using Blender VSE
>
> **2007 September** - First Blender Python Script Development
>
> **2005 June** - First Professional Animation Production using Blender
>
> **2002 December** - First 3D Model Production using Blender Free Software

## Infos

* Author: **Uriel Deveaud** - [Kore Teknology](https://github.com/KoreTeknology) 

<img src="https://img.shields.io/badge/CG Art-1995-red" /> <img src="https://img.shields.io/badge/3D Blender-2002-red" /> <img src="https://img.shields.io/badge/Python Dev-2005-red" /> <img src="https://img.shields.io/badge/3D Trainer-2008-red" /> <img src="https://img.shields.io/badge/Coding Trainer-2010-red" /> <img src="https://img.shields.io/badge/GE-2015-darkorange" /> <img src="https://img.shields.io/badge/VR-2017-darkorange" />

* This work is dedicated to all Blender users ;)

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_header.jpg)
