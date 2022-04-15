# Audaspace Related Specifications

### Main Structure

Audaspace is built within a specific concept of Hardware/software to be able to connect virtual audio players to sources and listeners. The buffer is the container that store data and send it to the devices.


### The following (probably incomplete) features are supported by audaspace:

- input/output devices: input from microphones, line in, etc., output devices including 3D audio support
- file reading/writing
- filters like low-/highpass and effects like delay, reverse or fading
- generators for simple waveforms like silence, sine and triangle
- channel count - channel remapping
- sample format - the library internally uses 32 bit floats
- sample rate - resampling
- simple (superposition, joining and ping-pong aka forward-reverse) and more complex (non-linear audio editing) sequencing of sounds

---

### Modules included

- Devices	Input and output from hardware devices
- Files	Input and output from files
- Effects	Effect classes
- Generators	Signal generator classes
- Plugins	Plugins and plugin management
- Respecification	Rechanneling, resampling and reformatting
- Sequencing	Simple and complex sequencing
- Utilities	(such as Buffer)

### Classes included

[ALL Classes](https://audaspace.github.io/annotated.html)

- Mixer Class [reference](https://audaspace.github.io/classMixer.html)


TO BE CONTINUED...
