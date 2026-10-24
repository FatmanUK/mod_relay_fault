# Speed and tempo

Status: selected starting settings; musical suitability remains unauditioned.

| Setting | Value | Meaning |
| --- | --- | --- |
| Speed | `06` hex | Six ticks per row. |
| BPM | `84` hex = 132 decimal | Initial tempo. |

This is a composition choice based on the brief, not a recovered setting from an earlier project. It gives the mechanical rhythm weight while retaining room for busy percussion and short melodic responses.

When effects are needed, `F06` sets speed to six ticks per row; `F84` sets tempo to 132 BPM. Both are ProTracker effects. Initialisation must agree with `song.yaml` and use separate channel effect fields if both commands appear on one row.

At constant speed and tempo, one row lasts 6 × 2.5 / 132 seconds; one full 64-row pattern lasts approximately 7.273 seconds. Thirty-three full pattern plays total 240 seconds. This is a planning budget, not an order list or a measured playback duration; breaks, delays and later tempo changes would affect the result.

The final coda must also have an explicit compatible stopping strategy verified with ptgen and MilkyTracker. Reaching the end of an order list alone must not be assumed to prevent player restart.
