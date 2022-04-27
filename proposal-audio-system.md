![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_header.jpg)

> This document is not a definitive version! I do add, remove and update many parts, "without announcement", to re-format the complete documentation. Stay tuned!

- ### PART 1:  [New General Audio Features]()
  > Definition, Classes, Sub-Classes, Methods, Properties, Operators
- ### PART 2:  [New Audio Preferences Features]()
  > Device, Device_channels, Outputs, Device_outputs
- ### PART 3:  [New Sequencer Features]()
  > Sequencer_strip, Audio_strip, Strip_seq_channel, Strip_aud_bus
- ### PART 4:  [New Clip Editor Features]()
  > File, Path, Open, Save, Modifiers 
- ### PART 5:  [New 3D Objects Features]()
  > Channels Configuration, Direction, Distance
- ### PART 6:  [New Sound Mixer Features]()
  > Audio Nodes, Signals, Effects 





---

## 1/ Audio System Preferences (IN PROGRESS)

**Note:** *Depends on Channels settings, user can select outputs configuration, based on driver´s options.*

- IF #channel_config = **"Mono"**: Channel > **Outputs 1 OR 2**
- IF #channel_config = **"Stereo"**: Channels > **Outputs 1 AND 2**
- IF #channel_config = **"4 Channels"**: Channels > **Outputs 1/2 AND 3/4**
- IF #channel_config = **"Surround 5.1"**: Channels > **Outputs 1/2 AND 3/4 AND 5**
- IF #channel_config = **"Surround 7.1"**: Channels > **Outputs 1/2 AND 3/4 AND 5/6 AND 7**
- IF #channel_config = **"Custom"**: Channels > **Outputs "SELECT"**

### Channels Mixing 

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio_channel_settings2.jpg)

### Custom

<table>
<tr>
<th align="left", width="200">
Channels Settings
</th>
<th align="center", width="200">
Available Properties
</th>
<th align="left", width="482">
Options
</th>
</tr>

<tr>
<td>
Up to 16
</td>
<td align="center">
Stereo Mode
</td>
<td>
Dual-Mono
</td>
</tr>
 
</table>

### GUI Implementation

1/ **New GUI Properties** User Preferences Device options: Soundcard, Outputs settings

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/prefs_after2.jpg)

- [x] ADD **Channels Configuration Options** > SELECT SOUND CARD HARDWARE (INT, STR)
- [x] ADD **Channels Configuration Options** > SELECT SOUND CARD OUTPUTS (INT)
- [x] ADD **Mixbuses Configuration Options** > USE NODES (BOOL)
- [x] ADD **Sound Clips Configuration Options** > USE MODIFIERS IN CLIP EDIT MODE (BOOL)
- [x] ADD **Mixer Configuration Options** > USE REAL-TIME VUMETERS (BOOL)
- [x] ADD **MixBuses Configuration Options** > NUMBER OF MIXBUSES (INT)

> Files:


2/ **New GUI Properties** Scene Properties: Sound, Mix Buses Configuration Panel

- [x] ADD **New Property** > (Set_AudBus_Volume)
- [x] ADD **New Property** > (Set_AudBus_count up to 16)
- [ ] ADD **Default Property** > (Set_AudBus_count[0] Stereo *!!!cannot be removed!!!*)
- [ ] ADD **Fonction** > Vu-meter(sample_level, sync_channels, buffer_read)

The Scene Panel includes options,regarding the channels count and preferences (Vu-meters, Volume Sliders). 

> Files:


3/ **New GUI Properties** Sequencer Audio Strip: Audio Mix Bus routing(Default)

- [x] ADD **MixBus Input Selection** > TYPES (INT, STR, ...)

> Files:
> 
```diff
- **Blender Struct**: Audio_Preferences_NEW_Settings_Channels
+ **Change #01:** The Audio Preference settings includes audio routing and Soundcard options.
```

---

## 2/ Sound Mixer Editor (NEW)

- [x] ADD **Audio Nodes Window Area** > TYPES (INT, STR, ...)

> By DEFAULT the first Mix Bus is directly connected to the first available Output. A Mix Buses INPUT Node and a Device Outputs Nodes are loaded, their data are related to preferences and Scene Audio settings.

**Tools Panel (N)**
- Node
- Group
- View
- Tools
- Metadata


---

## 4/ Audio Clip Editor (NEW)

- [x] ADD **Audio Edition** > CLIP EDITOR > CLIP TYPES (INT, STR)

**Tools:** *Set_Volume, Set_Pan, Set_Clip_Start, Set_Clip_end, Set_Fade_In, Set_Fade_Out*

- LOAD Audio Clip > SELECT file_from_path (OPEN)
- SAVE Audio Clip > SELECT file_to_path (SAVE, PACK)
- EDIT Audio Clip > VIEW > OPTIONS*
- TRANSFORM Audio Clip > EDIT > AUDIO MODIFIERS

```diff
- **Blender Struct**: Clip_Editor_NEW_Type_Audio
+ **Change #02:** The Clip Editor includes *Audio Clip* and basic editing features
```

---

## 5/ Audio Speaker Object in 3D View

- [x] ADD **Speaker 3D Object Options** > TYPES (INT, STR, ...)

---


> Updated on 24.05.22
