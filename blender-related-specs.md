[<< Back to main page](/../..) ```Blender Audio Research - uriel Deveaud @2022 ```

---

# Blender related specifications

## Audio Project Scenes Settings

In the Scene Properties Panel is located an audio settings box, that includes:
<table>
<tr>
<th align="left", width="200">
Settings
</th>
<th align="left", width="382">
Details
</th>
<th align="left", width="100">
Min.
</th>
<th align="left", width="100">
Max.
</th>
<th align="left", width="100">
Default
</th>
</tr>
  
<tr>
<td>
Volume (Main)
</td>
<td>
is_Animated
</td>
<td>
<i>0.0</i>
</td>
<td>
<i>100.0</i>
</td>
<td>
<i>1.0</i>
</td>
</tr>
  
<tr>
<td>
Distance Model
</td>
<td>
- None<br>- Iverse / Inverse Clamped<br>- Linea / Linear Clamped<br>- Exponent / Exponent Clamped
</td>
<td>
[0]
</td>
<td>
[7]
</td>
<td>
[3]
</td>
</tr>
  
<tr>
<td>
Doppler Speed
</td>
<td>
Speed of Sound
</td>
<td>
<i>0.01</i>
</td>
<td>
<i>10 000.0</i>
</td>
<td>
<i>1.0</i>
</td>
</tr>
  
<tr>
<td>
Doppler Factor
</td>
<td>
Pitch Factor for Doppler Effect
</td>
<td>
<i>0.0</i>
</td>
<td>
<i>10 000.0</i>
</td>
<td>
<i>1.0</i>
</td>
</tr>

</table>

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

```diff 
- !!! At this time, Audio clip cannot be edited !!!
```

## Rendering Audio

About the multi-channel rendering and export features... **Render Audio Mixdown**

```diff
- ONLY Render Audio based on Channels settings (Mono export option)
+ text in green
! text in orange
# text in gray
@@ Remap (and bold)@@
```

# Audio Operators

> bpy.ops.sound.mixdown
```diff
! (filepath='', check_existing=True, filter_blender=False, filter_backup=False, filter_image=False, filter_movie=False, 
! filter_python=False, filter_font=False, filter_sound=True, filter_text=False, filter_archive=False, filter_btx=False, 
! filter_collada=False, filter_alembic=False, filter_usd=False, filter_obj=False, filter_volume=False, filter_folder=True, 
! filter_blenlib=False, filemode=9, relative_path=True, display_type='DEFAULT', sort_method='', accuracy=1024, container='FLAC', 
! codec='FLAC', format='S16', bitrate=192, split_channels=False)
```

## Relations

### DeviceManager Class Reference

```c++
#include <DeviceManager.h> > 
```

**aud.Device** Device objects represent an audio output backend like OpenAL or SDL, but might also represent a file output or RAM buffer output

<table>
<tr><th align="left", width="441">Audaspace</th><th align="left", width="441">Blender</th></tr>
<tr><td>registerDevice()</td><td>_</td></tr>
<tr><td>getDeviceFactory()</td><td>_</td></tr>
<tr><td>getDefaultDeviceFactory()</td><td>_</td></tr>
<tr><td>setDevice()</td><td>_</td></tr>
<tr><td>openDevice()</td><td>_</td></tr>
<tr><td>openDefaultDevice()</td><td>_</td></tr>
<tr><td>releaseDevice()</td><td>_</td></tr>
<tr><td>getDevice()</td><td>_</td></tr>
<tr><td>get3DDevice()</td><td>_</td></tr>
<tr><td>getAvailableDeviceNames()</td><td>_</td></tr>
</table>



