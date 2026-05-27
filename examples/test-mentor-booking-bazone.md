# Test Scenario 2 — Mentor Booking System

> **Input:** `"Cần xây dựng hệ thống đặt lịch mentor cho BA Zone"`
> (English: "We need to build a mentor booking system for BA Zone")
>
> **Difficulty:** Medium — Feature Request with embedded Solution Bias.
> The booking system is proposed as the solution before the problem is
> confirmed.
>
> **Author:** Phúc NT · BA Zone · bazone.org

---

## Expected Behaviour

### Turn 1 — Skill response

The skill should:

1. **Flag intent type:** Feature Request with Solution Bias signal
   ("booking system" is a solution, not a problem statement).

2. **Show layer status:**

   | Layer | Status |
   |---|---|
   | Business Requirement | ⛔ empty |
   | Stakeholder Requirement | ⛔ empty |
   | Functional Requirement | ⛔ empty |
   | NFR | ⛔ empty |
   | Transition | ⛔ empty |

3. **Ask 4 contextual questions:**
   - What business KPI should a booking system improve — mentor utilisation,
     learner satisfaction, or session volume?
   - How do BA Zone learners and mentors coordinate sessions today — and what
     breaks in the current process?
   - Who experiences the most friction: the learner trying to book, the mentor
     managing their calendar, or the BA Zone ops team coordinating both?
   - What happens today when a learner can't find a suitable mentor slot?

4. **Do NOT** start designing booking flows, calendar integrations, or
   notification logic in Turn 1.

---

### Turn 2 — User reply (typical)

> "Hiện tại mentor và học viên nhắn tin qua Zalo để đặt lịch. Tốn nhiều
> thời gian và hay bị nhầm lịch, no-show. Ops team phải nhắc thủ công."
>
> (Mentors and learners currently book sessions via Zalo messages. It's
> time-consuming, prone to scheduling errors, no-shows. Ops team has to
> remind manually.)

### Turn 2 — Skill response

Now the problem is clear. The skill should:

1. **Reclassify intent:** Workaround → Operational Pain.
   The Zalo coordination is a workaround for a missing scheduling feature.

2. **Confirm the problem statement:**
   > "So the real problem is: BA Zone's mentor-learner scheduling is running
   > on informal Zalo messages, causing time waste, double-bookings, no-shows,
   > and manual ops overhead. A booking system may solve this — but let's
   > size the problem first."

3. **Quantify the pain:**
   - How many mentor sessions happen per week across BA Zone?
   - What % result in no-show or reschedule?
   - How many hours does the ops team spend per week on manual reminders?

4. **Challenge scope before building:**
   - Could a shared Google Calendar + automated reminder solve 80% of the
     problem at near-zero cost?
   - Is the real gap scheduling, reminders, or cancellation handling?
   - What's the threshold at which a custom booking system is justified?

5. **Edge-case scan:**
   - What if a mentor cancels within 2 hours of the session?
   - Can learners reschedule, and how many times?
   - What happens to learner session quota if a mentor no-shows?
   - Timezone handling for international learners?
   - Does BA Zone charge for sessions, and if so, is payment in scope?

---

## Acceptance Criteria

- [ ] Skill reclassifies from Feature Request → Operational Pain when
      the workaround pattern (Zalo coordination) emerges
- [ ] Skill quantifies pain in hours/sessions before accepting scope
- [ ] Skill surfaces Google Calendar as a low-cost alternative
- [ ] Skill investigates cancellation, no-show, and quota rules as edge cases
- [ ] Skill asks about payment integration before assuming it's out of scope
- [ ] Structured summary clearly distinguishes symptom (Zalo chaos) from
      root cause (no scheduling system) in `pain_points` vs `root_causes`

---
*Scenario by **Phúc NT** · BA Zone · bazone.org*
