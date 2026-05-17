# Volca Modular Patch Box

A single-file web app for drawing, saving, and *playing* patches for the **Korg Volca Modular**. Drag cables, twist knobs, hit ⏻ ON, and play it from your keyboard or the built-in step sequencer.

## Features

- Full vector recreation of the patching area, with four themes (device, dark, B&W, paper diagram)
- Drag-cable patching with snap-to-jack — cables route real audio/CV through Web Audio
- Signal-flow colour coding — audio red, CV blue, gates green
- **Built-in sound engine** with FM source, wavefolder, AHR + Rise-Fall envelopes, dual LPG, convolution reverb, compressor + saturation on the master bus
- **Step sequencer** below the patch area — 16 steps by default, expandable / shrinkable in 16-step jumps up to 64, or type any length 1–64 directly
- Scale-aware sequencer editing — Up/Down snaps the current step's pitch to the active scale and auditions it
- Floating instructions menu (Patching / Sequencer / Keyboard) — popover that never resizes the patch or sequencer area
- 7 scales, octave shifting, per-note microtuning
- Save patches by name with notes; export/import as JSON
- Print or export as PNG (one per patch, or all stacked into one)

## Sound engine

Hit **⏻ ON** in the header (top right). The engine is a Web Audio educational emulation: carrier + modulator triangle oscillators, frequency modulation, Buchla-style sin-fold wavefolding (oversampled), AHR / Rise-Fall envelopes normalled to LPG A so notes are percussive by default, sample-&-hold from pink noise, dual low-pass gates with coupled VCA + filter response, and a convolution reverb plus BBD-style slap delay for SPACE OUT. The master bus has a high-pass, dynamics compressor, and tanh saturation to keep things musical at loud settings.

The CLOCK knob sets the BPM range from ~56 to ~240 BPM and drives the sequencer tempo.

## Keyboard

**Playing notes**
- **A W S E D F T G Y H U J K …** — play notes (white & black keys, QWERTY piano)
- **Z / X** — octave down / up
- **3–9** — pick scale: Major, Dorian, Phrygian, Lydian, Mixolydian, Minor, Locrian
- **C** — back to Chromatic

**Sound shaping**
- **1** — toggle long-envelope mode (×3 attack/release)
- **2** — randomize per-note microtuning (each MIDI key gets its own random cents)
- **Shift+2** — clear microtuning back to 12-TET
- **0** — panic / silence modulation

**Sequencer**
- **Spacebar** — start / stop the sequencer (also wakes up the audio engine if it was off)
- **←** / **→** — move the cursor between steps
- **↑** / **↓** — pitch the current step up / down within the active scale (with current microtuning), plays a quick preview
- **−** — toggle the current step on / off (captures the most recent note played)
- **=** — insert a rest (silent step, advance cursor)
- **`** (backtick) — toggle live recording (or click the **REC** button)

## Sequencer

Sits below the patch area. Each step shows clearly whether it has a note:

- **Dim square** → step is off (no note will play)
- **Bright square with a yellow LED dot** → step is on and will play its assigned note
- **Cyan outline + cyan triangle above** → the cursor (your current edit position)

Click any step to toggle it on/off — it captures the most recent note you played. With the cursor on an active step, press any key to live-edit that step's note, or use ↑/↓ to snap up/down within the active scale. Hit **REC** (or `` ` ``) and play notes to fill steps live. **▶** starts/stops the cursor; **−16 / +16** shrink or grow the pattern; the **Len** input takes any value 1–64.

## Instructions menu

The bar below the sequencer has three tabs: **Patching**, **Sequencer**, **Keyboard**. Click one to pop up a floating help panel that overlays without resizing anything. Click the tab again or click anywhere outside the bar to dismiss it.

## Usage

1. Download `volca_patch_designer.html`
2. Open it in any modern browser
3. Patch away, hit ⏻ ON, press a key

No install, no server, no dependencies. To put it on the web just upload that single HTML file to any static host (Netlify, GitHub Pages, your own server). Patches live in your browser's `localStorage` — use **Export JSON** for real backups.

## Note

Not affiliated with Korg lol
