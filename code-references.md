# Code References (Blender Sources)



## [blender/blenkernel/BKE_sound.h](https://github.com/blender/blender/blob/master/source/blender/blenkernel/BKE_sound.h)

### Line 65: eSound Channels

```c++
/* Matches AUD_Channels. */
typedef enum eSoundChannels {
  SOUND_CHANNELS_INVALID = 0,
  SOUND_CHANNELS_MONO = 1,
  SOUND_CHANNELS_STEREO = 2,
  SOUND_CHANNELS_STEREO_LFE = 3, // Not exposed in GUI
  SOUND_CHANNELS_SURROUND4 = 4,
  SOUND_CHANNELS_SURROUND5 = 5,
  SOUND_CHANNELS_SURROUND51 = 6, // Mono sub out ?
  SOUND_CHANNELS_SURROUND61 = 7, // Not exposed in GUI
  SOUND_CHANNELS_SURROUND71 = 8,
} eSoundChannels;
```

### Line 90: Mixdown Master Sound

```c++
/* Get information about given sound. Returns truth on success., false if sound can not be loaded
 * or if the codes is not supported. */
bool BKE_sound_info_get(struct Main *main, struct bSound *sound, SoundInfo *sound_info);

/* Get information about given sound. Returns truth on success., false if sound can not be loaded
 * or if the codes is not supported. */
bool BKE_sound_stream_info_get(struct Main *main,
                               const char *filepath,
                               int stream,
                               SoundStreamInfo *sound_info);

#if defined(WITH_AUDASPACE)
AUD_Device *BKE_sound_mixdown(const struct Scene *scene,
                              AUD_DeviceSpecs specs,
                              int start,
                              float volume);
#endif
```
