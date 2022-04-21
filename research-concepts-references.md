# Main Project Concepts

## Audio specifications

Blender can work with various types of audio files and formats: .WAV, .MP3, ...

### Blender Sound Settings Preferences

Blender gots a bunch of Audio settings in the system configuration preferences:
- Audio Device
- Channels
- Mixing Buffer
- Sample Rate
- Sample Format

> !!! Rework of audio settings preferences is necessary !!!
> It must include the per-output channel settings (e.g. Rename, Mix Buses)

### GUI Objects

THINK The user actions on sounds is limited in sequencer view, alternative view for edit.
IF Audio Fx is placed between the mix buses and the Master Output buses, 
  Audio nodes system is permited.



### NEXT: Audio Levels

- The unit used for audio level (inputs/outputs) is expressed in decibel dB.
- The reference range is -60 <> 0dB
- the steps can be linear or dynamic (optional)
