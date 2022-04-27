[< Back to Homepage](/../..)

---

##  NEW Sound Mixer Editor

### :speaker: Sound Mixer Area

- [x] ADD **Audio Nodes Window Area** > TYPES (INT, STR, ...)

![image](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/sound-area-menu.jpg)

---

### :speaker: Sound Mixer Nodes

> By DEFAULT the first Mix Bus is directly connected to the first available Output. A Mix Buses INPUT Node and a Device Outputs Nodes are loaded, their data are related to preferences and Scene Audio settings.
> 
![image](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/sound-area-nodes.jpg)

The Outputs Node is defined in the Channels Settings (Audio System Preferences)
- IF #channel_config = ```"Mono"```: Channel > **Outputs 1 OR 2**
- IF #channel_config = ```"Stereo"```: Channels > **Outputs 1 AND 2**
- IF #channel_config = ```"Stereo LFE"```: Channels > **Outputs 1/2 AND 3**
- IF #channel_config = ```"4 Channels"```: Channels > **Outputs 1/2 AND 3/4**
- IF #channel_config = ```"Surround 5"```: Channels > **Outputs 1/2 AND 3/4 AND 5**
- IF #channel_config = ```"Surround 5.1"```: Channels > **Outputs 1/2 AND 3/4 AND 5/6**
- IF #channel_config = ```"Surround 7"```: Channels > **Outputs 1/2 AND 3/4 AND 5/6 AND 7**
- IF #channel_config = ```"Surround 7.1"```: Channels > **Outputs 1/2 AND 3/4 AND 5/6 AND 7/8**
- IF #channel_config = ```"Custom"```: Channels > **Outputs "SELECT"** (up to 8)


---

### :speaker: Add Menu (SHIFT-A)

- Inputs
- Outputs
- Filter
- Effects
- Mixers
- Math

---

### :speaker: Tools Panel (N)

- Node
- Group
- View
- Tools
- Metadata

