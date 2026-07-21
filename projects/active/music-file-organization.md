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

## Safety boundary

- Recheck the Windows host and music volume before resuming.
- Regenerate a current read-only manifest/audit before planning because the library may have changed since 2026-07-17.
- Generate and review a non-mutating online plan before any write operation.
- Records with read errors and their affected membership groups must not be written automatically.
- Do not run `apply` without explicit user approval of the frozen plan and pilot process.

## Next step

Confirm Windows and `H:` availability, rerun the read-only inventory, then continue with online matching and a review-only change plan.

