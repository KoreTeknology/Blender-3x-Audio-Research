# Main Project Concepts

Based on Blender Audio Specifications and Audaspace Implementation: [Audio in Blender](blender-related-specs.md)
This is a Research pool for that project. Once the concepts is written and code analysis is done, the documentation section will be moved to the proposal section, available from the [homepage](https://github.com/KoreTeknology/Blender-3x-Audio-Research#development-strategy-and-gsoc-proposal
).

<table>
<tr>
<th align="left", width="250">Concepts</th>
<th align="left", width="632">Features</th>
</tr>
<tr>
<td><a href="">Device Outputs Channels</a></td>
<td align="left">The Device physical outputs fromthe user´s soundcard specifications. Audio driver will allow up to 16 outputs channels</td>
</tr>
<tr>
<td><a href="">Bus Mixer Routing</a></td>
<td align="left">The Mixing Channels. The internal audio routing includes a Bus mixing areawhere user can define his sound strategy.</td>
</tr>
<tr>
<td><a href="">Strip Bus Channels</a></td>
<td align="left">Assign Buses to Strip</td>
</tr><tr>
<td><a href="">Audio Mixdown</a></td>
<td align="left">Export Channel Strips</td>
</tr>
 
</table>

## New Concept I: Mix Buses and Effects

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



---


