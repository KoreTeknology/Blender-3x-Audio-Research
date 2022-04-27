[< Back to Homepage](/../..)

---

## NEW Blender Audio System Preferences

### :speaker: Channels Options

By DEFAULT, When the user is selecting his channels options, these ```audio routings``` will apply:

- IF #channel_config = ```"Mono"```: Channel > **Outputs 1 OR 2**
- IF #channel_config = ```"Stereo"```: Channels > **Outputs 1 AND 2**
- IF #channel_config = ```"Stereo LFE"```: Channels > **Outputs 1/2 AND 3**
- IF #channel_config = ```"4 Channels"```: Channels > **Outputs 1/2 AND 3/4**
- IF #channel_config = ```"Surround 5"```: Channels > **Outputs 1/2 AND 3/4 AND 5**
- IF #channel_config = ```"Surround 5.1"```: Channels > **Outputs 1/2 AND 3/4 AND 5/6**
- IF #channel_config = ```"Surround 7"```: Channels > **Outputs 1/2 AND 3/4 AND 5/6 AND 7**
- IF #channel_config = ```"Surround 7.1"```: Channels > **Outputs 1/2 AND 3/4 AND 5/6 AND 7/8**
- IF #channel_config = ```"Custom"```: Channels > **Outputs "SELECT"**

**Note:** *Depends on Channels "Device" settings (Driver Selection), user can select outputs configuration, based on soundcard specifications.*

### :speaker: Custom Channels

This is where it becomes interesting, the custom option offers a 1-to-1 channels configuration.

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

In this configuration, the user can create/Edit/Delete channels and apply a customized outputs routing. Also, if the user has an option selected (e.g. surround 5.1), and if he delete or add a channel, the option becomes automatically a "custom" type.

### :speaker: Channels Outputs Configuration 

![Mix](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/Audio_channel_settings2.jpg)


### :speaker: GUI Implementation

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

``` - **Blender Struct**: Audio_Preferences_NEW_Settings_Channels  ```

---

> Updated on 24.05.22
