# Changelog · BA Zone Ask Why Skill

> Maintained by **Phúc NT** · BA Zone · bazone.org

## [1.0.0] - 2026-05-27

### Initial release — BA Zone Edition

#### Added
- Core `SKILL.md` — 7-step elicitation workflow (Intent → Layer → Gap → Questions → Insight → Edge Case → Summary)
- 10 intent types with Solution Bias as highest-priority flag
- 5 BABOK v3 requirement layers with visible status table
- Gap detection across 12 dimensions
- Question priority order (business impact → root cause → stakeholder → process → risk → edge case → value)
- Stop condition rules
- `references/detection-logic.md` — signal phrases and first-response moves for all 10 intent types
- `references/requirement-layers.md` — BABOK layer taxonomy with Digital School examples
- `references/question-library.json` — domain starter questions for EdTech, Digital School enrollment, mentor matching, loyalty, reporting, payment, AI features, integration
- `references/output-schema.json` — 13-field structured summary schema
- `templates/findings-summary.md` — markdown output template
- `examples/test-ai-feature-digital-school.md` — Solution Bias scenario: "Add AI to Digital School"
- `examples/test-mentor-booking-bazone.md` — Workaround pattern: Zalo scheduling chaos
- `examples/test-certificate-digital-school.md` — Hidden business rules: digital certificates

#### Design decisions
- 30% of advanced question-sequencing methodology withheld — covered in Digital School BA Advanced
- All examples use BA Zone / Digital School domain (EdTech, mentor matching, certificates)
- Question library includes `ai_feature` and `edtech_platform` domains not in the original
- LICENSE includes explicit note that advanced methodology is proprietary to BA Zone

#### Attribution
- Author: Phúc NT · BA Zone · Digital School · bazone.org
- License: MIT with attribution requirement
