# Unnamed Mod: **Initial** Project Bootstrap File

**Project:** Unnamed Mod  
**Status:** Not Started  
**Tracker:** MilkyTracker  
**Platform:** Linux / PikaOS  
**Target format:** 4-channel ProTracker MOD  

---

## Source-of-Truth Hierarchy

Use this hierarchy whenever records disagree:

1. **The auditioned project files are authoritative** for:
   - exact sample loop points
   - exact sample volumes
   - exact per-row volume edits
   - exact finetune values
   - any last by-ear edits
2. **The bootstrap file is authoritative** for:
   - project architecture
   - pattern roles
   - order list
   - note/rhythm/effect structure
   - final sample identities
   - tested status
3. The sample archives (currently ST-01 and ST-02) are only the source of the sample files.

---

## Primary Goal

Compose an original, classic, highly-polished 1990s-Amiga-game-style tune (`.mod`) using authentic **ProTracker 2** (PT2) constraints, ST-01/ST-02 samples, four channels and compact pattern reuse. Do not loop the composition; there should be a definite coda. The coda should not be a simple fade out but an interesting flourish instead.

The intended character of the piece is:

* industrial, dark electro, aggressive rhythm
* gritty, mechanical edge
* heavy on the pattern reuse
* interesting pattern order list
* musical influences: Brian Johnston, Paul van der Valk, Ray Norish
* unmistakably early-1990s tracker in construction
* 4 channels
* 64 rows per pattern

The `.mod` play length should be in the range of 240±15 seconds, but exact final runtime is not important. Musical flow, authenticity, and ProTracker compatibility matter more.

Since we're insisting on PT2 compatibility, there are to be no XM-only features.

New concept: use memories and learned lessons to automate this.

This might look difficult, but I know you can do it!

---

## All Steps

### 1. Select a title

Suggest ten possible titles which reflect the intended character as specified above. A title isn't strictly necessary, but having one helps keep the musical direction consistent. It gives the piece a little identity before pattern00 is even composed. The suggested titles should be short, evocative, and technical without being overly descriptive. Select your favourite title.

Using previously learned knowledge, assign an appropriate speed and beats-per-minute.

Output the candidates and the final winner as a Markdown file named `title.md`. Output the chosen speed and BPM as a Markdown file named `speed.md`.

### 2. Select a solid sample set

Using previously learned knowledge, select eight to ten samples from the ST-01 and ST-02 archives which will accomplish the goal and achieve the desired character for the `.mod`. State which samples are to be looped, if any. Using previously learned techniques, determine exact loop points and accept or reject samples for looping. Forward loops are the only kind of loops allowed per **ProTracker 2** compatibility rules.

Analyse the samples' envelopes and recommend default volume settings for each one. Note recorded peak and envelope behaviour. If you don't have access to the samples, report this lack and the user will upload the samples.

Since the source archives predate the finetune field, it is not relevant. Set finetune on all instruments to zero.

Lesson: Previous experiments with polyphonic instruments didn't go so well. As it turns out, chords are too hard in PT2. Until a mitigation is found for this, stick with instruments which can output only one note at a time.

Output selected sample set as a Markdown file named `samples.md`. Output loop data as a Markdown file named `loops.md`.

Generate note-range maps. Per **PT2** compatibility rules, only octaves 3-5 are allowed. Low-pitched samples should be restricted to octaves 4-5, and high-pitched samples should be restricted to octaves 3-4.

Output note-range maps as a Markdown file named `ranges.md`.

Suggest audition criteria for the samples. Output sample audition criteria as an addendum to `samples.md`.

**After the entire composition is complete**, the user will audition the sample set based on these criteria.

### 3. Write a structural arc and a motif map

The structural arc should be a narrative guiding the creation of patterns and their reuse in the order list. The structural arc springs forth from the name of the piece, which is our narrative and thematic 'seed'.

Each motif has a descriptive character. For example:

- Motif A: heartbeat kick + bass pulse
- Motif B: descending pad figure
- Motif C: metallic chime
- Motif D: chromatic tension figure

Then each pattern becomes a recombination of those motifs. Do not use this exact example in your motif map.

Output the structural arc and the motif map as a Markdown file named `motifs.md`.

### 4. Generate patterns

From the structural arc and the motif map, generate a pattern plan. This will dictate the number of patterns required and the pattern groups into which each pattern fits. It will also suggest a pattern order list. Pattern groups may have up to four members. Patterns may not be members of more than one group. Groups may be reused in the order list.

Output the pattern plan as a Markdown file named `plan.md`.

The first pattern group, the one containing `pattern00`, is the most important. It sets the tone of the entire piece, and is the sapling which will become our mighty oak. Compose it first.

Continue through the pattern groups. Compose an entire group at a time, to allow for phrases larger than one pattern.

Output each pattern with explanatory notes as a Markdown file named `patternNN.md`, where NN is a lowercase hex monotonic counter starting at 0x00. Patterns are numbered sequentially as they are composed. The pattern plan must match the counter. Adjust the plan if needed.

Suggest audition criteria for each pattern. Output pattern audition criteria as an addendum to its output Markdown file.

**After the entire composition is complete**, the user will audition the patterns based on these criteria.

### 5. Create the build package

Assemble the metadata file. The metadata file is in YAML format. Here is a **shortened** example based on *Clockwork Picnic*:

```
---
title: 'Clockwork Picnic'
speed: 6
bpm: 145
orderList:
  - 0x00
  - 0x01
  - 0x02
  - 0x03
  - 0x04
  - 0x01
  - 0x02
  - 0x05
instruments:
  - id: 1
    source: 'st02'
    name: 'ST-02/Pizza2'
    volume: 0x10
    finetune: 0x0
  - id: 2
    source: 'st01'
    name: 'ST-01/PanFlute'
    volume: 0x10
    finetune: 0x0
  - id: 7
    source: 'st01'
    name: 'ST-01/Strings7'
    volume: 0x20
    finetune: 0x0
    start: 0x00f0
    length: 0x25bc
  - id: 8
    source: 'st01'
    name: 'ST-01/PingBells'
    volume: 0x38
...
# vim: set filetype=yaml
```

This is just an example of the metadata structure. `title`, `speed`, `bpm`, `orderList` and `instruments` must all be present. The `orderList` numbers correspond to the pattern Markdown files. It is the order list from the pattern plan. The `instruments` are the sample set. `title`, `speed` and `bpm` are the values selected earlier. Construct and output this file as a YAML file named `song.yaml`.

Finally, create a tarball of all the Markdown files and `song.yaml`. Name the tarball after the song title and give it a revision number.

---

## Compatibility Rules

```text
4 channels only
ProTracker-compatible effects only
No XM-only composition features
No notes below C-3
No notes above B-5
Forward sample loops only
No ping-pong loops
Pattern reuse preferred
Exact final runtime is unimportant
```

Bonus points if the final `.mod` weighs in at less than 40KB, but this is a difficult goal.

## Arbitrary Guidelines

- All unpitched percussion hits written as note `C-4`.
- Unless otherwise specified or required, output lone numbers in hex format (eg. "3f").
- Explain effects the first time they're used.

## Tools Used

Testing Operating System: PikaOS
Testing Tracker: MilkyTracker
Pattern Compiler: ptgen

## Pattern Format

The patterns will not be entered into MilkyTracker directly. Instead, I have written a compiler for the final `.mod`. The compiler requires pattern rows in a specific format, as follows:

`| RR | NNN II EEE | NNN II EEE | NNN II EEE | NNN II EEE |`
where RR is the row number, NNN is the note, II is the instrument slot and EEE is the effect.

Row number must be in decimal, not hex. This is due to a bug in the compiler.

The row format is compatible with Markdown tables, so each pattern should have a Markdown table header. Headers should be 'Row', 'Ch1', 'Ch2', 'Ch3' and 'Ch4'.

Write no note as '---'. Write no instrument as '--'. Write no effect as '---'. Omit entirely empty lines. Instrument is a hex number, so for example you would output instrument 10 as "0A". Use only uppercase for hex numbers in II and EEE.
