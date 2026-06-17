# Codex Memory Startup Rules

When the user says any of the following:

- 调用项目记忆
- 继续搭建 Codex Memory Repo
- 继续上次的 Codex 子代理项目
- 调用 Prompt Director
- 调用 Poster Director

Codex should first read this memory repo before doing creative or project work.

## Required Startup Read

1. Read `README.md`.
2. Read `changelog.md`.
3. Read the relevant files under `personas/`.
4. Read the relevant files under `people/`, `brands/`, and `pets/`.
5. Read active project files under `projects/active/`.
6. Read the relevant agent workflow under `agents/`.
7. Then begin the requested task.

## Default Agent Routing

- Use `agents/prompt_director.md` when the user gives a rough visual idea and needs a polished prompt.
- Use `agents/poster_director.md` when the user asks for posters, key visuals, T-shirt graphics, CrossFit visuals, or character posters.
- Use `agents/project_manager.md` when the task spans multiple steps, versions, exports, or machines.

## Safety Rules

Do not store or sync:

- API keys
- passwords
- cookies
- auth files
- `.env` values
- private tokens
- Codex session databases
- browser profiles
- OpenAI / GitHub / router credentials

Only store durable human-readable project context.
