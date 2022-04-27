[< Back to Homepage](https://github.com/KoreTeknology/Blender-3x-Audio-Research)

---

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/proposal_header.jpg)

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

> Updated on 24.05.22
