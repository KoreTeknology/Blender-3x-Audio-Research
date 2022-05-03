[<< Back to main page](/../..) ```Blender Audio Research - uriel Deveaud @2022 ```

---

# :fire: Blender Audio NEW Operators & Properties


- FILE Operators and Properties: [Open](), [Save](), [Reload](), [Replace](), [From Disk]()
- STRIP Operators and Properties: [Open](), [Save](), [Reload](), [Replace](), [From Disk](), [Mono](), [Modifiers]()
- TRANSPORT Operators and Properties: [Strip Play & Stop](), [Strip Forward & Backward](), [Strip Record & Overdub]()
- MIXBUS Operators and Properties:  [Bus Assign](), [Bus Volume](),  [Bus Master Volume](), [Bus Fx](),
- VISUALIZATION Operators and Properties:  [Level-meters](), [Vu-meter](),  [Multi-channels](), [Bus Fx](), [Spectral Analysis](). [Spectogram](), [Sound Field]()
- DSP Operators and Properties: [Gain Control](blender-audio-gain.md), [Filters](blender-audio-filter.md), [Equalizer](blender-audio-equalizer.md), [Compressor & limiter](blender-audio-compressor.md), [Reverb & Delay](blender-audio-compressor.md), [Spatial audio](blender-audio-spatial.md)





<table align="center">
<tr>
<th align="left", width="20"><a href="">A</a></th>
<th align="left", width="20"><a href="">B</a></th>
<th align="left", width="20"><a href="">C</a></th>
<th align="left", width="20"><a href="">D</a></th>
<th align="left", width="20"><a href="">S</a></th>
<th align="left", width="20"><a href="">U</a></th>
</tr>
<table>

## Visualization Features
 
<table>
<tr>
<th align="left", width="200">Operators</th>
<th align="left", width="132">State</th>
<th align="left", width="582">Features</th>
</tr>
 
<tr>
 <td  valign="top"><a href="">Vu-level</a><br><sub>Type: VU_audioMeter</sub></td>
<td align="left"  valign="top">-</td>
 <td align="left">A volume unit (VU) meter or standard volume indicator (SVI) is a device displaying a representation of the signal level in audio equipment.(<a href="https://en.wikipedia.org/wiki/VU_meter">Wikipedia</a>).<br><a href="https://github.com/KoreTeknology/Blender-3x-Audio-Research/blob/main/blender-audio-visualizations.md#1-vu-meter">See Research Details</a></td>
</tr>
<tr>
<td  valign="top"><a href="">Vu-Spectrogram</a><br><sub>Type: VU_audioMeter</sub></td>
<td align="left"  valign="top">-</td>
<td align="left">A spectrogram is a visual representation of the spectrum of frequencies of a signal as it varies with time.(<a href="https://en.wikipedia.org/wiki/Spectrogram">Wikipedia</a>).</td>
</tr>  
<tr>
<td  valign="top"><a href="">Vu-Fourier</a><br><sub>Type: VU_audioMeter</sub></td>
<td align="left"  valign="top">-</td>
<td align="left">(<a href="https://en.wikipedia.org/wiki/Fourier_analysis">Wikipedia</a>).</td>
</tr> 
<tr>
<td  valign="top"><a href="">Vu-Phase</a><br><sub>Type: VU_audioMeter</sub></td>
<td align="left"  valign="top">-</td>
<td align="left"></td>
</tr> 
<tr>
<td  valign="top"><a href="">Vu-Spectral</a><br><sub>Type: VU_audioMeter</sub></td>
<td align="left"  valign="top">-</td>
<td align="left"></td>
</tr> 
<tr>
<td  valign="top"><a href="">Vu-Field</a><br><sub>Type: VU_audioMeter</sub></td>
<td align="left"  valign="top">-</td>
<td align="left"></td>
</tr> 
</table> 
 
<table>
<tr>
<th align="left", width="200">Properties</th>
<th align="left", width="132">State</th>
<th align="left", width="582">Features</th>
</tr>
 
<tr>
<td><a href="">Master_level_meter</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
<tr>
<td><a href="">Strip_level_meter</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>  
</table> 
 
---
 
 ## File Features
 
## Transport Features
 
<table>
<tr>
<th align="left", width="200">Operators</th>
<th align="left", width="132">State</th>
<th align="left", width="582">Features</th>
</tr>
 
<tr>
<td><a href="">Strip_Edit_Play</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
<tr>
<td><a href="">strip_Edit_Pause</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>  
<tr>
<td><a href="">strip_Edit_Stop</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
<tr>
<td><a href="">strip_Edit_Reverse</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
</table> 
 
<table>
<tr>
<th align="left", width="200">Properties</th>
<th align="left", width="132">State</th>
<th align="left", width="582">Features</th>
</tr>
 
<tr>
<td><a href="">Strip_Edit_Play</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
<tr>
<td><a href="">strip_Edit_Pause</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>  
<tr>
<td><a href="">strip_Edit_Stop</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
<tr>
<td><a href="">strip_Edit_Reverse</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
</table> 
 
---
  
<table>
<tr>
<th align="left", width="200">Mixbus Ops Types</th>
<th align="left", width="132">State</th>
<th align="left", width="582">Features</th>
</tr>
 
<tr>
<td><a href="">Mixbus_Bus_Leveler</a></td>
<td align="left">-</td>
<td align="left"></td>
</tr>
</table> 

<table>
<tr>
<th align="left", width="200">Dsp Ops Types</th>
<th align="left", width="132">State</th>
<th align="left", width="582">Features</th>
</tr>
  
<tr>
<td><a href="">Gain Control</a></td>
<td align="left">-</td>
<td align="left">Volume data</td>
</tr>
  
<tr>
<td><a href="">Sound Mix</a></td>
<td align="left">-</td>
<td align="left">Compute Audio Data Mix Buffer</td>
</tr>

<tr>
<td><a href="">Audio Filters</a></td>
<td align="left">-</td>
<td align="left">LPF, BPF, HPF</td>
</tr>

<tr>
<td  valign="top"><a href="">Equalizer</a></td>
<td align="left" valign="top">-</td>
<td align="left">Equalization in sound recording and reproduction is the process of adjusting the volume of different frequency bands within an audio signal. (<a href="https://en.wikipedia.org/wiki/Equalization_(audio)">Wikipedia</a>). Multiple options:<br>
<i>
<ul>
<li>Single parametric band (very used in studio mastering)</li>
<li>Tri-bands , up to 12 bands (fixed freqs)</li>
<li>Tri-bands parametric (most common type)</li>
<li>etc…</li>
  </ul></i>
<b>Fixed bands EQ</b> (in case of tri-bands selection):
<ul><li>20Hrz > 500Hrz (-15/+15db)</li>
<li>200Hrz > 5kHrz (-15/+15db)</li>
<li>800Hrz > 20kHrz (-15/+15db)</li>
</ul></i>
As well as the gain for that frequencies range, we should have a Q (curve shape for each band), i didnt try with audaspace if the Q will be a constant value, but we can look at.</td>
</tr>
  
<tr>
<td><a href="">Compresor/Limiter</a></td>
<td align="left">-</td>
<td align="left">Care signals</td>
</tr>


</table>


---
