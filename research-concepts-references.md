# Main Project Concepts

## Audio specifications

Blender can work with various types of audio files and formats: .WAV, .MP3, ...

## Rendering Audio

About the multi-channel rendering and export features...

### Blender Sound Settings Preferences

Blender gots a bunch of Audio settings in the system configuration preferences:
- Audio Device
- Channels
- Mixing Buffer
- Sample Rate
- Sample Format

> !!! Rework of audio settings preferences is necessary !!!
> It must include the per-output channel settings (e.g. Rename, Mix Buses)

### NEXT: Mix Buses and Effects

This option includes a set of Mix Buses between the audio strips and the Master-to-Devices outputs

![Mixbuses](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/mixbuses_concept.jpg)


### NEXT: GUI Objects

THINK The user actions on sounds is limited in sequencer view, alternative view for edit.
IF Audio Fx is placed between the mix buses and the Master Output buses, 
  Audio nodes system is permited.

### NEXT: Audio Levels

- The unit used for audio level (inputs/outputs) is expressed in decibel dB.
- The reference range is -60 <> 0dB
- the steps can be linear or dynamic (optional)


