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

---

### 2026-09-11 — A payment that changes nothing can still just be a slow payment

**What happened.** DataForSEO returned 402 after a reported top-up, and again after a £46
payment. I reasoned that zero change across five independent product lines pointed at a
credentials mismatch rather than funds. It did not — the payment simply took time to settle,
and everything worked on the next retest.

**Rule.** The diagnostic probe was right and worth keeping; the conclusion drawn from it was
not. When a payment is minutes old, "not settled yet" outranks every cleverer hypothesis, and
the honest answer is "retest in fifteen minutes" rather than a confident theory. Reserve the
credentials explanation for a balance the provider's own account endpoint confirms is healthy.

---

### 2026-09-11 — Mark unverified figures, then let the data delete your plan

**What happened.** The first `config/targets.md` was built from a crawl with every volume
marked `[unverified]`. When real data arrived, four of the Tier A keywords had no search
volume at all, the flagship page's target term was worth 10 searches a month, and the largest
opportunity on the site (Postinor-2, 1,600/mo) was absent from the plan entirely.

**Rule.** A hypothesis written as a hypothesis costs nothing to throw away. Never let a
plausible keyword list harden into a plan before a measured number touches it — and when the
number arrives, delete what it contradicts rather than defending it.

