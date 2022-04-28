[< Back to Homepage](/../..)

---

## Development Strategy and Methodology

Keeping in mind that we are **NOT** making Blender looking like a **Digital Audio workstation DAW**, we want to focus on the most relevant audio processing implementation to support the users tasks during Animation and Movie production. My approach is to look at the fundamental audio settings and preferences before going further. At this very beginning stage, a more **advanced preferences panel** is necessary. 

I also consider any changes from the user´s point of view. **A discrete implementation with "no forced settings" is requested**. As long as the user doesn´t look for Audio mixing features and its usage, the default audio setup will apply.

**The final decision was made, regarding 3 focused developments agendas:**
- Preferences and Default Sound Mixer Setup (from 1 to 16 output channels)
- Sequencer Sound Strip Properties and Operators (Mix Bus and Modifiers)
- Advanced Mixer Setup within a new Editor space (Complex routing/Processing)


### :speaker: Known Audaspace capabilites

Audspace is a strong C++ Audio library, it includes a wide variety of Audio procesing features (See Audaspace Modules and Classes). We can identify thoses modules in different categories:
- Device
- Generators
- Inputs/Outputs
- Effects
- Mixer
- ...


### :speaker: Multiplex Audio Routing

### :speaker: Basic to Complex

### :speaker: Soundcards and Drivers

### :speaker: Audio Channels and Outputs

### :speaker: Mixer Component

### :speaker: Bus Component
