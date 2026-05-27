# Test Scenario 1 — AI Feature Request

> **Input:** `"Chúng tôi cần thêm AI vào Digital School"`
> (English: "We need to add AI to Digital School")
>
> **Difficulty:** Hard — maximum Solution Bias. "AI" is named as the solution
> with no problem statement. The actual problem could be: low completion rate,
> poor mentor matching, slow content search, ineffective feedback, or
> personalisation gaps.
>
> **Author:** Phúc NT · BA Zone · bazone.org

---

## Expected Behaviour

### Turn 1 — Skill response

The skill MUST:

1. **Explicitly flag Solution Bias.** "AI" is a tool, not a problem.

   Sample wording:
   > "Trước khi scope tính năng AI, tôi muốn chắc chắn đây là giải pháp
   > đúng. 'AI' là công cụ — hãy tìm vấn đề cần giải quyết trước.
   > Một vài câu hỏi:"
   >
   > "Before I scope the AI feature, I want to make sure it's the right
   > answer. 'AI' is a tool — let's find the problem first."

2. **Show layer status — all empty:**

   | Layer | Status |
   |---|---|
   | Business Requirement | ⛔ empty |
   | Stakeholder Requirement | ⛔ empty |
   | Functional Requirement | ⛔ empty |
   | NFR | ⛔ empty |
   | Transition | ⛔ empty |

3. **Ask 4-5 problem-discovery questions:**
   - Which part of the learner journey is broken today — discovery, enrollment, learning, or completion?
   - What is the current course completion rate, and what's the target?
   - Who experiences the problem most — self-paced learners, cohort learners, or enterprise-assigned learners?
   - What does the Digital School team try today when a learner disengages?
   - Is the problem content quality, engagement, mentor availability, or something else?

4. **Refuse to scope AI features in Turn 1.** No "should it use GPT-4 or
   Claude", no "should it personalise content or generate quizzes". Those
   are downstream decisions that depend on the confirmed problem.

---

### Turn 2 — User reply (typical)

> "Tỷ lệ hoàn thành khoá học chỉ có 38%. Học viên bỏ học nhiều nhất ở
> tuần 2-3. Chúng tôi không biết họ đang gặp khó khăn ở đâu."
>
> (Course completion rate is only 38%. Most learners drop off in weeks 2-3.
> We don't know where they're struggling.)

### Turn 2 — Skill response

NOW the problem is clear. The skill should:

1. **Confirm the problem statement:**
   > "So the real problem is: 62% of learners don't complete courses, with
   > peak drop-off in weeks 2-3, and the Digital School team has no early
   > warning signal to intervene. This is a retention and visibility problem,
   > not necessarily an AI problem."

2. **Validate the AI hypothesis vs alternatives:**
   - Could structured mentor check-ins at week 2 solve this without AI?
   - Could a simple engagement score (login frequency + lesson progress)
     alert ops without AI?
   - If AI wins: what specifically would it do — predict drop-off risk,
     personalise content, or generate mentor nudges?
   - What data is available to train or power the AI (login history, quiz
     scores, video watch time)?

3. **Update layer status:**

   | Layer | Status | Evidence |
   |---|---|---|
   | Business Requirement | ✅ | Increase completion rate from 38% to target X% |
   | Stakeholder Requirement | 🟡 | Learners in weeks 2-3; ops team needs visibility |
   | Functional Requirement | ⛔ | Not yet — depends on chosen solution |
   | NFR | ⛔ | Empty |
   | Transition | ⛔ | Empty |

4. **Edge-case scan:**
   - What if the AI flags a learner as at-risk but they're just on holiday?
   - Who acts on the AI alert — ops team, mentor, or automated message?
   - Is the intervention opt-in or automatic?
   - What's the privacy implication of tracking learner behaviour at
     this granularity (PDPA)?

---

## Acceptance Criteria

- [ ] Skill flags Solution Bias **explicitly** in Turn 1
- [ ] Skill asks zero AI-feature questions in Turn 1
- [ ] Skill surfaces ≥2 non-AI alternatives before accepting AI as the lever
- [ ] Skill establishes a measurable completion-rate KPI before scoping
- [ ] Skill surfaces data availability as a critical constraint
- [ ] Skill flags PDPA/privacy as an edge case for learner behaviour tracking
- [ ] Structured summary, when produced, lists alternatives considered in `assumptions`

---
*Scenario by **Phúc NT** · BA Zone · bazone.org*
