# Blender 3x Audio Research

<img src="https://img.shields.io/badge/Blender-3.1+-green" /> <img src="https://img.shields.io/badge/Audaspace-C++-purple" /> <img src="https://img.shields.io/badge/Gsoc-2023-orange" />

THIS DOCUMENTATION IS PROVIDED BY ME (uriel Deveaud) "AS IS", <br>WITHOUT ANY WARRANTIES OR CONDITIONS OF ANY KIND, PLEASE, BE AWARE OF!

## Introduction

This current documentation is intended to demonstrate the audio features needed in the context of editing audio files within [Blender](https://www.blender.org/), the well known Free and Open Source 3D application. Audaspace is integrated in Blender as Audio C++ Library. It is used in the **video sequencer editor (VSE)** and **3D Space**. Audio data can be treated in various types:
- *per VSE **Sound Strip** (type:audio)*
- *Master VSE audio **Outputs** (sequencer´s channel 0)*
- *Speaker Object **3D** (Location, Rotation, Distance)*

Here, we want to add specific functions which will make it possible to work on the audio data by offering inputs, processing, control, visualizations and outputs as internal components within the application. For users with specific needs in terms of Audio Mixing, this proposal focus on Media Productivity, VR Art Experiments, Multiverse and Surround Contents creation, and more... One of the proposal relate to **Audio nodes (Sound Mixer)** implementation.

## Ongoing works

- [ ] **Main Development:** **[Concepts References](research-concepts-references.md)** and **[Proposal 2022](proposal-audio-system.md)** (V 0.4)
- [x] **Personal documentation:** [Blender](blender-related-specs.md) and [Audaspace](audaspace-related-specs.md) related specifications.
- [x] **Features Development:** [Visualization Tools](blender-audio-visualizations.md) and [Operators and Properties](blender-audio-operators.md)
- [x] Blender Fundation & Audaspace Library **Documentations:** [External Links](ext-references.md)
- [x] Extra: [Standard MIDI 2.0 implementation](blender-midi-implementation.md) for **External Control Devices**

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
> **2005 Jun** - First Professional Animation Production using Blender
>
> **2002 December** - First 3D Model Production using Blender Free Software

## Infos

* Author: **Uriel Deveaud** - [Kore Teknology](https://github.com/KoreTeknology) 

<img src="https://img.shields.io/badge/CG Art-1995-red" /> <img src="https://img.shields.io/badge/3D Blender-2002-red" /> <img src="https://img.shields.io/badge/Python Dev-2005-red" /> <img src="https://img.shields.io/badge/3D Trainer-2008-red" /> <img src="https://img.shields.io/badge/Coding Trainer-2010-red" /> <img src="https://img.shields.io/badge/GE-2015-darkorange" /> <img src="https://img.shields.io/badge/VR-2017-darkorange" />

* This work is dedicated to all Blender users ;)
