# Job Map Express — Agent Skill

Installable [Agent Skill](https://cursor.com/docs/skills) that runs the **Job Map Express** method in chat: job maps, success metrics, related jobs, situational factors, social/emotional jobs, financial metrics, solution approaches, root causes, and consumption jobs.

License: **PolyForm Shield 1.0.0** (see `LICENSE` + `NOTICE`).

## Install in Cursor

### Option A — GitHub remote (UI)

1. Open **Customize** in the sidebar  
2. **Rules** → **Add Rule** → **Remote Rule (Github)**  
3. Paste this repository URL: `https://github.com/mikeboysen/job-map-express-skill`

### Option B — Global skill folder (reliable)

```bash
git clone https://github.com/mikeboysen/job-map-express-skill.git temp-jme-skill
mkdir -p ~/.cursor/skills
cp -R temp-jme-skill/job-map-express ~/.cursor/skills/job-map-express
rm -rf temp-jme-skill
```

On Windows (PowerShell):

```powershell
git clone https://github.com/mikeboysen/job-map-express-skill.git $env:TEMP\jme-skill
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.cursor\skills" | Out-Null
Copy-Item -Recurse -Force "$env:TEMP\jme-skill\job-map-express" "$env:USERPROFILE\.cursor\skills\job-map-express"
```

### Option C — Project skill

Copy `job-map-express/` into `.cursor/skills/job-map-express/` in any project.

## Use

- `/job-map-express` — run the skill  
- `/job-map-express help` — full capability list  

## Not included

- Does **not** publish to OpenAI or Anthropic skill stores  
- Does **not** replace the hosted Job Map Express web app  

## Layout

```
job-map-express/
  SKILL.md
  references/
    help.md
    job-map-kb.md
```
