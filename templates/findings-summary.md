# Discovery Findings — `{{project_name}}`

> **Status:** Draft v{{version}} · {{date}}
> **BA:** Phúc NT · BA Zone · bazone.org
> **Digital School — BA/PO Discovery Workshop Output**

---

## 1. Business Problem

{{business_problem}}

## 2. Business Goal

{{business_goal}}

> *Measurable target:* `{{kpi_name}}` from `{{baseline}}` → `{{target}}` by `{{deadline}}`

---

## 3. Stakeholders

| Role | Organisation | Interest |
|---|---|---|
{{#each stakeholders}}
| {{role}} | {{org}} | {{interest}} |
{{/each}}

## 4. Pain Points

{{#each pain_points}}
- {{this}}
{{/each}}

## 5. Root Causes

> ⚠️ Root causes, not symptoms. Each item should be one 5-Why level deeper than the pain point.

{{#each root_causes}}
- {{this}}
{{/each}}

---

## 6. Functional Requirements

{{#each functional_requirements}}
- **FR-{{@index}}** — {{this}}
{{/each}}

## 7. Non-functional Requirements

{{#each non_functional_requirements}}
- **NFR-{{@index}}** — {{this}}
{{/each}}

## 8. Business Rules

{{#each business_rules}}
- **BR-{{@index}}** — {{this}}
{{/each}}

---

## 9. Constraints

{{#each constraints}}
- {{this}}
{{/each}}

## 10. Risks

| # | Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|---|
{{#each risks}}
| {{@index}} | {{description}} | {{likelihood}} | {{impact}} | {{mitigation}} |
{{/each}}

---

## 11. Assumptions

> ⚠️ Every assumption below needs validation before downstream BRD/PRD/SRS work begins.

{{#each assumptions}}
- {{this}}
{{/each}}

## 12. Dependencies

{{#each dependencies}}
- {{this}}
{{/each}}

## 13. Open Questions

> 🟡 These remain unresolved and block move-to-design until answered.

{{#each open_questions}}
- **Q-{{@index}}** — {{question}} *(owner: {{owner}}, needed by: {{deadline}})*
{{/each}}

---

## Next Steps

- [ ] Validate assumptions with stakeholders
- [ ] Resolve open questions (assign owners + deadlines)
- [ ] Hand off to PRD / BRD / Use Case writer
- [ ] Schedule edge-case review with engineering
- [ ] Share findings with BA Zone Digital School cohort (if applicable)

---
*Discovery output by **Phúc NT** · BA Zone · bazone.org*
*Template from the Ask-Why Elicitation Skill — Digital School edition*
