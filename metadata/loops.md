# Loop decisions

Status: numerical seam search completed for KorgFilter; no listening test performed. No loops are selected in revision 02.

| ID | Sample | Decision | Loop start / length |
| --- | --- | --- | --- |
| 01 | BassDrum2 | One-shot percussion | Disabled |
| 02 | PopSnare1 | One-shot percussion | Disabled |
| 03 | CloseHiHat | One-shot percussion | Disabled |
| 04 | PopBass | Preserve finite envelope | Disabled |
| 05 | Leader | Preserve finite envelope | Disabled |
| 06 | KorgFilter | Finite stab; reject candidate loop for this draft | Disabled |
| 07 | SynClaves | One-shot percussion | Disabled |
| 08 | Cymbal2 | One-shot percussion | Disabled |
| 09 | SynBuz | Preserve finite envelope | Disabled |

The KorgFilter search compared even byte offsets and even loop lengths in the sustained body, using a 64-sample context comparison plus boundary value and slope penalties. Best candidate: byte start `04AE`, byte length `0278`, exclusive end `0726`. It has a one-unit endpoint difference, but the context RMS error is about 9.33 sample units against a body RMS around 24–26. Endpoint continuity alone does not establish a convincing musical loop. The candidate is not entered in metadata and is not approved for sustained use.

All positions above are byte offsets in the untouched raw source. A MOD header expresses repeat positions and lengths in words; do not copy byte numbers directly into header fields. ptgen's optional `start`/`length` semantics are not verified, and those fields are deliberately absent from `song.yaml` because all samples are one-shot. Verify disabled loops after compilation; a conventional MOD non-loop sentinel is not a musical two-byte repeat.

No ping-pong loops, reverse playback, envelope sustain or XM-only loop mechanism is used. If audition establishes that an original sample ending clicks, review the exact imported sample before deciding whether a source edit is needed.
