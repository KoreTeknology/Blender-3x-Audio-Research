# Proposal

## 1/ Audio System Preferences

- [x] ADD **Channels Configuration Options** > SELECT SOUND CARD HARDWARE (INT, STR)
- [x] ADD **Channels Configuration Options** > SELECT SOUND CARD OUTPUTS (INT)
- [x] ADD **Channels Configuration Options** > USE NODES (BOOL)
- [x] ADD **MixBus Configuration Options** > NUMBER OF MIXBUSES (INT)

**Note:** *Depends on Channels settings, user can select outputs configuration, based on driver´s options.*

- IF #channel_config = **"Mono"**: Channel > **Outputs 1 OR 2**
- IF #channel_config = **"Stereo"**: Channels > **Outputs 1 AND 2**
- IF #channel_config = **"4 Channels"**: Channels > **Outputs 1/2 AND 3/4**
- IF #channel_config = **"Surround 5.1"**: Channels > **Outputs 1/2 AND 3/4 AND 5**
- IF #channel_config = **"Surround 7.1"**: Channels > **Outputs 1/2 AND 3/4 AND 5/6 AND 7**
- IF #channel_config = **"Custom"**: Channels > **Outputs "SELECT"**

<table>
<tr>
<th align="left", width="200">
Channels Settings
</th>
<th align="center", width="200">
Available Outputs
</th>
<th align="left", width="482">
Drivers
</th>
</tr>
  
<tr>
<td>
Custom
</td>
<td align="center">
Up to 16
</td>
<td>
ALL
</td>
</tr>
 
</table>

```diff
- **Blender Struct**: Audio_Preferences_NEW_Settings_Channels
+ **Change #01:** The Audio Preference settings includes audio routing and Soundcard options.
```

---

## 2/ Audio Scene Options

- [x] ADD **New Settings** > ()

---

## 3/ Audio Clip Editor

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

## 4/ Audio MixBus Editor

- [x] ADD **Audio Nodes Window Area** > TYPES (INT, STR, ...)

---

## 5/ Audio Speaker Object in 3D View

- [x] ADD **Speaker 3D Object Options** > TYPES (INT, STR, ...)

---


> Updated on 24.05.22
