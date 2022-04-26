# Code References (Blender Sources)

[blender/blenkernel/BKE_sound.h](https://github.com/blender/blender/blob/master/source/blender/blenkernel/BKE_sound.h)

```c++
/* Matches AUD_Channels. */
typedef enum eSoundChannels {
  SOUND_CHANNELS_INVALID = 0,
  SOUND_CHANNELS_MONO = 1,
  SOUND_CHANNELS_STEREO = 2,
  SOUND_CHANNELS_STEREO_LFE = 3,
  SOUND_CHANNELS_SURROUND4 = 4,
  SOUND_CHANNELS_SURROUND5 = 5,
  SOUND_CHANNELS_SURROUND51 = 6,
  SOUND_CHANNELS_SURROUND61 = 7,
  SOUND_CHANNELS_SURROUND71 = 8,
} eSoundChannels;

```
