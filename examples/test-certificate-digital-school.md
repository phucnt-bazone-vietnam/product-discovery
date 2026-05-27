# Test Scenario 3 — Digital Certificate & Compliance

> **Input:** `"Digital School cần cấp chứng chỉ số cho học viên hoàn thành khoá học"`
> (English: "Digital School needs to issue digital certificates for learners who complete courses")
>
> **Difficulty:** Easy-Medium — Feature Request that looks clear but hides
> several business rule, compliance, and fraud-risk gaps.
>
> **Author:** Phúc NT · BA Zone · bazone.org

---

## Expected Behaviour

### Turn 1 — Skill response

The skill should:

1. **Flag intent type:** Feature Request (legitimate, specific) — but with
   important gaps in business rules, fraud risk, and compliance.

2. **Show layer status:**

   | Layer | Status |
   |---|---|
   | Business Requirement | 🟡 partial — completion goal implied, no KPI |
   | Stakeholder Requirement | 🟡 partial — learner named, employer not |
   | Functional Requirement | ⛔ empty — no rules defined |
   | NFR | ⛔ empty |
   | Transition | ⛔ empty |

3. **Ask 4 contextual questions:**
   - What defines "completion" — 100% lesson progress, passing a final
     assessment, or both?
   - Who verifies the certificate — employers, LinkedIn, or third-party
     accreditation bodies?
   - Does Digital School need to meet any regulatory standard (Ministry of
     Education recognition in Vietnam, ISO, or professional body accreditation)?
   - What prevents a learner from sharing login credentials and having
     someone else complete the course on their behalf?

4. **Surface the fraud/integrity question early** — it's the most commonly
   missed requirement in EdTech certificate features.

---

### Turn 2 — User reply (typical)

> "Học viên cần pass bài test cuối ≥ 70% mới được cấp. Chứng chỉ cần có
> QR code để nhà tuyển dụng verify. Chưa cần công nhận nhà nước."
>
> (Learners need to pass the final assessment ≥ 70% to receive the
> certificate. Certificate needs a QR code for employer verification.
> State recognition not required yet.)

### Turn 2 — Skill response

1. **Update layer status:**

   | Layer | Status | Evidence |
   |---|---|---|
   | Business Requirement | ✅ | Increase course credibility for learner employability |
   | Stakeholder Requirement | ✅ | Learner (receives cert), Employer (verifies cert) |
   | Functional Requirement | 🟡 | Pass ≥70%, QR verification — rules incomplete |
   | NFR | ⛔ | Empty |
   | Transition | ⛔ | Empty |

2. **Drill into business rules:**
   - What's the assessment — multiple choice, project submission, or live
     demo? Who grades non-MC assessments?
   - Can a learner retake the assessment? How many times, and with what
     cooling-off period?
   - Does the certificate expire? Does Digital School re-issue if content
     is significantly updated?
   - Is the certificate PDF, blockchain-anchored, or Open Badge standard?

3. **Edge-case scan:**
   - What if the QR verification service is down when an employer scans?
   - What if a learner disputes their assessment result?
   - What if Digital School revokes a certificate (fraud, plagiarism) —
     how does the employer know?
   - PDPA: what learner data is embedded in the QR/certificate, and for
     how long is it stored?

---

## Acceptance Criteria

- [ ] Skill surfaces the identity/fraud question in Turn 1
- [ ] Skill asks about assessment retake rules and grading process
- [ ] Skill probes certificate validity, expiry, and revocation
- [ ] Skill flags QR service availability as a reliability edge case
- [ ] Skill raises PDPA implications of data embedded in certificates
- [ ] Structured summary includes fraud/integrity in `risks` and
      retake limits in `business_rules`

---
*Scenario by **Phúc NT** · BA Zone · bazone.org*
