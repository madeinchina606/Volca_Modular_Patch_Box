# Gorka Modular — Patch Box

Recreation of the Gorka Modular-style synthesizer in your browser: drag cables, twist knobs, play it from the keyboard or the built-in step sequencer, and listen through a real Web Audio sound engine.

## Features

- Vector patching area in four themes (device, dark, B&W, paper diagram)
- Drag-cable patching with snap-to-jack and signal-flow colour coding (audio / CV / gate / mixed)
- Real-time sound engine: FM source with continuous RATIO, Buchla-style wavefolder, AHR + Rise-Fall envelopes, sample-and-hold, dual low-pass gates, convolution reverb + BBD-style delay, master HPF + compressor + saturation + makeup gain
- On-panel oscilloscope with **ON / OFF toggle** (save CPU when you don't need it)
- 1&ndash;64 step sequencer with **Bounce** (ping-pong) and **Stochastic** (probability + scale-aware pitch jitter) modes
- 28 scales: standard set (modes, pentatonics, blues, diminished, augmented, Japanese) plus 5 microtonal (19-TET, 24-TET, 31-TET, Bohlen-Pierce, Just Intonation) and 8 atonal (Messiaen modes 3&ndash;7, 12-tone row, tritone, clusters)
- Tonic C&ndash;B selectable; per-note microtuning randomization
- Three voice modes: Mono, Poly (6 light voices), Poly-Full (6 full FM voices, patches still apply)
- **Randomize** &mdash; random patch (skips volume) or random sequence in the active scale; keyboard shortcuts `[` patch, `]` sequence, `\` both
- **Save / Load patches** by name with optional group tags &mdash; create groups, filter by group, browse grouped or filtered views
- **Pack export / import** &mdash; bundle any selection of patches or whole groups into a single JSON pack file
- **MIDI** export / import for the sequencer (Standard MIDI File, preserves length)
- **WAV recording** &mdash; capture master output to a downloadable WAV (filename includes the current BPM)
- Export panel as PNG or print (single patch or multiple)

## Usage

1. Open `gorka_patch_designer.html` in any modern browser
2. Press **Enter** or click **&#9211; ON** in the top-right
3. Patch some cables, press a key, hit **Space** to start the sequencer

Click **Help &#9662;** in the header for the full in-app reference (Patching / Sequencer / Keyboard / Modules &amp; sound). It's a draggable popup so you can keep it open while you play.

To put it on the web, just upload the single HTML file &mdash; no install, no server, no dependencies. Patches live in `localStorage`; use **Export Pack** to back them up or share.

## Note

Not affiliated with anyone real. Gorka and Xorg are made up.
