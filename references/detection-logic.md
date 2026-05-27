# Detection Logic — Intent Classification

> Compiled by **Phúc NT** · BA Zone · bazone.org
> *Reference for the Ask Why elicitation skill — Digital School edition*

Use this when the user's wording is ambiguous. Each intent type lists signal
phrases and the recommended first response.

---

## 1. Feature Request

**Signals:** "I want to add", "we need to build", "add a button for", "can we
support feature X".

**Risk:** stakeholder is already in solution mode. Treat the feature as a
*hypothesis to test*.

**First response:** ask about the underlying problem, the impacted user, and
the success metric before discussing any feature details.

**Digital School example:**
> "We need a progress tracker on the Digital School platform."
> → Don't design the tracker yet. Ask: *What problem does the learner have
> today? Are they unaware of their progress, unmotivated to continue, or
> unable to communicate it to their employer?*

---

## 2. Complaint

**Signals:** "X is broken", "learners are unhappy with", "the platform is too
slow", "we keep getting support tickets about".

**Risk:** the symptom is described, but the root cause is unknown.

**First response:** use 5-Whys to drill from symptom to root cause. Ask for
frequency and business impact before proposing any fix.

**Digital School example:**
> "Learners say the video player keeps buffering."
> → Is the problem the video player, the CDN, the learner's connection,
> or the file encoding? Frequency? Which courses? Which devices?

---

## 3. Operational Pain

**Signals:** "the ops team spends hours doing", "manual reconciliation",
"copy-paste between systems", "BA Zone admin team does this by hand every week".

**Risk:** users have built workarounds — the real cost is hidden labour.

**First response:** quantify the labour cost (hours × people × frequency),
ask who owns the process today and what happens when they're unavailable.

---

## 4. Workaround

**Signals:** "we currently do this by exporting to Excel and...", "we use a
Zalo group to coordinate mentor sessions", "the team manages cohorts via
Google Sheets".

**Risk:** the workaround masks the real requirement. Stakeholder may demand
the workaround be productised, but a different solution may serve better.

**First response:** ask why the workaround exists, what the original gap was,
and what would happen if the workaround were removed tomorrow.

**Digital School example:**
> "We track learner attendance in a Google Sheet."
> → Why? Does the LMS not have this feature? Is it an export/integration
> problem? Or is it because the ops team needs a custom view the LMS
> doesn't support?

---

## 5. KPI Goal

**Signals:** "we want to reduce churn by", "increase course completion from
X% to Y%", "grow enterprise license revenue by Q4".

**Risk:** the KPI is clear but the lever is unknown.

**First response:** ask which learner or operator behaviour drives the KPI
today, and which candidate levers the business is considering. Don't jump to
solutions.

---

## 6. Solution Bias ⚠️ HIGHEST PRIORITY

**Signals:** user names a specific technology, platform, or feature pattern
as the requirement. "We need AI", "build a recommendation engine",
"add a chatbot to Digital School", "use blockchain for certificates".

**Risk:** stakeholder has skipped problem-discovery entirely.

**First response:** politely surface the bias. Do not scope the named
solution until the business problem is articulated clearly.

Script:
> "Before I scope [the solution], I want to make sure it's the right answer.
> '[Solution name]' is a tool — let's find the problem it's meant to solve
> first. A few questions: what's breaking today, who experiences it, and
> how would we measure success?"

**Never** ask what features the chatbot/AI/system should have until you've
confirmed the problem justifies that type of solution.

---

## 7. Business Objective

**Signals:** "our OKR this quarter is", "leadership wants us to", "the board
asked for", "Digital School's goal for H2 is".

**Risk:** objective is high-level; multiple feature paths could satisfy it.

**First response:** decompose into candidate problem statements, then ask
which one is the actual bottleneck today.

---

## 8. Process Issue

**Signals:** "the mentor booking flow has too many steps", "approval for
enterprise licenses takes too long", "handoff between Sales and CS is unclear".

**Risk:** process redesign may be in scope, not just a system tweak.

**First response:** map the as-is flow (steps, actors, handoffs, decision
points) before discussing the to-be state. Never design a new flow without
understanding the current one.

---

## 9. Reporting Need

**Signals:** "I need a report that shows", "can you export learner data",
"we need a dashboard for course performance".

**Risk:** stakeholder may want a static Excel export when a live dashboard
would serve them better — or vice versa.

**First response:** ask who consumes the report, how often, and what decision
it drives. Then evaluate: report vs dashboard vs API vs automated alert.

---

## 10. Compliance Concern

**Signals:** "regulation requires", "auditor flagged", "we need to comply
with PDPA / KYC / data localisation", "Vietnam MoET requirement".

**Risk:** compliance language is often imprecise. The actual control required
may be narrower than the regulatory citation suggests.

**First response:** ask for the specific clause or auditor finding, the
deadline, and the consequence of non-compliance. Then translate into a
testable control requirement.

---

## Ambiguous cases

If the input doesn't clearly fit one type, default to **Feature Request**
and ask:
> *"Before I scope this, can you tell me what problem this is solving
> and who experiences it most?"*

This question is safe for any of the 10 intent types and surfaces the
right classification naturally.

---
*Compiled by **Phúc NT** · BA Zone · bazone.org*
*Advanced signal detection and escalation logic covered in Digital School BA Advanced.*
