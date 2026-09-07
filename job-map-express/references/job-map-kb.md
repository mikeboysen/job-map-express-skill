# Job Map Express — method KB (skill-only)

Minimal method needed to run maps in chat. No consulting playbooks, no inversion strategy, no survey engines.

## Critical distinction

**Job phases ≠ job steps.**

- **Phases** are a universal MECE frame (Define → Conclude). They classify and check coverage.
- **Steps** are the chronological actions for *this* job. Fidelity sets how many steps you write.
- **Never** emit one step per phase by default. That collapses the frame into a fake 9-step map.
- A phase may contain **zero, one, or many** steps. Tag each step with its phase. Ensure the map’s steps, read in order, still make the job MECE for this scenario.
- If a phase has zero steps, that is allowed only when `start_point` / `end_point` or the job scope truly excludes that phase — say so explicitly. Do not invent filler steps just to “hit” a phase.

## 1. Scenario inputs

| Field | Required | Rule |
|-------|----------|------|
| `job` | yes | `[Verb] + [Object] + [Contextual clarifier]`. What the person is trying to accomplish — not a product or project name. |
| `end_user` | yes | One human role (Job Executor). Never a company, demographic, or department-as-actor. |
| `focus` | no (default **NA**) | `B2C` \| `B2B` \| `NA`. Default to `NA` unless the user sets otherwise. |
| `fidelity` | yes | `low` (5–8 steps) \| `med` (8–14) \| `high` (14–20). Step **count**, not phase count. |
| `context` | no | Setting constraints (industry, channel, regulation). |
| `start_point` / `end_point` | no | Optional map boundaries. |

**Missing inputs:** stop and ask in short batches (2–4 questions). Never invent `job`, `end_user`, or `fidelity`. Default `focus` to `NA` when omitted.

**Solution-shaped job:** if they name a tool/vendor, ask what outcome they are trying to get done until `job` is solution-agnostic; confirm the reframed job before mapping.

## 2. Phases (coverage frame — not the map)

Use these labels to tag steps and audit gaps:

1. **Define** — define, plan, or assess what must be known upfront  
2. **Locate** — locate/gather/access resources (tangible or intangible)  
3. **Prepare** — prepare or integrate inputs/environment  
4. **Confirm** — verify, prioritize, or decide before execution  
5. **Execute** — core action(s) that get the job done  
6. **Monitor** — monitor during execution  
7. **Resolve** — fix deviations / failures  
8. **Modify** — adjust based on monitor/resolve  
9. **Conclude** — finish and wrap up  

## 3. Steps (the actual job map)

1. Choose step **count** from fidelity (low 5–8, med 8–14, high 14–20).
2. Write chronological steps for **this** `job` / `end_user` / `context`.
3. Each step: verb-led `name`, short `description` of *what* (not *how*/tool), one `phase` tag.
4. Dense phases (often Execute, Resolve) may need several steps; quiet phases may need none or one.
5. After drafting, audit: reading only the steps, is the job complete and MECE? Any phase gap that the job actually requires?
6. Respect `start_point` / `end_point` if set.

## 4. Success metrics (outcomes)

PJTBD outcome syntax only:

`[Minimize|Increase] + [metric] + **[object of control]** + [contextual clarifier]`

- Object of control in **bold**
- Objective voice (no “you” / “the customer”)
- Solution-agnostic
- Attach metrics to **steps**, not to phases
- Ask: all steps or one step

Do **not** use public “When … I want to … so I can …” statement templates.

## 5. Optional (only if asked)

- Root causes for a named metric (several causes; no fake survey math)
- Solution *approaches* for a step/metric — labeled as approaches, not as the job map

## 6. Hard rejects

- Map without required Scenario fields  
- Non-human Job Executor  
- Solution/vendor language in job or steps  
- **One-step-per-phase autopilot** (especially a forced 9-step map)  
- Filler steps added only to populate empty phases  
- Step count outside fidelity band without user override  
- Vague verbs: manage, facilitate, empower, enable, ensure, oversee  

## 7. Tiny EXAMPLE (synthetic) — low fidelity, NOT 1:1 phases

- end_user: `Plant reliability engineer`  
- job: `Qualify a replacement sensor package for a sour-gas service envelope`  
- focus: `B2B` · fidelity: `low` (7 steps)

1. Define — Lock the combined operating envelope and certification obligations.  
2. Locate — Gather applicable standards and prior certificate packs for the service.  
3. Prepare — Build the constraint sheet from envelope + cert inputs.  
4. Confirm — Decide go/no-go scope against site and insurance rules.  
5. Execute — Specify the replacement configuration against the locked envelope.  
6. Resolve — Clear mismatches between offered configuration and envelope requirements.  
7. Conclude — Close acceptance with traceability artifacts for install and audit.  

*(Monitor/Modify have no dedicated steps here — scope didn’t require separate actions; Execute absorbs in-flight checks as description detail. That is intentional, not an error.)*

Sample Execute metric: `Minimize the likelihood of specifying **wetted materials** that fail the sour-service obligation`

Synthetic only — not evidence.
