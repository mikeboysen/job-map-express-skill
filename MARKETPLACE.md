# Marketplace checklist (gates)

Wrappers are in-repo. **Do not submit** to public directories until Mike opens each gate in CoS chat.

## Ready now (self-hosted / team)

- [x] Cursor Team Marketplace manifests (`.cursor-plugin/`)
- [x] Claude Code marketplace manifests (`.claude-plugin/`)
- [x] Codex marketplace manifests (`.agents/plugins/`)
- [ ] Cursor Team import (Teams/Enterprise admin pastes repo URL)
- [ ] Claude: `/plugin marketplace add mikeboysen/job-map-express-skill`
- [ ] Codex: `codex plugin marketplace add mikeboysen/job-map-express-skill`

## Public directories (submit only when opened)

- [ ] Cursor public marketplace — https://cursor.com/marketplace/publish
- [ ] Claude community — `claude plugin validate ./plugins/job-map-express` then https://platform.claude.com/plugins/submit
- [ ] Codex official / curated directory — only if invited or form opens

## Notes

- License remains PolyForm Shield 1.0.0 (Competing Use prohibited).
- Direct skill-folder install stays supported via top-level `job-map-express/`.
