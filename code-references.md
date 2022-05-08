# Code References (Blender Sources)

- **Sound Operators** [Repository](https://github.com/blender/blender/tree/master/source/blender/editors/sound)
- **Sound Strip** [SEQ_sound.h](#blendersequencerseq_soundh)
- **Sequencer channels** [SEQ_channels.h](#blendersequencerseq_channelsh)
- **Blender Kernel** [BKE_sound.h](#blenderblenkernelbke_soundh)

:speech_balloon: [Diff VSE](https://developer.blender.org/D14412)

---

## Repository

- :open_file_folder: **extern/audaspace/**
  - :page_facing_up: [*AUD_Device.cpp*]()        :speech_balloon: Notes:
  - :page_facing_up: [*AUD_Sequence.h*]()
  - :page_facing_up: [*AUD_Sequence.cpp*]()
- :open_file_folder: **config/**
  - :page_facing_up: [*Audaspace.h.in*]()
- :open_file_folder: **include/**
  - :open_file_folder: **fx/**
  - :open_file_folder: **sequence/**
    - :page_facing_up: [*SequenceEntry.h*]()
  - :open_file_folder: **util/**
    - :page_facing_up: [*FFTPlan.h*]()
- :open_file_folder: **src/**
  - :open_file_folder: **fx/**
    - :page_facing_up: [*VolumeReader.h*]()
  - :open_file_folder: **sequence/**
    - :page_facing_up: [*SequenceEntry.cpp*]()
    - :page_facing_up: [*SequenceHandle.h*]()
    - :page_facing_up: [*SequenceHandle.cpp*]()
  - :open_file_folder: **util/**
    - :page_facing_up: [*FFTPan.cpp*]()
- :open_file_folder: **releae/scripts/startup/bl_ui/**
  - :page_facing_up: [*space_sequencer.py*]()
- :open_file_folder: **source/blender/**
  - :open_file_folder: **blenkernel/**
    - :page_facing_up: [*BKE_sound.h*]()
    - :open_file_folder: **intern/**
      - :page_facing_up: [*sound.c*]()
  - :open_file_folder: **editors/space_sequencer/**
    - :page_facing_up: [*sequencer_intern.h*]()
    - :page_facing_up: [*sequencer_modifier.c*]()
    - :page_facing_up: [*sequencer_ops.c*]()
  - :open_file_folder: **makesdna/**
    - :page_facing_up: [*DNA_sequence_type.h*]()
  - :open_file_folder: **makesdna/intern/**
    - :page_facing_up: [*rna_sequencer.c*]()
  - :open_file_folder: **sequencer/**
    - :page_facing_up: [*SEQ_sequencer.h*]()
    - :page_facing_up: [*SEQ_sound.h*]()
      - :open_file_folder: **intern/**
        - :page_facing_up: [*sequencer.c*]()
        - :page_facing_up: [*sound.c*]()


---

## :bookmark_tabs: [blender/sequencer/SEQ_sound.h](https://github.com/blender/blender/blob/master/source/blender/sequencer/SEQ_sound.h)

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

---

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

---

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
---

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

---

in Specification.h (Audaspace)

 enum Channels
 {
     CHANNELS_INVALID    = 0,    
     CHANNELS_MONO       = 1,    
     CHANNELS_STEREO     = 2,    
     CHANNELS_STEREO_LFE = 3,    
     CHANNELS_SURROUND4  = 4,    
     CHANNELS_SURROUND5  = 5,    
     CHANNELS_SURROUND51 = 6,    
     CHANNELS_SURROUND61 = 7,    
     CHANNELS_SURROUND71 = 8 
 };
 
 enum Channel
 {
     CHANNEL_FRONT_LEFT = 0,
     CHANNEL_FRONT_RIGHT,
     CHANNEL_FRONT_CENTER,
     CHANNEL_LFE,
     CHANNEL_REAR_LEFT,
     CHANNEL_REAR_RIGHT,
     CHANNEL_REAR_CENTER,
     CHANNEL_SIDE_LEFT,
     CHANNEL_SIDE_RIGHT,
     CHANNEL_MAX
 };

