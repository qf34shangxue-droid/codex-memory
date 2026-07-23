# 音乐文件整理

Last updated: 2026-07-23 CST

## Project location

`/Users/qiufeng/Documents/New project 2/Codex项目/进行中/音乐文件整理`

## Goal

Complete and normalize the six required MP3 tag fields, cross-check uncertain albums online, and archive readable files under `H:\标签已整理` using `artist-album` directories with frozen plans and rollback evidence.

## Final state

- `H:\标签已整理` contains 6,926 readable MP3 files, 103,385,467,413 bytes, and 825 album directories.
- Missing required fields: 0. Unknown title/artist placeholders: 0. Generic `Track01`-style titles: 0. Malformed track/disc fractions: 0.
- The final correction round updated 142 files; all 142 passed post-write reread verification.
- 111 affected files were internally relocated to their corrected `artist-album` directories; all 111 passed full-file fingerprint and tag verification with no overwrite.
- Final evidence: `windows-run-20260722-organize/final-quality-v2/` and `windows-run-20260722-organize/final-audit-v4/`.
- Final report: `windows-run-20260722-organize/FINAL_REPORT_FINAL.md`.
- Fresh tests: Mac 224/224 passed; Windows 224 passed with 2 expected ffmpeg skips.

## Cross-check sources

- Apple Music/iTunes, MusicBrainz, Spotify, JOOX, Qobuz, record-label pages, retailer catalogs, and original CUE metadata were used in combination.
- The Teresa Teng 1977 Shimbashi release was identified by CUE barcode `4988005165978` and checked against MusicBrainz, Rakuten Books, Suruga-ya, and Qobuz.
- Li Chien-fu's `柴拉可汗` was checked against JOOX, Five Music, and the National Museum of Taiwan History catalog.

## Unrepairable source/audio exceptions

- Two files remain in `H:\-中文流行-` because they have no valid MPEG audio header: one is 0 bytes and one is 87 bytes.
- 181 organized files have complete readable tags but no measurable duration: 180 are approximately 2 KB tag-only placeholders inherited from the source set; one is an 8,922,906-byte duration-unreadable file.
- These are audio-payload defects, not missing tags. Audio data was not fabricated or rewritten.

## Next step

The tag organization project is closed. Audio repair or replacement of the 183 payload-level exceptions requires a separate user-approved project because it would modify audio content.
