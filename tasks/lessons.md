# Lessons

Corrections, and the rule written so the same mistake cannot recur. Append; never delete.
Every bot reads this file before working.

---

### 2026-09-11 — Don't assume the deliverable from a pasted document

**What happened.** A launch announcement was pasted into an empty repo with no instruction.
Building something from it directly would have guessed wrong — the actual ask was a new
repository and an analysis.

**Rule.** When the input is a document and the instruction is absent, ask what the deliverable
is before building. One question costs a minute; the wrong build costs the session.

---

### 2026-09-11 — Check integration permissions before promising an action

**What happened.** Repository creation was attempted and returned
`403 Resource not accessible by integration`. The limit was in the GitHub App's scope, not in
anything recoverable from the session.

**Rule.** When an action depends on an integration's permissions, treat failure as a real
possibility and report the exact error and the remedy rather than retrying or working around
it silently. Say which specific permission is missing.

---

### 2026-09-11 — A regulated buyer inverts the autonomy pitch

**What happened.** The analysed launch page sells autonomy as the reward, up to a testimonial
endorsing no human review at all. For health and pharmacy clients that framing is
disqualifying rather than aspirational.

**Rule.** In everything this team produces for health brands, the audit trail and the named
human reviewer are the feature, not the caveat. Never draft copy that sells the removal of
clinical review, including for ourselves.

---

### 2026-09-11 — Diagnose a 402 before reporting it as "still broken"

**What happened.** DataForSEO was reported as topped up and still returned 402. Reporting only
that would have sent Alex back to the same screen with no new information.

**Rule.** When a paid API keeps failing after the user says they fixed it, probe across product
lines and include a free or unmetered endpoint in the probe. A free endpoint returning 200 while
every billable one returns 402 isolates the fault to account balance and rules out credentials,
connector and scope in one pass. Report the table, not the verdict.

