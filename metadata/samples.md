# Sample set — Relay Fault, revision 02

Status: measured from the supplied archives; musical suitability, tuning and balance are provisional. No sample has been auditioned in this session.

Interpretation: headerless signed 8-bit mono PCM, consistent with the ST archive layout. The files contain no rate, tuning or loop metadata. This interpretation must be confirmed at import. Source bytes are preserved; no normalisation, trimming or retuning is applied. All finetunes are `00`.

| ID | Source | Role | Bytes (hex) | Peak / 128 | RMS by quarter (sample units) | DC mean | Default volume |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 01 | ST-01/BassDrum2 | Kick | 0BB8 | 127 / 128 | 41.2 / 29.4 / 6.6 / 2.5 | 0.98 | `38` |
| 02 | ST-01/PopSnare1 | Snare | 07D0 | 127 / 128 | 78.0 / 49.8 / 20.1 / 5.3 | 0.30 | `2C` |
| 03 | ST-01/CloseHiHat | Closed hat | 04B0 | 34 / 128 | 11.3 / 3.2 / 0.7 / 0.2 | 0.02 | `40` |
| 04 | ST-01/PopBass | Bass | 0A8C | 122 / 128 | 51.6 / 38.1 / 27.1 / 28.4 | 0.35 | `30` |
| 05 | ST-01/Leader | Lead | 0D48 | 127 / 128 | 48.7 / 30.0 / 12.4 / 2.0 | -0.04 | `24` |
| 06 | ST-01/KorgFilter | Filter stab | 0D48 | 86 / 128 | 22.3 / 26.3 / 25.0 / 24.3 | -0.06 | `20` |
| 07 | ST-01/SynClaves | Metallic tick | 03E8 | 127 / 128 | 46.1 / 11.8 / 4.3 / 1.5 | -0.16 | `20` |
| 08 | ST-02/Cymbal2 | Cymbal | 0CE4 | 128 / 128 | 68.8 / 40.6 / 10.8 / 3.4 | -0.25 | `20` |
| 09 | ST-02/SynBuz | Buzzer answer | 0E74 | 112 / 128 | 45.0 / 28.7 / 9.7 / 3.5 | -2.85 | `26` |

Peak/RMS/DC measurements above use decimal signal units for readability. Volumes are hexadecimal tracker values, with `40` the maximum. Defaults are starting balance choices, not loudness measurements. The closed hat is naturally much quieter than the snare; its full default level avoids needlessly attenuating it. Kick and bass have separate channels; snare shares the kick channel, so its onset intentionally replaces any kick tail.

- `01` ST-01/BassDrum2: Round low impact; leaves room for bass.
- `02` ST-01/PopSnare1: Strong attack with a cleanly decaying tail.
- `03` ST-01/CloseHiHat: Quiet source; full default level, with softer written accents.
- `04` ST-01/PopBass: Low recorded fundamental; use the upper permitted register.
- `05` ST-01/Leader: Decaying harmonic voice for breath-sized phrases.
- `06` ST-01/KorgFilter: Bright harmonic voice; use short, naturally decaying stabs.
- `07` ST-01/SynClaves: Treat as unpitched percussion throughout.
- `08` ST-02/Cymbal2: Accent and terminal strike, used sparingly.
- `09` ST-02/SynBuz: Low recorded voice, used in the upper permitted register.

## Suitability and loop decisions

All selected voices are treated as single-note instruments. The pitched candidates show harmonic series compatible with monophonic material; spectral analysis cannot prove the absence of a layered voice. No chord, arpeggiator effect or premixed chord sample is used.

No sample is looped. PopBass, Leader and SynBuz have usable attack-and-decay envelopes. KorgFilter has a sustained body but is assigned a finite stab role; its original end is not artificially sustained. Percussion remains one-shot. See `loops.md`.

Rejected alternatives: DXBass has mean DC about -81.34 sample units and does not give a trustworthy untreated bass source. BassDrum1 has a heavily saturated attack and mean DC about -13.68. Claps2 also has substantial DC and a near-flat noisy envelope; it is unnecessary alongside the selected snare. These are source-specific decisions, not judgements about similarly named samples in other archives.

## Audition criteria — after composition

- Solo each sample at every distinct trigger pitch listed in `ranges.md`; confirm signed PCM import, usable attack and absence of an accidental chord or unwanted buzz.

- Compare `04` PopBass against `05` Leader on nominal E and D, then `06` KorgFilter and `09` SynBuz. Confirm an octave-related pitch relationship. If beating is objectionable, report it; finetune remains zero under this brief.

- Check PopBass for end clicks or an unnaturally truncated tail, especially at E-5. Do not add a loop merely to make the waveform continuous.

- Check KorgFilter at E-3 and F-3 for a clean finite stab and reasonable decay; verify it is not unpleasantly shrill at these low trigger labels.

- Check kick/bass weight in stereo and mono; snare must cut through without making kick and bass seem quiet. Check that hat accents remain audible without hiss dominating.

- Check cymbal and tick for hard clipping, harshness and DC-like clicks. Source peak values alone do not establish audible clipping.

- Preserve any accepted by-ear edits in the auditioned project as authoritative. Return that exact project with notes before changing metadata defaults.
