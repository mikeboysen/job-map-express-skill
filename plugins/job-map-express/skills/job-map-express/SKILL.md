---
name: job-map-express
description: >-
  Job Map Express — build JTBD job maps in chat. Use when the user mentions
  Job Map Express / JME or runs /job-map-express. Ask for missing inputs
  before inventing; never one step per phase by default.
---

# Job Map Express

Run the **Job Map Express** method in chat. Rigorous, solution-agnostic, interview-first.

## Help (do this first when asked)

If the user says `/job-map-express help`, `help`, `what can you do`, `commands`, or `capabilities`:

1. Open `references/help.md` and present the capability list clearly.
2. Do **not** generate a map until they ask for one.
3. Offer one-line examples of asks they can type next.

## Core distinction

**Phases ≠ steps.** Phases (Define→Conclude) tag and audit coverage. Steps are the chronological job map; `fidelity` controls **step count**. Never default to one step per phase or invent filler steps for empty phases.

Method detail: `references/job-map-kb.md`. Capability list: `references/help.md`.

This skill is **not** the hosted Job Map Express app and does **not** publish to OpenAI or Anthropic.

## Procedure

1. **Route the ask** — help → `help.md`; else pick the capability (map, metrics, related jobs, etc.).
2. **Intake** — For a job map, required: `job`, `end_user`, `fidelity`. `focus` defaults to `NA`. Optional: `context`, `start_point`, `end_point`. Ask only for missing required fields.
3. **Confirm** — Restate Scenario when generating a map (unless they already said proceed).
4. **Generate** — Follow `job-map-kb.md` for maps/metrics; use product dimension shapes for related / situational / social / emotional / financial / approaches / consumption.
5. **Close** — What we built, phase coverage notes (for maps), what’s open, next ask.

## Hard gates

- Singular human Job Executor  
- Solution-agnostic functional job and steps  
- No one-step-per-phase autopilot  
- No vague verbs (manage / facilitate / empower / enable / ensure / oversee)  
- FACT / ASSUMPTION / HUNCH on unsourced market claims  
