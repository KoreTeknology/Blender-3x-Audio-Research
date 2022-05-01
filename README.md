# Blender 3x Audio Research

> **Work in Progress** [Last Updated: 01-05-2022]() by Uriel Deveaud (AKTIV25)

<img src="https://img.shields.io/badge/Blender-3.1+-green" /> <img src="https://img.shields.io/badge/Audaspace-C++-purple" /> <img src="https://img.shields.io/badge/Gsoc-2023-orange" /> 

## :radio_button: Introduction

This current documentation is intended to demonstrate the requested audio features in the context of editing audio contents/data within **Blender**[^1] itself, the well known Free and Open Source 3D application and **Audaspace**[^2] the Audio C++ Library built in Blender to process digital audio. It is mainly used in the **Video Sequencer Editor (VSE)** for playing Audio strips and **3D Space** as 3D Speaker Objects.

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

## :radio_button: Development Strategy and GSoc Proposal (In Progress)


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

> This document is not a definitive version yet! I do add, remove and update many parts, "without announcement", to re-format the complete documentation. Stay tuned!

---

## :radio_button: Audio Data Specifications

<table>
<tr>
<th align="left", width="250">Specifications</th>
<th align="left", width="632">Details</th>
</tr>
<tr>
<td><a href="/">Main OS Plateforms</a></td>
<td align="left">Windows, MacOS, Linux (32/64bits operating systems)</td>
</tr>
<tr>
<td><a href="/">Main Application</a></td>
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
<td align="left">WASAPI (ASIO), OpenAL, OpenAL Soft, SDL</td>
</tr>
<tr>
<td><a href="/">Audio Level Unit</a></td>
<td align="left">Decibel (dB), -60 <> 0dB range, linear/Exp.</td>
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
<td><a href="/">Audio Output Channels</a></td>
<td align="left">0...8 (None, Mono to Surround 7.1)</td>
</tr>
<tr>
<td><a href="/">Audio Intput Channels</a></td>
<td align="left">None</td>
</tr>
<tr>
<td><a href="/">Sequence Strips</a></td>
<td align="left">Inf. (Mu)</td>
</tr>
<tr>
<td><a href="/">Sequencer Channels</a></td>
<td align="left">128</td>
</tr>
<tr>
<td><a href="/">Scene Audio Main Volume</a></td>
  <td align="left">0...<b>10000?</b></td>
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

- VSE Addons: [Audio Strip Fade](https://github.com/snuq/VSEQF) / [Text to Speech](https://github.com/technisculpt/blender-text-to-speech-gtts) / [VSE customizations](https://github.com/Botmasher/blender-vse-customizations)
- [VSE Sound Clip (RightClicSelect)](https://blender.community/c/rightclickselect/vQ65/)
- [Blender Audacity Tools](https://github.com/tin2tin/audacity_tools_for_blender)


### DevTalks Users Proposals

- [Proposal VSE Nodes](https://devtalk.blender.org/t/proposal-using-compositor-nodes-on-vse-strips/21732)

TO BE CONTINUED...

---

## :radio_button: History

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

## :radio_button: Infos

* Author: **Uriel Deveaud**[^note] - [Kore Teknology](https://github.com/KoreTeknology) 

<img src="https://img.shields.io/badge/CG Art-1995-red" /> <img src="https://img.shields.io/badge/3D Blender-2002-red" /> <img src="https://img.shields.io/badge/Python Dev-2005-red" /> <img src="https://img.shields.io/badge/3D Trainer-2008-red" /> <img src="https://img.shields.io/badge/Coding Trainer-2010-red" /> <img src="https://img.shields.io/badge/GE-2015-darkorange" /> <img src="https://img.shields.io/badge/VR-2017-darkorange" />


[^1]: **Blender** is the free and open source 3D creation suite. It supports the entirety of the 3D pipeline—modeling, rigging, animation, simulation, rendering, compositing and motion tracking, even video editing and game creation. Advanced users employ Blender’s API for Python scripting to customize the application and write specialized tools; often these are included in Blender’s future releases. Blender is well suited to individuals and small studios who benefit from its unified pipeline and responsive development process. Examples from many Blender-based projects are available in the showcase. Blender is cross-platform and runs equally well on Linux, Windows, and Macintosh computers. Its interface uses OpenGL to provide a consistent experience. To confirm specific compatibility, the list of supported platforms indicates those regularly tested by the development team. As a community-driven project under the GNU General Public License (GPL), the public is empowered to make small and large changes to the code base, which leads to new features, responsive bug fixes, and better usability. Blender has no price tag, but you can invest, participate, and help to advance a powerful collaborative tool: Blender is your own 3D software. More help is always welcome! From developing and improving Blender to writing documentation, etc, there are a number of different things you can do to get involved. Please, visit the [Blender Official Website](https://www.blender.org/).
[^2]: Audaspace is a C++ Library: [Audaspace WebPage](https://audaspace.github.io/)... TODO
[^3]: In This case, Blender is used as a Audio/Video Sequencer Editor
[^4]: The Blender Foundation is TODO
[^5]: GSoc or Google Summer of Code is...TODO
[^note]:
    This work is dedicated to **all Blender users** ;) and the **Free Software Foundation Members**.
    I do this work in my free time, without any profit, enjoy!
