# Notes


Features (preview):
- Audio strip in sequencer with edition capabilities
- Audio panel (N) with editing features
- Audio nodes per channel
- 2 sets of audio data: per strip/master

---

Fade-in / Fade-out... see Python Addon


**Audio data is processed in various areas:**
- In the Sequencer, *per VSE **Sound Strip** (type:audio, Volume, Pitch...)*
- In the Scene as *Master audio **Output** (Volume, Distance, Doppler)*
- In the 3D view as a *Speaker Object **3D** (Location, Rotation, Distance)*

---


## Audio Clip Editor (NEW)

- [x] ADD **Audio Edition** > CLIP EDITOR > CLIP TYPES (INT, STR)

**Tools:** *Set_Volume, Set_Pan, Set_Clip_Start, Set_Clip_end, Set_Fade_In, Set_Fade_Out*

- LOAD Audio Clip > SELECT file_from_path (OPEN)
- SAVE Audio Clip > SELECT file_to_path (SAVE, PACK)
- EDIT Audio Clip > VIEW > OPTIONS*
- TRANSFORM Audio Clip > EDIT > AUDIO MODIFIERS
