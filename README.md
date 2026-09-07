# Job Map Express — Agent Skill
From the creator of the Jobs-to-be-Done Masterclass -- the original prompting that leveraged early AI to replace expensive consulting theater in the JTBD world. If it's not good enough (it's actually better) than just tweak it. There are no **Gods** in Jobs-to-be-Done. Only egos.

Installable [Agent Skill](https://agentskills.io) (`SKILL.md`) that runs the **Job Map Express** method in chat: job maps, success metrics, related jobs, situational factors, social/emotional jobs, financial metrics, solution approaches, root causes, and consumption jobs.

This repo is the **GitHub install source**. Copy the `job-map-express/` folder into your agent’s skills directory (paths below). It is **not** a listing in the OpenAI or Anthropic marketplaces — install is from this repository.

License: **PolyForm Shield 1.0.0** (see `LICENSE` + `NOTICE`). Competing Use is prohibited. Trademarks reserved.

---

## What you get

| Capability | Example ask |
|---|---|
| Job map | “Build a job map…” |
| Help | `/job-map-express help` |
| Success metrics | “Outcomes for step 12” |
| Related jobs | Precursor / concurrent / successor |
| Situational factors | Condition / event / time |
| Social / emotional jobs | Desired + undesired |
| Financial metrics | Direction + metric + unit |
| Solution approaches | Approaches for a step (not the job) |
| Root causes | Causes for a metric (no fake survey math) |
| Consumption job | Separate map around a solution class |

**Hard method rule:** phases ≠ steps. Phases (Define→Conclude) are coverage tags. Steps are the chronological map; `fidelity` sets step count. Never one-step-per-phase by default.

Method detail: `job-map-express/references/job-map-kb.md`. Capability list: `job-map-express/references/help.md`.

---

## Repo layout

```text
job-map-express-skill/
├── README.md
├── LICENSE
├── NOTICE
├── .cursor-plugin/marketplace.json      # Cursor Team Marketplace
├── .claude-plugin/marketplace.json      # Claude Code marketplace
├── .agents/plugins/marketplace.json     # Codex / ChatGPT Work
├── job-map-express/                     # direct skill-folder install
│   ├── SKILL.md
│   └── references/
└── plugins/job-map-express/             # plugin wrapper
    ├── .cursor-plugin/plugin.json
    ├── .claude-plugin/plugin.json
    ├── .codex-plugin/plugin.json
    └── skills/job-map-express/          # same skill payload
```

For folder installs, copy `job-map-express/` (or `plugins/job-map-express/skills/job-map-express/`) into your agent’s skills directory. Folder name must stay `job-map-express`.

---

## Install from GitHub (any compatible agent)

```bash
git clone https://github.com/mikeboysen/job-map-express-skill.git
# Then copy job-map-express/ into the path for your tool (sections below)
```

Windows (PowerShell):

```powershell
git clone https://github.com/mikeboysen/job-map-express-skill.git $env:TEMP\jme-skill
# Then Copy-Item the job-map-express folder into the tool path below
```

After install, start a **new** agent session (or reload the window). Invoke with `/job-map-express` or ask naturally. Use `/job-map-express help` for the full capability list.

---

### Cursor

| Scope | Path |
|---|---|
| User (global) | `~/.cursor/skills/job-map-express/` |
| Project | `.cursor/skills/job-map-express/` |

Cursor also discovers `.agents/skills/` in a project.

**Clone into global skills**

```bash
mkdir -p ~/.cursor/skills
git clone https://github.com/mikeboysen/job-map-express-skill.git /tmp/jme-skill
cp -R /tmp/jme-skill/job-map-express ~/.cursor/skills/job-map-express
rm -rf /tmp/jme-skill
```

Windows:

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
git clone https://github.com/mikeboysen/job-map-express-skill.git $env:TEMP\jme-skill
Copy-Item -Recurse -Force "$env:TEMP\jme-skill\job-map-express" "$env:USERPROFILE\.cursor\skills\job-map-express"
```

**Cursor UI (Remote Rule)**

1. Open **Customize** → **Rules** → **Add Rule**
2. Choose **Remote Rule (Github)**
3. Paste: `https://github.com/mikeboysen/job-map-express-skill`

**Cloud Agents:** Settings → Agents → **Sync Skills for Cloud Agents** if you want `~/.cursor/skills/` available remotely.

Docs: [Cursor Agent Skills](https://cursor.com/docs/skills)

---

### Google Antigravity

| Scope | Path |
|---|---|
| Workspace | `<workspace>/.agents/skills/job-map-express/` |
| Global | `~/.gemini/config/skills/job-map-express/` |

Prefer `.agents/skills/` (plural). Older `.agent/skills/` still works.

**Workspace (recommended for teams)**

```bash
mkdir -p .agents/skills
git clone https://github.com/mikeboysen/job-map-express-skill.git /tmp/jme-skill
cp -R /tmp/jme-skill/job-map-express .agents/skills/job-map-express
rm -rf /tmp/jme-skill
```

**Global**

```bash
mkdir -p ~/.gemini/config/skills
git clone https://github.com/mikeboysen/job-map-express-skill.git /tmp/jme-skill
cp -R /tmp/jme-skill/job-map-express ~/.gemini/config/skills/job-map-express
rm -rf /tmp/jme-skill
```

**Optional:** `npx skills add mikeboysen/job-map-express-skill -a antigravity` (writes under `.agents/skills/`). If nesting or symlinks mis-resolve, copy `job-map-express/` into the path above.

Docs: [Antigravity Skills](https://www.antigravity.google/docs/skills/)

---

### Claude Code

| Scope | Path |
|---|---|
| Personal (global) | `~/.claude/skills/job-map-express/` |
| Project | `.claude/skills/job-map-express/` |

```bash
# Personal
mkdir -p ~/.claude/skills
git clone https://github.com/mikeboysen/job-map-express-skill.git /tmp/jme-skill
cp -R /tmp/jme-skill/job-map-express ~/.claude/skills/job-map-express
rm -rf /tmp/jme-skill

# Or project
mkdir -p .claude/skills
cp -R job-map-express .claude/skills/job-map-express
```

New Claude Code session, then `/job-map-express`.

This is **GitHub folder install**, not an Anthropic marketplace listing.

Docs: [Claude Code Skills](https://code.claude.com/docs/en/skills)

---

### OpenAI Codex

| Scope | Path |
|---|---|
| User (global) | `~/.codex/skills/job-map-express/` (or `$CODEX_HOME/skills/` when set) |
| Project / repo | `.agents/skills/job-map-express/` (Codex scans `.agents/skills` up the tree); also commonly `.codex/skills/` |

```bash
# User
mkdir -p ~/.codex/skills
git clone https://github.com/mikeboysen/job-map-express-skill.git /tmp/jme-skill
cp -R /tmp/jme-skill/job-map-express ~/.codex/skills/job-map-express
rm -rf /tmp/jme-skill

# Project
mkdir -p .agents/skills
cp -R job-map-express .agents/skills/job-map-express
```

**Optional:** Codex `$skill-installer` can take a GitHub URL — paste `https://github.com/mikeboysen/job-map-express-skill`. Final path must be `…/skills/job-map-express/SKILL.md`.

Restart Codex if needed. Invoke via `/skills`, `$`, or natural language.

This is **GitHub folder install**, not an OpenAI curated marketplace listing.

Docs: [Codex Skills](https://developers.openai.com/codex/skills)

---

---

## Plugin marketplaces (ready — not submitted yet)

This repo also ships **plugin wrappers** so marketplaces can point at GitHub:

| Surface | Manifest |
|---|---|
| Cursor Team Marketplace | `.cursor-plugin/marketplace.json` → `plugins/job-map-express/` |
| Claude Code marketplace | `.claude-plugin/marketplace.json` → `plugins/job-map-express/` |
| Codex / ChatGPT Work plugins | `.agents/plugins/marketplace.json` → `plugins/job-map-express/` |

Plugin payloads live under `plugins/job-map-express/` (with `skills/job-map-express/` inside). The top-level `job-map-express/` folder remains for direct skill-folder installs.

### Add this repo as a marketplace (self-hosted)

**Claude Code**

```text
/plugin marketplace add mikeboysen/job-map-express-skill
/plugin install job-map-express@job-map-express-skill
```

**Codex**

```bash
codex plugin marketplace add mikeboysen/job-map-express-skill
codex plugin add job-map-express@job-map-express-skill
```

**Cursor Team Marketplace** (Teams/Enterprise admin)

1. Dashboard → Settings → Plugins → Team Marketplaces → Import / Add
2. Paste `https://github.com/mikeboysen/job-map-express-skill`
3. Review the parsed `job-map-express` plugin and assign access groups

### Public directory submissions (do later — gate closed until Mike opens)

- Cursor public marketplace: https://cursor.com/marketplace/publish
- Claude community directory: https://platform.claude.com/plugins/submit (public GitHub URL; run `claude plugin validate` first)
- Codex official directory: separate curated path — use repo marketplace add until invited/listed

Until those gates open, use **folder install** (sections above) or **self-hosted marketplace add**.


## Use

1. Install with one of the sections above.
2. New agent session.
3. `/job-map-express help` — capabilities.
4. `/job-map-express` or “Build a high-fidelity job map for …” — skill asks for missing required inputs (`job`, `end_user`, `fidelity`). `focus` defaults to `NA`.

### Required intake (job map)

- **Required:** `job`, `end_user`, `fidelity` (`low` 5–8 · `med` 8–14 · `high` 14–20 steps)
- **Default:** `focus` = `NA` (`B2C` / `B2B` / `NA`)
- **Optional:** `context`, `start_point`, `end_point`

---

## What this is not

- Not the hosted Job Map Express web app (`app.jtbd.one`)
- Not an OpenAI or Anthropic marketplace listing (GitHub install only)
- Not a license to Competing Use or trademark use — see `LICENSE` and `NOTICE`

---

## License

PolyForm Shield 1.0.0 — Practical JTBD, LLC. See `LICENSE` and `NOTICE`.
