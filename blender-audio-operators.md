# :fire: Blender Audio NEW Operators & Properties

- TRANSPORT Operators: [Strip Play & Stop](), [Strip Forward & Backward](), [Strip Record & Overdub]()
- DSP Operators and Properties: [Gain Control](blender-audio-gain.md), [Filters](blender-audio-filter.md), [Equalizer](blender-audio-equalizer.md), [Compressor & limiter](blender-audio-compressor.md), [Reverb & Delay](blender-audio-compressor.md), [Spatial audio](blender-audio-spatial.md)
- FILE Operators: [Open](), [Save](), [Reload](), [Replace](), [From Disk]()
- STRIP Operators: [Open](), [Save](), [Reload](), [Replace](), [From Disk](), [Mono](), [Modifiers]()
- MIXBUS Operators:  [Bus Assign](), [Bus Volume](),  [Bus Master Volume](), [Bus Fx](),





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


<table>
<tr>
<th align="left", width="250">Audio Operator Types</th>
<th align="left", width="632">Features</th>
</tr>
  
<tr>
<td><a href="">Gain Control</a></td>
<td align="left">Volume data</td>
</tr>
  
<tr>
<td><a href="">Sound Mix</a></td>
<td align="left">Compute Audio Data Mix Buffer</td>
</tr>

<tr>
<td><a href="">Audio Filters</a></td>
<td align="left">LPF, BPF, HPF</td>
</tr>

<tr>
<td><a href="">Equalizer</a></td>
<td align="left">About the EQ, we have here many options:<br>
<i>
<ul><li>tri-bands (fixed freqs*) with gain (what i see here in your proposal)</li>
<li>Single parametric band (very used in studio mastering)</li>
<li>up to 12 bands (fixed freqs)</li>
<li>tri-bands parametric (most common type)</li>
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
<td align="left">Care signals</td>
</tr>


</table>


---
