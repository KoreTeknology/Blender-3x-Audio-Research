## Project: Blender 3x Audio upgrades

The project is to study the possible implementation of new audio features in Blender 3 Releases. 

### Objectives: Add audio features (EQ, Compressor, limiter, vu-meter, gain stagging, mix, ...)

Features (preview):
- Audio strip in sequencer with edition capabilities
- Audio panel (N) with editing features
- Audio nodes per channel
- 2 sets of audio data: per strip/master

---

# EQs

About the EQ, we have here many options:

tri-bands (fixed freqs*) with gain (what i see here in your proposal)
Single parametric band (very used in studio mastering)
up to 12 bands (fixed freqs)
tri-bands parametric (most common type)
etc…
i would like to give some infos about the fixed bands EQ in case of tri-bands selection:

20Hrz > 500Hrz (-15/+15db)
200Hrz > 5kHrz (-15/+15db)
800Hrz > 20kHrz (-15/+15db)
As well as the gain for that frequencies range, we should have a Q (curve shape for each band), i didnt try with audaspace if the Q will be a constant value, but we can look at.


---

# Vu-meter




