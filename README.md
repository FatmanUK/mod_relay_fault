# Build and audition handoff

This package is a complete ptgen source draft, revision 02. It contains all composition Markdown files and `song.yaml`, plus numerical provenance and checksums. It does not contain a compiled or auditioned MOD.

Use the supplied ST-01 and ST-02 archives as ptgen's sample sources without renaming the files. The YAML uses source keys `st01` and `st02` and exact names such as `ST-01/PopBass` and `ST-02/SynBuz`, following the bootstrap dialect. Use your established ptgen invocation; no unverified command line is prescribed here.

Before accepting compilation, check the actual output is a four-channel MOD, that all twelve patterns contain 64 logical rows, and that its order list matches `song.yaml`. Confirm instrument defaults, zero finetunes, untouched sample bytes and disabled loops. Verify this project's C-3…B-5 trigger labels map to the expected classic three-octave period range.

The [official MilkyTracker manual](https://milkytracker.org/docs/manual/MilkyTracker.html) documents F00 as stopping playback. This supports the chosen terminal command; it does not establish that the actual generated file has been tested. Check the final pattern in the user's exact MilkyTracker version and replay mode. Verify it stops after the flourish without starting pattern00 again.

Follow the sample and per-pattern audition criteria, then the distinct boundary list in `validation.md`. Full-track acceptance is a separate final step. Keep edits in the actual auditioned project, and send that exact file back with your notes. The project hierarchy makes those by-ear sample and volume edits authoritative.

## Source archive identity

- `st-01.tar.gz` SHA-256: `34feb17a5130d5e45c032d28af04a9d9b6e6ef369316a203bd0df4ed4e3450ed`.
- `st-02.tar.gz` SHA-256: `39d170f7aa9a85e4ecefdd9221cc381567b886dd78060bac93c6668099bc0538`.
