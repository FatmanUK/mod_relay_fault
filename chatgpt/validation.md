# Static validation — revision 02

PASS: all twelve emitted pattern tables parse under the requested dialect: four cells, decimal rows 00–63, uppercase instrument/effect hex, no entirely empty rows, unique ordered row indices and correct empty tokens. Omitted rows are logical empty rows in a 64-row pattern.

PASS: YAML has all five required top-level fields, nine existing source identities and only defined pattern references. All finetunes zero; no loop metadata is enabled.

PASS: written notes obey C-3…B-5, per-instrument register restrictions and C-4-only unpitched percussion. Effect whitelist is Cxx, EC4, F06, F84 and terminal F00. No XM features or musical restart jump appear.

PASS: all groups have three members and no shared membership. The terminal pattern occurs once at the last order position; F00 occurs once at its final row.

| ID | Actual trigger subset |
| --- | --- |
| 01 | C-4 |
| 02 | C-4 |
| 03 | C-4 |
| 04 | A-5 B-5 C-5 D-5 E-5 F-5 G-5 |
| 05 | A-4 B-4 C-4 D-4 E-4 F-4 G-4 |
| 06 | C-3 D-3 E-3 F-3 |
| 07 | C-4 |
| 08 | C-4 |
| 09 | A-5 B-5 D-5 E-5 G-5 |

Distinct order boundaries: 00→01, 01→02, 02→03, 02→06, 03→04, 04→05, 05→00, 05→06, 06→07, 07→08, 08→00, 08→03, 08→06, 08→09, 09→0a, 0a→0b.

Parsed populated rows: 579 decimal. Theoretical full-order duration: 240.000 seconds. Standard MOD size estimate: 37,072 bytes (36.20 KiB). Sample bytes: 23,700. These are calculations, not compiled measurements.

## Pending checks

- ptgen compilation: not run; compiler not supplied. Exact Markdown ingestion, source routing, note periods and disabled-loop encoding need verification.
- Independent MOD parsing: pending an actual compiled MOD.
- Sample import/tuning/balance auditions: pending.
- Individual pattern and group auditions: pending.
- All listed boundary auditions, F00 stopping behaviour and no-restart check: pending.
- Full-track musical acceptance, actual duration and actual file size: pending.

No static pass is a playback or musical acceptance claim.
