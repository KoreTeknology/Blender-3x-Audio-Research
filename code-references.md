# Code References (Blender Sources)

## [blender/sequencer/SEQ_sound.h](https://github.com/blender/blender/blob/master/source/blender/sequencer/SEQ_sound.h)

### Line 14: Sound Strip

```c++
struct Main;
struct Scene;
struct Sequence;
struct bSound;

void SEQ_sound_update_bounds_all(struct Scene *scene);
void SEQ_sound_update_bounds(struct Scene *scene, struct Sequence *seq);
void SEQ_sound_update(struct Scene *scene, struct bSound *sound);
void SEQ_sound_update_length(struct Main *bmain, struct Scene *scene);
```


## [blender/sequencer/SEQ_channels.h](https://github.com/blender/blender/blob/master/source/blender/blenkernel/BKE_sound.h)

### Line 14: Sequencer channels

```c++
struct Editing;
struct ListBase;
struct Scene;
struct SeqTimelineChannel;
struct Sequence;

struct ListBase *SEQ_channels_displayed_get(struct Editing *ed);
void SEQ_channels_displayed_set(struct Editing *ed, struct ListBase *channels);
void SEQ_channels_ensure(struct ListBase *channels);
void SEQ_channels_duplicate(struct ListBase *channels_dst, struct ListBase *channels_src);
void SEQ_channels_free(struct ListBase *channels);

struct SeqTimelineChannel *SEQ_channel_get_by_index(const struct ListBase *channels,
                                                    const int channel_index);
char *SEQ_channel_name_get(struct ListBase *channels, const int channel_index);
bool SEQ_channel_is_locked(const struct SeqTimelineChannel *channel);
bool SEQ_channel_is_muted(const struct SeqTimelineChannel *channel);
int SEQ_channel_index_get(const struct SeqTimelineChannel *channel);
ListBase *SEQ_get_channels_by_seq(struct ListBase *seqbase, const struct Sequence *seq);
```

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
