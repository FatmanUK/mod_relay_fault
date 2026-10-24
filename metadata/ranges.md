# Trigger-register map

Status: provisional analytical register allocation. Trigger labels use the brief's C-3…B-5 convention. Check ptgen's label-to-period mapping before trusting playback pitch.

| ID | Sample | Permitted triggers | Used triggers in this revision | Reason |
| --- | --- | --- | --- | --- |
| 01 | BassDrum2 | C-4 only | C-4 | Unpitched percussion convention |
| 02 | PopSnare1 | C-4 only | C-4 | Unpitched percussion convention |
| 03 | CloseHiHat | C-4 only | C-4 | Unpitched percussion convention |
| 04 | PopBass | C-4…B-5 | C-5 D-5 E-5 F-5 G-5 A-5 B-5 | Low recorded bass, restricted to upper trigger octaves |
| 05 | Leader | C-3…B-4 | C-4 D-4 E-4 F-4 G-4 A-4 B-4 | Mid/high melodic role |
| 06 | KorgFilter | C-3…B-4 | C-3 D-3 E-3 F-3 | Bright source; low triggers tame its register |
| 07 | SynClaves | C-4 only | C-4 | Metallic unpitched accent |
| 08 | Cymbal2 | C-4 only | C-4 | Unpitched percussion convention |
| 09 | SynBuz | C-4…B-5 | D-5 E-5 G-5 A-5 B-5 | Low source raised for a short answering voice |

The used-trigger column lists the exact subset actually written; it is also reproduced in the static report. No pitches outside the per-sample permitted register may appear.

## Provisional tuning evidence

At a hypothetical C-4 playback period of 428 and PAL sample clock near 3.547 MHz, playback rate is about 8287 samples/second. A windowed spectrum of the source body gives PopBass a fundamental near 32.37 Hz (with a stronger second harmonic near 65 Hz), and Leader a fundamental near 130.62 Hz. These support C-related source roots separated by approximately two octaves. PopBass at E-5 is therefore expected to sit roughly an octave below Leader at E-4.

KorgFilter has a strong component near 524.77 Hz with weaker components near 262 Hz and its multiples; do not mistake the strongest component for an unrelated note. SynBuz autocorrelation supports a roughly 127-sample period, consistent with a C-related low voice. Slow envelope changes and short windows limit these estimates. No tuning claim is audition-confirmed, and no finetune correction is applied.

After compilation, confirm that the lowest legal label C-3 maps to period 856 and highest B-5 to period 113 under this project's octave convention. These are compatibility expectations to check against ptgen, not evidence that the compiler has already been tested.
