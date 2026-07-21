# 音乐文件整理

Last updated: 2026-07-21 CST

## Project location

`/Users/qiufeng/Documents/New project 2/Codex项目/进行中/音乐文件整理`

## Current state

- The project was formally moved out of the temporary `outputs/` inbox on 2026-07-21.
- The target library is the Windows music directory `H:\-中文流行-`.
- A read-only audit of 6,928 MP3 files has been completed.
- No online matching, tag write, rename, `apply`, or `restore` operation has been run.
- The project contains the Python tool, tests, deployment artifacts, and final read-only audit evidence.
- Post-migration Mac verification passed all 156 tests.
- A fresh Windows read-only batch `20260721-resume` confirmed the library is byte-for-byte unchanged at the manifest level from the 2026-07-17 baseline.
- Online matching completed without modifying the music library: 46 proposed writes, 34 unchanged, 6,205 review, and 643 skip across 6,928 MP3 files.
- The 46 proposed writes cover four albums and only fill missing track number, album artist, and disc number fields.
- A 20-group stratified review passed; the frozen plan remains unapproved for real-library writes.
- A three-file Windows C: copy-only pilot passed: 3/3 applied, 3/3 verified, 3/3 restored, with audio and non-target fingerprints unchanged. The final H: manifest still matches the baseline.

## Safety boundary

- Recheck the Windows host and music volume before resuming.
- Regenerate a current read-only manifest/audit before planning because the library may have changed since 2026-07-17.
- Generate and review a non-mutating online plan before any write operation.
- Records with read errors and their affected membership groups must not be written automatically.
- Do not run `apply` without explicit user approval of the frozen plan and pilot process.

## Next step

Wait for explicit user approval before modifying one real album on `H:`. Start with a single 10-track album, verify immediately, and do not expand scope without another decision.
