# Requirement Layers — BABOK v3 Taxonomy

> Compiled by **Phúc NT** · BA Zone · bazone.org
> *Aligned with IIBA BABOK v3 §3 — Digital School edition*

The skill classifies every requirement into one of five layers. Most user
input starts at the Business or Stakeholder layer — lower layers are empty.
The skill's job is to populate the missing layers progressively.

---

## 1. Business Requirement

**Definition:** *Why* the organisation is doing this — the goal, the problem,
the business value.

**Owner:** Executive sponsor / Product Owner / Founder.

**Digital School example:**
> "Increase Digital School course completion rate from 42% to 65% by Q4,
> to improve learner outcome and reduce churn."

**Empty-layer signal:** user describes a feature but cannot state why it
matters to the business.
→ Ask: *"What KPI does this move? What happens if we don't do it?"*

---

## 2. Stakeholder Requirement

**Definition:** *Who* needs what, expressed from the stakeholder's perspective.

**Owner:** End-user / Business stakeholder.

**Digital School example:**
> "As a Digital School learner in week 2 of a cohort, I need a structured
> check-in from my mentor so I don't fall behind without realising it."

**Empty-layer signal:** user describes system behaviour but no specific
stakeholder or role is named.
→ Ask: *"Who is the user of this feature? What's their role and context?"*

---

## 3. Functional Requirement

**Definition:** *What* the system must do — behaviours, transformations,
inputs, outputs.

**Owner:** BA / Product / Engineering.

**Digital School example:**
> "System shall send an automated check-in nudge to any learner who has not
> logged in for 5 consecutive days, with a personalised message from their
> assigned mentor."

**Empty-layer signal:** user is at stakeholder-need level but no concrete
system behaviour is articulated.
→ Ask: *"What specifically should the system do when [stakeholder] is
in [situation]?"*

---

## 4. Non-functional Requirement (NFR)

**Definition:** *How well* the system must do it — performance, availability,
security, scalability, usability, compliance.

**Owner:** Architecture / Security / SRE / Compliance.

**Digital School example:**
> "Nudge emails must be delivered within 15 minutes of trigger. System must
> support 50,000 active learners. Learner data must comply with Vietnam PDPA
> and not be stored outside Vietnam."

**Empty-layer signal:** functional requirements exist but no quantitative
quality attributes have been stated.
→ Ask: *"What's the acceptable response time? Volume? Data retention?
Compliance regime?"*

---

## 5. Transition Requirement

**Definition:** What's needed to move from the *current* state to the *future*
state — data migration, training, change management, cutover plan.

**Owner:** PMO / Change manager / Ops lead.

**Digital School example:**
> "Migrate 6 months of learner progress data to the new LMS. Run old and new
> systems in parallel for 30 days. Train 15 BA Zone instructors on the new
> mentor portal before go-live."

**Empty-layer signal:** team has agreed on the future state but no discussion
of *how the organisation gets there*.
→ Ask: *"What data needs to migrate? Who needs training? Is parallel-run
required? What's the rollback plan?"*

---

## Layer Status Table (use this every turn)

After collecting any new information, show this table to make discovery
state visible:

| Layer | Status | Evidence |
|---|---|---|
| Business Requirement | ✅ / 🟡 / ⛔ | *[one line]* |
| Stakeholder Requirement | ✅ / 🟡 / ⛔ | *[one line]* |
| Functional Requirement | ✅ / 🟡 / ⛔ | *[one line]* |
| Non-functional Requirement | ✅ / 🟡 / ⛔ | *[one line]* |
| Transition Requirement | ✅ / 🟡 / ⛔ | *[one line]* |

**✅** = clear and confirmed
**🟡** = partial — more detail needed
**⛔** = empty — not discussed yet

This table turns the conversation from "answer my question" to
"let's fill the gaps together" — a key technique from
BA Zone's discovery workshop methodology.

---
*Compiled by **Phúc NT** · BA Zone · bazone.org*
*Full layer-mapping exercises and case studies available in Digital School BA Advanced.*
