# Codex Memory Repo

This repo stores long-term collaboration memory shared by Codex sessions on different Macs.

## How To Use

When starting a long-running design, writing, courseware, or personal project, ask Codex:

```text
调用项目记忆，先读取 codex-memory，再继续这个项目。
```

Codex should first read the relevant files in this repo, then work from the stored project context, visual preferences, people, brands, assets, and prompt patterns.

## Folder Map

- `SYSTEM.md`: startup rules for loading this memory repo.
- `agents/`: reusable sub-agent workflows such as Prompt Director, Poster Director, and Project Manager.
- `personas/`: recurring creative systems, series, and project personalities.
- `people/`: people or character references used in visual and narrative projects.
- `brands/`: brand, team, organization, or identity systems.
- `pets/`: pet profiles and visual reference notes.
- `projects/`: active, completed, and archived project records.
- `prompts/`: reusable prompt patterns for posters, T-shirts, infographics, and other outputs.
- `changelog.md`: memory updates and structural changes.

## GitHub Sync Plan

Recommended repo name:

```text
codex-memory
```

Recommended visibility:

```text
Private
```

Mac mini and MacBook should use the same private GitHub repo. Before working, pull the latest memory. After meaningful updates, commit and push. On the other machine, pull again before continuing.

## Safety Rules

Do not store secrets here.

Never save:

- API keys
- passwords
- cookies
- auth files
- `.env` values
- private tokens
- Codex session databases
- browser profiles

Use this repo for durable human-readable context only.
