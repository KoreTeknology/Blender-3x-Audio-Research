# Blender 3x Audio Research

<img src="https://img.shields.io/badge/Blender-3.1+-green" /> <img src="https://img.shields.io/badge/Audaspace-C++-purple" /> <img src="https://img.shields.io/badge/Gsoc-2023-orange" />

## Introduction

This current documentation is intended to demonstrate the requested audio features in the context of editing audio files within [Blender](https://www.blender.org/), the well known Free and Open Source 3D application. [Audaspace](https://audaspace.github.io/) is an Audio C++ Library built in Blender to process digital audio. It is mainly used in the **video sequencer editor (VSE)** for playing Audio strips and **3D Space** as 3D Speaker Objects.

Here, i want to present specific features which will make it possible to work on the audio data, including **routing, processing and visualizations**. For all users with basic needs in terms of **Audio Mixing**, this proposal focus on **Media Productivity, VR/AR Art and Experiments, Multiverse and Surround Contents creation, and more...**. 

The main goal is to build a new patch (or maybe a Git Branch) to present to the **Blender Foundation** and **GSoC** 2023. The development of this patch is encouraged by the Blender community members and it will be first tested by other Blender developpers, then it will be sent to the BF for final approval. I invite you to post in the "Pull Requests" section any comments or suggestions that you think it is important to consider. Thank you.

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_band.jpg)

---

## Ongoing works

- [x] **Main Development Research:** **[Concepts References](research-concepts-references.md)**
- [x] **Personal documentation:** [Blender](blender-related-specs.md) and [Audaspace](audaspace-related-specs.md) related specifications.
- [x] **Features Development:** [Visualization Tools](blender-audio-visualizations.md) and [Operators and Properties](blender-audio-operators.md)
- [ ] Extra: [Standard MIDI 2.0 implementation](blender-midi-implementation.md) for **USB External Control Devices**
- [ ] **GSoc 2023** [Presentation](proposal-gsoc-presentation.md) (Video, 3D Avatar, Surround Audio)

---

## Development Strategy and GSoc Proposal


- **PART 1:  [Development Methodology](audio-dev-strategy.md)**
  - *[Priorities](audio-dev-strategy.md)*
  - [Sources](sources/sources-intro.md), Notes, List
- **PART 2:  [New General Audio Features & System Preferences](proposal-audio-system.md)**
  - *[Channels Options](proposal-audio-system.md#speaker-channels-options), [Custom Channels](proposal-audio-system.md#speaker-custom-channels), [Channels Outputs Configuration](proposal-audio-system.md#speaker-channels-outputs-configuration), [Gui Implementation](proposal-audio-system.md#speaker-gui-implementation)*
  - Classes, Properties, Operators, Device, Device_channels, Device_output_Name
  - [Sources](sources/sources-intro.md), Notes, List
- **PART 3:  [New Sequencer Sound Strip Properties](proposal-audio-clip.md)**
  - *[Mixer Properties](), [Sound_Strip Output Bus Assign](), [Device Main Mixer](), [Sound Modifiers]()*
  - Classes, Properties, Operators, Device, Device_channels, Device_output_Name
  - [Sources](sources/sources-intro.md)
- **PART 4:  [New Sound Mixer Space Features](proposal-sound-mixer.md)**
  - *[Sound Mixer Space](), [Audio Signals](), [Audio Nodes](), [Animate](), [FX Processing]()*
  - [Sources](sources/sources-intro.md)

> This document is not a definitive version! I do add, remove and update many parts, "without announcement", to re-format the complete documentation. Stay tuned!

---

## External Links and References

### Blender builds

- Blender Source Code: [Repository](https://github.com/blender) / [Code Structure](https://wiki.blender.org/wiki/Source/File_Structure) / [Developpers Documentation](https://www.blender.org/get-involved/developers/) / [Advices](https://wiki.blender.org/wiki/Developer_Intro/Advice)
- Building Blender [Windows OS](https://wiki.blender.org/wiki/Building_Blender/Windows) / [Coding Style](https://wiki.blender.org/wiki/Style_Guide) / [Patching](https://wiki.blender.org/wiki/Process/Contributing_Code) / [Diferencial](https://secure.phabricator.com/book/phabricator/article/differential/) / [Arcanist](https://wiki.blender.org/wiki/Tools/CodeReview#Use_Arcanist)

### Audaspace Library and Python

- Audaspace 1.3.0 [Official documentation](https://audaspace.github.io/)
- Audaspace in Blender API 3.1x [BF documentation](https://docs.blender.org/api/3.1/aud.html)
- Sound Operators in Blender API 3.1x [BF documentation](https://docs.blender.org/api/3.1/bpy.ops.sound.html)
- Sound Sequences (Strip) [BF Documentation](https://docs.blender.org/api/3.1/bpy.types.SoundSequence.html?highlight=audio%20strip#soundsequence-sequence)
- Audio Nodes by neXyon [Blender Free Addon](https://github.com/neXyon/audionodes)
- Audio Nodes by nomelif [Blender Free Addon](https://github.com/nomelif/Audionodes)
- Audaspace repository by neXyon [High level audio library written in C++](https://github.com/neXyon/audaspace)

### BPY Blender Python

- Audio VSE Fade Addon [Repo](https://github.com/snuq/VSEQF)
- Blender Audacity Tools Addon [Repo](https://github.com/tin2tin/audacity_tools_for_blender)
- VSE Sound Clip [RCS](https://blender.community/c/rightclickselect/vQ65/)
- VSE customizations Addon [Repo](https://github.com/Botmasher/blender-vse-customizations)
- VSE Text to Speech Addon [Repo](https://github.com/technisculpt/blender-text-to-speech-gtts)

### DevTalks Users Proposals

- [Proposal VSE Nodes](https://devtalk.blender.org/t/proposal-using-compositor-nodes-on-vse-strips/21732)

TO BE CONTINUED...



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

* This work is dedicated to all Blender users ;) and the Free Software Foundation Members

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_header.jpg)
