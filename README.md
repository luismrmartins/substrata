# substrata

A browser-based dub-techno track generator. Single-file HTML app with a Web Audio synth, drum, bass, lead, chord, mic, and granular engine, plus mixing/effects/recording.

Open `sequencer.html` to use it. Or visit the deployed Vercel URL.

## Channels

- **Drum** — switchable voice (kick / snare / clap / hat / open-hat / ride / crash / toms / clave)
- **Bass** — three-osc (sub + sine + saw/square), 24 dB low-pass, ADSR, LFO with multi-destination
- **Synth (Lead)** — Prophet-5-flavoured dual-osc, 24 dB lowpass with own ADSR + amp ADSR + LFO
- **Chord** — polyphonic Prophet-5, per-step degree (I–VII) and quality, scale-aware
- **Mic** — live mic capture (device-selectable) or tab audio, 8-band parametric EQ, HPF, input gain, live waveform
- **Granular** — sample player with truncation, play marker, length, loop, and LFO-modulated play position

## Per-track

Mute, solo, arm, randomise, duplicate, mute-groups (G1–G8), per-step velocity + pan, per-track swing, track-level LFO (vol + auto-pan).

## Master

EQ, warmth, compressor, ducker (per-track receive amount, source-channel sidechain).

## Effects

Delay (with tempo sync), reverb, chorus, flanger, bitcrush.

## Mixer

Two-deck audio mixer with crossfade, per-deck EQ; accepts audio files **and** project `.json` files (renders the project loop offline into the deck).

## Recording

- `● Rec` in the transport records the master output and downloads it.
- If a project folder is set via `📁 Folder` (Chrome / Edge), recordings save into `<folder>/exports/` and granular samples save into `<folder>/samples/`.
- `Save` / `Load` use JSON; with a project folder, granular sample files are restored on load.

## Modes

- **Track** tab — full per-channel view.
- **Mix** tab — compact list with just M / A / S / R / D / G× / × per channel. Mute/arm changes in Mix mode are deferred to each track's next downbeat.

## Themes

Light / dark toggle (`☼` / `☾`), full-screen toggle (`⛶`). Theme persists in `localStorage`.
