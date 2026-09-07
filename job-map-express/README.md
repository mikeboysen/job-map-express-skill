# Job Map Express — Agent Skill

Installable Agent Skill (`SKILL.md`) that runs the **Job Map Express** method in chat: job map, success metrics (outcomes), and follow-on analysis — with **mandatory prompts for missing inputs**.

## Install (Cursor)

See the repo root `README.md`, or copy this folder to:

- `.cursor/skills/job-map-express/` (project), or
- `~/.cursor/skills/job-map-express/` (user; turn on Sync Skills for Cloud Agents if needed)

Repo: `https://github.com/mikeboysen/job-map-express-skill`

Invoke with `/job-map-express` or ask naturally (“build a job map for…”).

For the full capability list: `/job-map-express help`.

## What it does

- Interviews for required scenario fields when missing
- Builds a MECE job map on Define→Conclude phases
- Writes outcome-style success metrics (PJTBD format)
- Optional: root causes and solution approaches

## What it does not do

- Does not publish to OpenAI or Anthropic surfaces
- Does not replace the Job Map Express web app (no hosted save without MCP)

## License

PolyForm Shield 1.0.0 — see `LICENSE` and `NOTICE`.
