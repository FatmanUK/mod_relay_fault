# Pattern plan and order list

Revision 02: complete source draft; static validation only. Groups each contain three patterns, forming twelve-bar phrases under the four-rows-per-beat interpretation. All group memberships are exclusive.

| Group | Patterns | Role |
| --- | --- | --- |
| A | 00 01 02 | Complete initial state and recurring mechanical identity |
| B | 03 04 05 | C–D–E transfer, broader melody |
| C | 06 07 08 | E–F–E pressure state |
| D | 09 0a 0b | C–D–E terminal phrase; used once |

Group order: A B A C B C A B C C D. The adjacent final C repetitions are deliberate insistence before the one-time terminal group. No breakdown-and-rebuild section is inserted.

| Order position (hex) | Pattern |
| --- | --- |
| 00 | 00 |
| 01 | 01 |
| 02 | 02 |
| 03 | 03 |
| 04 | 04 |
| 05 | 05 |
| 06 | 00 |
| 07 | 01 |
| 08 | 02 |
| 09 | 06 |
| 0A | 07 |
| 0B | 08 |
| 0C | 03 |
| 0D | 04 |
| 0E | 05 |
| 0F | 06 |
| 10 | 07 |
| 11 | 08 |
| 12 | 00 |
| 13 | 01 |
| 14 | 02 |
| 15 | 03 |
| 16 | 04 |
| 17 | 05 |
| 18 | 06 |
| 19 | 07 |
| 1A | 08 |
| 1B | 06 |
| 1C | 07 |
| 1D | 08 |
| 1E | 09 |
| 1F | 0a |
| 20 | 0b |

Thirty-three full 64-row positions at speed `06`, BPM `84` give about 240 seconds before stop-command/player timing nuances. Twelve distinct patterns use `3000` hex pattern bytes. Selected raw samples total `5C94` hex bytes; standard MOD layout estimate is 37,072 bytes, under 40 KiB, if the compiler copies the samples unchanged and emits exactly these patterns. Confirm actual file size after ptgen compilation.

Pattern `0b` has a composed final flourish, silence preparation on row 60, and `F00` on row 63. `F00` is the proposed ProTracker stop command. Its handling must be checked in ptgen, MilkyTracker and the intended replay mode. Some replay software treats this differently; the non-repeating ending is not yet playback-confirmed. There is no Bxx restart jump or musical self-loop.

## Boundary checks after compilation

Test every distinct adjacent pair in the order list, including 02→03, 05→00, 02→06, 08→03, 05→06, 08→00, 08→06 and 08→09. The static report gives the complete deduplicated list. Confirm handoffs replace preceding tails cleanly, the short lead phrases breathe and repeated group A sounds like a return at full strength. Test 0a→0b and the final stop separately.
