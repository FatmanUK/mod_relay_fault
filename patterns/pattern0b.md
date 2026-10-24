# Pattern 0b — Terminal switching flourish

Group D. Tonal root E; 64 logical rows. Status: complete source draft, unauditioned.

Cxx sets immediate volume; EC4 cuts on tick four. These commands are explained first in `pattern00.md`.
F00 requests a ProTracker stop on final row 63. Player-specific handling remains a required boundary test. Row 60 silences all channels after the last strike; this is an articulated end following a flourish, not a gradual fade.

Channel roles: Ch1 kick/snare; Ch2 bass; Ch3 lead/buzzer replies; Ch4 filter, hat and metallic accents. Phrase boundaries are explicit; no held-note dependency is required for a later reuse.

| Row | Ch1 | Ch2 | Ch3 | Ch4 |
| --- | --- | --- | --- | --- |
| 00 | C-4 01 C38 | E-5 04 --- | --- -- --- | E-3 06 C20 |
| 02 | --- -- --- | --- -- --- | E-4 05 C24 | --- -- --- |
| 03 | --- -- --- | E-5 04 --- | --- -- --- | --- -- --- |
| 04 | C-4 02 C2C | --- -- --- | --- -- --- | --- -- --- |
| 06 | --- -- --- | B-5 04 EC4 | G-4 05 C20 | C-4 03 C40 |
| 07 | C-4 01 C30 | --- -- --- | --- -- --- | --- -- --- |
| 08 | C-4 01 C38 | E-5 04 --- | --- -- --- | C-4 03 C28 |
| 10 | C-4 01 C30 | --- -- --- | B-4 05 C20 | C-4 03 C40 |
| 11 | --- -- --- | G-5 04 --- | --- -- --- | --- -- --- |
| 12 | C-4 02 C2C | --- -- --- | --- -- --- | C-4 03 C28 |
| 14 | --- -- --- | E-5 04 EC4 | --- -- --- | C-4 03 C40 |
| 15 | --- -- --- | --- -- --- | --- -- C00 | --- -- --- |
| 16 | C-4 01 C38 | B-5 04 --- | --- -- --- | C-4 03 C28 |
| 18 | --- -- --- | --- -- --- | D-4 05 C24 | C-4 03 C40 |
| 19 | --- -- --- | E-5 04 --- | --- -- --- | --- -- --- |
| 20 | C-4 02 C2C | --- -- --- | --- -- --- | C-4 03 C28 |
| 22 | --- -- --- | G-5 04 EC4 | B-4 05 C20 | C-4 03 C40 |
| 23 | C-4 01 C30 | --- -- --- | --- -- --- | --- -- --- |
| 24 | C-4 01 C38 | E-5 04 --- | --- -- --- | C-4 03 C28 |
| 26 | C-4 01 C30 | --- -- --- | G-4 05 C20 | C-4 03 C40 |
| 27 | --- -- --- | D-5 04 --- | --- -- --- | --- -- --- |
| 28 | C-4 02 C2C | --- -- --- | --- -- --- | C-4 03 C28 |
| 30 | --- -- --- | B-5 04 EC4 | --- -- --- | C-4 03 C40 |
| 31 | --- -- --- | --- -- --- | --- -- C00 | C-4 07 C18 |
| 32 | C-4 02 C2C | E-5 04 EC4 | E-4 05 C24 | --- -- --- |
| 34 | --- -- --- | --- -- --- | --- -- --- | C-4 07 C20 |
| 38 | C-4 02 C2C | B-5 04 EC4 | G-4 05 C20 | --- -- --- |
| 40 | --- -- --- | --- -- --- | --- -- --- | C-4 07 C20 |
| 43 | C-4 02 C2C | --- -- --- | --- -- --- | --- -- --- |
| 44 | --- -- --- | E-5 04 EC4 | B-4 05 C20 | --- -- --- |
| 45 | --- -- --- | --- -- --- | --- -- --- | C-4 07 C20 |
| 46 | --- -- --- | --- -- --- | A-4 05 C24 | --- -- --- |
| 47 | C-4 02 C2C | G-5 04 EC4 | --- -- C00 | --- -- --- |
| 48 | --- -- --- | --- -- --- | G-4 05 C20 | --- -- --- |
| 49 | --- -- --- | --- -- --- | --- -- --- | C-4 07 C20 |
| 50 | C-4 02 C2C | B-5 04 EC4 | E-4 05 C20 | --- -- --- |
| 54 | C-4 01 C38 | E-5 04 --- | E-4 05 C28 | C-4 08 C20 |
| 58 | C-4 07 C18 | --- -- --- | --- -- --- | --- -- --- |
| 59 | --- -- --- | --- -- --- | --- -- --- | C-4 07 C10 |
| 60 | --- -- C00 | --- -- C00 | --- -- C00 | --- -- C00 |
| 61 | --- -- --- | --- -- --- | --- -- C00 | --- -- --- |
| 63 | --- -- F00 | --- -- --- | --- -- --- | --- -- --- |

## Audition criteria

- Check the full phrase at song tempo: bass weight, snare placement, clear melodic answer and deliberate rests. Confirm that channel sharing makes sense instead of sounding like accidental sample stealing.
- Listen to filter-to-hat handoffs and melodic cut rows for clicks or abruptly lost notes. Check bass tail against the next attack at every EC4 gate.
- Compare both internal sixteen-row transitions and the preceding/following patterns at each order-list occurrence. Judge the complete three-pattern group before making isolated edits.
- Hear the ratchet as a deliberate acceleration into the final E hit. Confirm the last tails have enough room before row 60 silence. Verify F00 actually stops and does not restart the order list in MilkyTracker.
