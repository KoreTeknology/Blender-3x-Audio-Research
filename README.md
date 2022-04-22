# Blender 3x Audio Research

<img src="https://img.shields.io/badge/Blender-3.1+-green" /> <img src="https://img.shields.io/badge/Audaspace-C++-purple" /> <img src="https://img.shields.io/badge/Gsoc-2023-orange" />

THIS DOCUMENTATION IS PROVIDED BY ME (uriel Deveaud) "AS IS", THE EXPERIMENTAL SOURCE CODE GIVEN IN THIS DOCUMENT NO OFFERS ANY WARRANTIES OR CONDITIONS OF ANY KIND AND CAN DAMAGE YOUR BLENDER INSTALLATION IN CASE YOU TRY TO IMPLEMENT IT WITHOUT CARE, PLEASE, BE AWARE OF!

## Introduction

This current documentation is intended to demonstrate the audio features needed in the context of editing audio files within [Blender](https://www.blender.org/), the well known Free and Open Source 3D application. 
Audio editing functions are currently non-existent in the software and the only dedicated tools are present only in the context of video/audio strip editing in the VSE (Video Sequencer Editor). We want to add specific functions which will make it possible to work on the audio data by offering inputs, processing, control, visualizations and outputs as internal components within the application.

Audaspace in the integrated **video sequencer editor**, we can add features at 3 types of elements:
- *per VSE **strip** (type:audio)*
- *per VSE **channel** (channels 1...128)*
- *Master VSE audio **Outputs** (channel 0)*

Also, another option depends on **Audio nodes** (Experimental)

## Ongoing works

- [x] Personal documentation: [Concepts References](research-concepts-references.md)
- [x] [Blender](blender-related-specs.md) and [Audaspace](audaspace-related-specs.md) related specifications.
- [x] Blender Fundation & Audaspace Library documentations: [External References](ext-references.md)
- [x] Development: [Visualization Tools](blender-audio-visualizations.md) and [Operators and Properties](blender-audio-operators.md)
- [x] Extra: [Standard MIDI 2.0 implementation](blender-midi-implementation.md) for external control devices

---

## History

> **Abril 2022** - First Dev Planning and ideas, [Tasks list](Tasks.md)

## Infos

* Author: **Uriel Deveaud** - [Kore Teknology](https://github.com/KoreTeknology) 

<img src="https://img.shields.io/badge/CG Art-1995-red" /> <img src="https://img.shields.io/badge/3D Blender-2002-red" /> <img src="https://img.shields.io/badge/Python Dev-2005-red" /> <img src="https://img.shields.io/badge/3D Trainer-2008-red" /> <img src="https://img.shields.io/badge/Coding Trainer-2010-red" /> <img src="https://img.shields.io/badge/GE-2015-darkorange" /> <img src="https://img.shields.io/badge/VR-2017-darkorange" />

* This work is dedicated to all Blender users ;)
