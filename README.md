# Blender 3x Audio Research

> **Work in Progress** [Last Updated: 01-05-2022]() by Uriel Deveaud (AKTIV25)

<img src="https://img.shields.io/badge/Blender-3+-green" /> <img src="https://img.shields.io/badge/Audaspace-C++-purple" /> <img src="https://img.shields.io/badge/Gsoc-2023-orange" /> 

## :radio_button: Introduction

This current documentation is intended to demonstrate the requested audio features in the context of editing audio contents/data within **Blender**[^1] itself, the well known Free and Open Source 3D application, and within **Audaspace**[^2], the Audio C++ Library built in Blender to process digital audio. It is mainly used in the **Video Sequencer Editor (VSE)** for playing Audio strips and **3D Space** as 3D Speaker Objects.

Here, i want to present specific [features](#radio_button-ongoing-works) which will make it possible to work on the [audio data](#radio_button-audio-data-specifications), including **routing, processing and visualizations**. For all users with basic needs in terms of **Audio Mixing**, this **[proposal](#radio_button-development-strategy-and-gsoc-proposal)** is focused on:
- **Media Productivity**[^3], including audio and Video editing, Animations, Games Post-production...
- **VR/AR Art and Experiments**, including Multiverse Production, Installations and Real-time Performances
- **Surround Contents Creation**, including music clip edition and digital mixing console, up to 8 outputs channels

> The main goal is to build a new patch (or maybe a Git Branch) to present to the **Blender Foundation**[^4] and **GSoC** 2023[^5]. The development of this patch is encouraged by the Blender community members and it will be first tested by other Blender developpers, then it will be sent to the BF for final approval. I invite you to post in the "Pull Requests" section any comments or suggestions that you think it is important to consider. Thank you.

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_band.jpg)

---

## :radio_button: Ongoing works

- [x] **Main Development Research:** **[Concepts References](research-concepts-references.md)** and **[Gui References](research-gui-references.md)**
- [x] **Personal documentation:** [Blender](blender-related-specs.md) and [Audaspace](audaspace-related-specs.md) related specifications.
- [x] **Features Development:** [Visualization Tools](blender-audio-visualizations.md) and [Operators and Properties](blender-audio-operators.md)
- [ ] **GSoc 2023** [Presentation](proposal-gsoc-presentation.md) (Video, 3D Avatar, Surround Audio)

---

## :large_blue_circle: Development Strategy and GSoc Proposal


- :one: **[Development Methodology](audio-dev-strategy.md)**
  - *[Priorities](audio-dev-strategy.md), [Sources](sources/sources-intro.md), [Diff](sources/sources-intro.md), [Notes](notes.md)*
- :two: **[New General Audio Features & System Preferences](proposal-audio-system.md)**
  - *[Channels Options](proposal-audio-system.md#speaker-channels-options), [Custom Channels](proposal-audio-system.md#speaker-custom-channels), [Channels Outputs Configuration](proposal-audio-system.md#speaker-channels-outputs-configuration), [Gui Implementation](proposal-audio-system.md#speaker-gui-implementation)*
  - Classes, Properties, Operators, Device, Device_channels, Device_output_Name
  - [Sources](sources/sources-intro.md), Notes, List

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/bas.jpg)

- :three: **[New Sequencer Sound Strip Properties](proposal-audio-clip.md)**
  - *[Mixer Properties](), [Sound_Strip Output Bus Assign](), [Device Main Mixer](), [Sound Modifiers](), [Preview]()*
  - Classes, Properties, Operators, Device, Device_channels, Device_output_Name
  - [Sources](sources/sources-intro.md)

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/bas2.jpg)

- :four: **[New Sound Mixer Space Features](proposal-sound-mixer.md)**
  - *[Sound Mixer Space](), [Audio Signals](), [Audio Nodes](), [Animate](), [FX Processing]()*
  - [Sources](sources/sources-intro.md)

> Opt

- :five: **[New Sound Clip Editor Features (Optional)](proposal-sound-mixer.md)**
  - *[Clip Editor](), [Markers](), [Fades](), [Export](), [FX Processing]()*
  - [Sources](sources/sources-intro.md)


> This document is not a definitive version yet! I do add, remove and update many parts, "without announcement", to re-format the complete documentation. Stay tuned!

---

## :radio_button: Audio Data Specifications

<table>
<tr>
<th align="left", width="250">Specifications</th>
<th align="left", width="632">Details</th>
</tr>
<tr>
<td><a href="#">Main OS Plateforms</a></td>
<td align="left">Windows, MacOS, Linux (32/64bits operating systems)</td>
</tr>
<tr>
<td><a href="#">Main Application</a></td>
<td align="left">Blender 3D</td>
</tr>
<tr>
<td><a href="/">Sound Engine</a></td>
<td align="left">Audaspace</td>
</tr>
<tr>
<td><a href="/">Codebases</a></td>
<td align="left">C++, Python</td>
</tr>
<tr>
<td><a href="/">Audio Devices</a></td>
<td align="left">WASAPI (Pulseaudio, Coreaudio, ASIO), OpenAL, OpenAL Soft, SDL</td>
</tr>
<tr>
<td><a href="/">Audio Output Channels</a></td>
<td align="left">0...8 (None, Mono to Surround 7.1)</td>
</tr>
<tr>
<td><a href="/">Audio Input Channels</a></td>
<td align="left">None</td>
</tr>
<tr>
<td><a href="/">Audio Mixing Buffer Sizes</a></td>
  <td align="left">256, 512, 1024, 2048, 4096, 8192, 16384, <b>32768</b></td>
</tr>
<tr>
<td><a href="/">Sample Rates</a></td>
<td align="left">44.1kHz 48kHz, 96kHz, <b>192kHz</b></td>
</tr>
<tr>
<td><a href="/">Sample Formats</a></td>
<td align="left">8-bit Unsigned, 16/24/32-bit Signed, <b>32/64-bit Float</b></td>
</tr>
<tr>
<td><a href="/">Sound Files</a></td>
<td align="left">AC3, FLAC, MKV, MP2, MP3, OGG, WAV</td>
</tr>
<tr>
<td><a href="/">Audio Level Unit</a></td>
<td align="left">Decibel (dB), -60 <> 0dB range, linear/Exp.</td>
</tr>
<tr>
<td><a href="/">Scene Audio Main Volume</a></td>
  <td align="left">Value: 0...<b>10000?</b></td>
</tr>
<tr>
<td><a href="/">Scene Audio Distance Models</a></td>
  <td align="left">None, Inverse, Linear, Exponent (Clamped)</td>
</tr>
<tr>
<td><a href="/">Sequence Strips</a></td>
<td align="left">Inf. (Mu)</td>
</tr>
<tr>
<td><a href="/">Sequencer Channels</a></td>
<td align="left">128</td>
</tr>
</table>

---

## :radio_button: External Links and References

### Blender builds

- Blender Source Code: [Repository](https://github.com/blender) / [Code Structure](https://wiki.blender.org/wiki/Source/File_Structure) / [Developpers Documentation](https://www.blender.org/get-involved/developers/) / [Advices](https://wiki.blender.org/wiki/Developer_Intro/Advice)
- Building Blender [Windows OS](https://wiki.blender.org/wiki/Building_Blender/Windows) / [Coding Style](https://wiki.blender.org/wiki/Style_Guide) / [Patching](https://wiki.blender.org/wiki/Process/Contributing_Code) / [Diferencial](https://secure.phabricator.com/book/phabricator/article/differential/) / [Arcanist](https://wiki.blender.org/wiki/Tools/CodeReview#Use_Arcanist)

### Audaspace Library and Python

- Audaspace Library [1.3.0 Official documentation](https://audaspace.github.io/), and neXyon´s [repository](https://github.com/neXyon/audaspace)
- Audaspace in Blender [Python API 3.1x](https://docs.blender.org/api/3.1/aud.html) / [Sound Operators](https://docs.blender.org/api/3.1/bpy.ops.sound.html) / [Sound Sequences (Strip)](https://docs.blender.org/api/3.1/bpy.types.SoundSequence.html?highlight=audio%20strip#soundsequence-sequence)
- Audio Nodes [by neXyon](https://github.com/neXyon/audionodes) / [by noemlif](https://github.com/nomelif/Audionodes)

### BPY Blender Python

- VSE Addons: [Audio Strip Fade](https://github.com/snuq/VSEQF) / [Text to Speech](https://github.com/technisculpt/blender-text-to-speech-gtts) / [VSE customizations](https://github.com/Botmasher/blender-vse-customizations) / [Sequencer Audio Recording](https://github.com/britalmeida/push_to_talk) / [Dolby Atmos Exporter](https://github.com/iluvcapra/soundobjects_blender_addon) / [Channels Export](https://github.com/samytichadou/Audio_Channels_Export) / [Cut on Peak](https://github.com/OllyFunkster/bangingcuts)
- Talks: [VSE Sound Clip](https://blender.community/c/rightclickselect/vQ65/) (RightClicSelect) / [Proposal VSE Nodes](https://devtalk.blender.org/t/proposal-using-compositor-nodes-on-vse-strips/21732)
- External Tools Addons: [Blender Audacity](https://github.com/tin2tin/audacity_tools_for_blender)

---

## :radio_button: History

> **2022 May** - Basic Audio Preferences rewriting, Vu-meter Class, [Tasks list](Tasks.md)
>
> **2022 Abril** - First Dev Planning and ideas, Files and contents structure
>
> **2017 Abril** - First Vst Plugin Development, Samples Players, Filters in C++
>
> **2016 March** - First Sequencer Script/Addon Development, Strips Management
> 
> **2014 February** - First Midi Script/Addon Development, Learning RTmidi C++ Lib
> 
> **2012 March** - First Movie Making workshop,teaching using the Blender VSE (82 students)
>
> **2011 January** - First Professional Blender Training, Design and Architecture (113 students)
>
> **2010 January** - First Audio Script/Addon Development, Learning Audaspace C++ Lib
>
> **2009 October** - First 3D Animation School Program, (185 students)
>
> **2008 October** - First Professional Video Editing using Blender VSE
>
> **2007 September** - First Blender Python Script Development
>
> **2005 June** - First Professional Animation Production using Blender
>
> **2002 December** - First 3D Model Production using Blender Free Software
>
> **2001 September** - Audio Prosessing Hardware Development [Google Patents](https://patents.google.com/patent/FR2839601A1/en)

## :radio_button: Infos

* Author: **Uriel Deveaud**[^note] - [Kore Teknology](https://github.com/KoreTeknology) 

<img src="https://img.shields.io/badge/CG Art-1995-red" /> <img src="https://img.shields.io/badge/3D Blender-2002-red" /> <img src="https://img.shields.io/badge/Python Dev-2005-red" /> <img src="https://img.shields.io/badge/3D Trainer-2008-red" /> <img src="https://img.shields.io/badge/Coding Trainer-2010-red" /> <img src="https://img.shields.io/badge/GE-2015-darkorange" /> <img src="https://img.shields.io/badge/VR-2017-darkorange" />

[^1]: **Blender** is the free and open source 3D creation suite. It supports the entirety of the 3D pipeline—modeling, rigging, animation, simulation, rendering, compositing and motion tracking, even video editing and game creation. Please, visit the [Blender Official Website](https://www.blender.org/).
[^2]: **Audaspace** (pronounced "outer space") is a high level audio library written in C++ with language bindings for Python for example. It started out as the audio engine of the 3D modelling application Blender and is now released as a standalone library. [Audaspace Website](https://audaspace.github.io/)... TODO
[^3]: In This case, Blender is used as a Audio/Video Sequencer Editor
[^4]: The Blender Foundation (2002) is an independent public benefit organization with the purpose to provide a complete, free and open source 3D creation pipeline, managed by public projects on blender.org.
[^5]: **GSoc** or **Google Summer of Code** is a global, online program focused on bringing new contributors into open source software development. GSoC Contributors work with an open source organization on a 12+ week programming project under the guidance of mentors.
[^note]:
    This work is dedicated to **all Blender users** ;) and the **Free Software Foundation Members**.
    I do this work in my free time, without any profit, enjoy!
