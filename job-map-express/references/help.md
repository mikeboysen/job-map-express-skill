# Job Map Express skill — help

Trigger this file when the user runs `/job-map-express help`, `help`, `what can you do`, or asks for capabilities/commands.

## Commands / asks

| User says (examples) | What you do |
|---|---|
| `/job-map-express help` | Show this capability list (do not generate a map). |
| Build / create a **job map** | Intake → confirm → chronological steps (fidelity sets count). |
| **Success metrics** / outcomes for step N (or all) | PJTBD outcome syntax on steps. |
| **Related jobs** | Precursor / Concurrent / Successor jobs for the core job. |
| **Situational factors** | Condition / Event / Time factors with impact + worst→best. |
| **Social jobs** | Desired + Undesired social jobs for the end user in this job. |
| **Emotional jobs** | Desired + Undesired emotional jobs (same pairing pattern). |
| **Financial metrics** | Direction + metric + unit (+ optional step tie). |
| **Solution approaches** for step N | 3–7 classes of means — labeled approaches, not the job. |
| **Root causes** for a metric | Multiple causes; no fake survey math. |
| **Consumption job** (e.g. maintain/buy/install X) | Separate map for a consumption journey around a solution class. |

## Required intake (job map)

- **Required:** `job`, `end_user`, `fidelity` (`low` 5–8 · `med` 8–14 · `high` 14–20)
- **Default:** `focus` = `NA` if omitted (`B2C` / `B2B` / `NA`)
- **Optional:** `context`, `start_point`, `end_point`

If required fields are missing → **ask**. Never invent them.

## Hard rules (short)

- **Phases ≠ steps.** Phases tag coverage; steps are the chronological map. Never one-step-per-phase autopilot.
- Solution-agnostic core job and functional steps (consumption jobs may name the solution class).
- Singular human Job Executor.
- No public “When … I want to … so I can …” templates.
- No OpenAI/Anthropic publish paths from this skill.

## Method detail

See `references/job-map-kb.md` for phases, step rules, and metric syntax.
