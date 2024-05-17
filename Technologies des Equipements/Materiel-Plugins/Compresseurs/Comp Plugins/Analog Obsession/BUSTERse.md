---
Date: 2024-01-07
Type: note de plugin
Genre de plugin: compresseur
Concepteur: Analog Obsession
tags:
  - musique
  - logiciel
  - plugin
  - compresseur-audio
---
# BUSTERse
Here is big brother of "BUSTER" with tons of improvements and new features!

Classic console compressor with extra Filter and Transient sidechain options to dominate whole signal!

Emulation du [[SSL Quad Master Bus]] 
[[Type de Compresseurs#VCA (Voltage Control Amplifier)|VCA]] 

**FEATURES**
STEREO COMPRESSOR : Compressor Section
FLT : Filter Section
TR : Transient Section
CONTROL : Control section
**Compressor Section**

- THRESHOLD (dB) : +15 to -15
- ATTACK (ms) : 0.1, 0.3, 1, 3, 10, 30
- RELEASE (sec) : 0.1, 0.3, 0.6, 1.2, Auto
- RATIO : 1.5, 2, 3, 4, 5, 10
- MAKE UP (dB) : 0 to 15
- MIX (%) : DRY to WET

**Filter Section (Sidechain)**

- HPF (Hz) : 20 to 500
- MID (~1500Hz) : -6dB to +6dB
- HF (~10kHz) : 0dB to -10dB *Will work like famous optical-tube compressor and help you to control high frequencies, better.

**Transient Section (Sidechain)**

- BOOST (dB) : 0 to 10 *While boosting attack, it will reduce decay/release of signal to make compressor more sensitive with only attacks/peaks.
- TILT (~1kHz Center) : -6dB to 6 dB *It's placed before BOOST to send only dedicated range to BOOST. So, BOOST will affect only given frequency range and will boost only this range's transients. If TILT is default, BOOST will affect overall transients.
- MIX (%) : DRY to WET *Will blend DRY and WET signal. After boosting transients, you can blend with DRY signal to keep reduced release of signal. When MIX in default position, TR is off. So, you can turn MIX knob to all the way up to engage TR section.

>[!note]
>EXT (External Sidechain) : When you engage EXT, sidechain circuit will listen incoming signal and you can stil use Filter and Transient sections on incoming signal.

**Control Section**

- MAIN : General Bypass
- TURBO : Turbo Mod *Turbo mod will help to compressor to affect whole signal range. Otherwise, compressor will focus on mid frequencies. This mod added to keep original sign of hardware.
- XFORMER : In/Out Transformers *If you engage XFORMER, in/out ICs will be replaced with transformer to balance it. This will affect to impedance, character, overall sound.

- ANALOG OBSESSION label is oversampling. Simply click it and engage 4x oversampling.
- Touchscreen support
- Resizable interface. Simple "Bottom Right Corner Handle" to resize. 50% to 200%.