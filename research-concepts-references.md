# Main Project Concepts

## Audio specifications

Blender can work with various types of audio data:
- **File containers:** .AC3, .FLAC, .MKV, .MP2, .OGG, .WAV, .MP3
- **Sample Format:** S16/S24

## Blender Sound Settings Preferences

Blender gots a bunch of Audio settings in the system configuration preferences:

<table>
<tr>
<th align="left", width="200">
Settings
</th>
<th align="left", width="682">
Options
</th>
</tr>
<tr>
<td>
Audio Device
</td>
<td>
WASAPI, OpenAL, SDL, (no ASIO?)
</td>
</tr>
<tr>
<td>
Channels
</td>
<td>
Mono, Stereo, 4 Channels, 5.1 Surround, 7.1 Suround
</td>
</tr>
<tr>
<td>
Mixing Buffer
</td>
<td>
256...up to 32768 samples
</td>
</tr>
<tr>
<td>
Sample Rate
</td>
<td>
44.1...192kHrz
</td>
</tr>
<tr>
<td>
Sample Format
</td>
<td>
8...64bits
</td>
</tr>
</table>

> !!! Rework of audio settings preferences is necessary !!!
> It must include the per-output channel settings (e.g. Rename, Mix Buses)

## Audio Project Scenes Settings

In the Scene Properties Panel is located an audio settings box, that includes:
- Volume (Main, animated)
- Distance Model
- Doppler Speed
- Doppler Factor

## Audio Strip

An Audio file is loaded in blender as a sequence file (AKA "Audio Strip"). This content includes several properties:
- Volume (animated)
- Pitch (animated)
- Pan
- Mono (Bool)
- Display Waveform (Bool)
- Channel (Sequencer channel!) (Int)
- Start
- Duration
- Strip Offset Start
- Strip Offset End
- Hold Offset Start
- Hold Offset End
- Source File (String)
- Path to file (String)
- Packing (Bool)
- Caching (Bool)
- Strip Modifiers (Add)
- Cache Settings (Check if apply to audio?)

## Clip Editor

!!! At this time, Audio clip cannot be edited !!!

## Rendering Audio

About the multi-channel rendering and export features... **Render Audio Mixdown**

---

## New Concept: Mix Buses and Effects

### Main audio unit
- The unit used for audio level (inputs/outputs) is expressed in decibel dB.
- The reference range is -60 <> 0dB
- the steps can be linear or dynamic (optional)

### Audio Routing
This option includes a Mix Buses routing interface between the audio strips and the Master-to-Devices outputs.
- Preferences Settings are: **Number of Buses** (1,2,4,8) and **Device Output Channels**
- Options are: **Audio Strip Bus** (depends on preferences)
- Default connections: **Bus ST 1 > Output 1+2** ...

![Mixbuses](https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/images/mixbuses_concept.jpg)

**Notes:** The user actions on sounds is limited in sequencer view, alternative view for edit.
IF Audio Fx is placed between the mix buses and the Master Output buses, 
  Audio nodes system is permited.

### Structural Update

- **Audio system Preferences** (regarding the channels model, add device outputs connection selection
- **Audio File/Project Settings** (Number of buses)
- **Export Mixdown** (optional multi files, e.g. ToMono output single files)
- **Audio Nodes Window area** (Inputs, Buses Inputs, Output Files, Device Outputs
- **Audio Clip editor** (Add audio type and previews)


