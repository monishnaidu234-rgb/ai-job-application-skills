---
name: job-fit-flag-analyzer
description: Screens a job description against the user's own hard exclusions, sector preferences, and known scam/mismatch patterns before any CV or cover letter time gets spent on it. Use whenever the user pastes a job description or vacancy link and asks "should I apply", "is this worth my time", or before starting any tailoring work. Also use to triage a batch of search results before the user picks which to pursue.
---

# Job Fit & Flag Analyzer

Read `references/profile.md` before doing anything. This skill relies on Sections B, C,
and D specifically — right to work, career target and exclusions, and standing hard
exclusions. Never ask the user for information already in that file.

**Whenever the user corrects a fact — a wrong assumption about a gap, a sector they
actually don't mind, a tool they do have experience with — update `profile.md`
immediately in that turn.**

## First-Run Setup (mandatory before first use)

If `references/profile.md` doesn't exist yet or is essentially empty, work through
`references/PROFILE_TEMPLATE.md` Sections B, C, and D with the user first — a few
questions at a time. This is what prevents the same role being wrongly flagged or
wrongly waved through later. Sections E through K aren't needed for this skill alone; if
the user is also using a CV or cover letter skill from this same set, those sections get
filled in when that skill is used.

## What This Skill Does

Given a job description, decide — before any writing work happens — whether it's worth
the user's time, and say so plainly. This is a triage step, not a tailoring step.

## Step 1 — Tracker check

If the user maintains an application tracker (in `profile.md` or elsewhere), check for
a matching company and role first. If already processed, say so immediately and show
the prior outcome rather than re-analysing from scratch.

## Step 2 — Hard exclusion check

Check the JD against the user's own Standing Hard Exclusions (`profile.md` Section D) —
never against a generic assumption of what "most people" would exclude. Flag and stop
(don't proceed to any writing work) if any of the following are true:

- A tool, platform, or skill the user has named as a genuine gap is listed as essential,
  not desirable
- A driving licence is required and the user doesn't hold one for that country
- Security clearance is required and the user can't meet it
- An explicit years requirement in a *specific named sub-discipline* doesn't match the
  user's actual specific experience (e.g. "2 years in X specifically" where their real
  background is a different specific area) — this functions as a literal ATS knockout
  question. Distinguish this from a broad, generic years requirement the user is
  genuinely close to (check `profile.md`'s experience breakdown in Section D) — that
  stays a flagged, workable gap, not an automatic exclusion.
- The actual body text and duties are majority a different function (sales, reception,
  admin, operations) despite a matching-sounding title
- The sector or company type is on the user's own exclusion list (Section C or D)
- A right-to-work gate is stated in current tense and genuinely conflicts with the
  user's actual status (Section B) — not a future date, a present-tense requirement

**Never flag** anything the user has told Claude is already settled for them (visa
already confirmed workable, relocation already agreed, a degree title that already
covers a stated requirement).

## Step 3 — Scam and mismatch pattern check

**Field-sales-as-marketing (or similar bait-and-switch) pattern:** watch for vague
culture language with no named clients or sectors, phrases like "brand representation"
or "live campaign activity," multiple near-identical job titles from the same company, a
narrow or absent base salary paired with vague "performance-based progression," and
sometimes a long list of unrelated entry-level job titles pasted at the bottom purely for
SEO capture. Two or more of these signs → flag hard, verify with a quick web search for
"[company] reviews" before proceeding any further. Keep a private log of confirmed
instances in `profile.md` for the user's own future reference — never publish or share
this log anywhere, since naming specific companies as suspect carries real reputational
and legal risk if shared publicly.

**Scraped or reposted listings:** if the JD body text names a different employer than
the one on the posting, that's scraped content. Point the user toward the legitimate
employer's own listing instead.

**Toxic-culture language:** repeated "fast-paced" (3+ uses), "wear many hats," "like a
family," "rockstar/ninja/guru," "unlimited vacation," or "competitive salary"/"DOE"
with genuinely no figure anywhere. Note briefly, don't auto-exclude on this alone unless
combined with other flags.

**Deadline collisions:** if the user has told Claude about a hard personal deadline
(a thesis, a notice period, another commitment), flag any role whose start date or
timeline would collide, and suggest checking the live listing rather than assuming
either way.

## Step 4 — Timing check

If the posting date is visible or findable, check it. Fresh postings (within 48-72
hours) have materially better odds — many recruiters review in arrival order and pause
after a large volume of applications. Say so if timing suggests speed matters, or if the
listing is old enough that expectations should be calibrated down.

## Step 5 — Genuine-or-volume classification

If the role clears Steps 2 and 3, classify it as genuine (a real, specific reason for
wanting this company that would survive a follow-up question at interview) or volume (an
honest, general motivation, no fabricated enthusiasm). Check `profile.md` Section C for
the user's stated default. State the classification plainly — this feeds directly into
how a cover letter skill or application-answer skill should approach the same role
later.

## Output Format

Keep this tight and scannable, not a long essay:

1. One line: tracker status (new / already processed, with outcome if so)
2. If excluded: the specific reason, in one or two sentences, then stop
3. If flagged but not excluded: the specific gap or concern, named plainly, with the
   user's own words used wherever possible ("you've said you don't have X" rather than
   an invented justification)
4. Timing note, if relevant
5. Genuine/volume classification, one line

Never proceed to CV or cover letter work within this skill — that's out of scope here.
If the user asks to proceed with tailoring after seeing the flag output, hand off
naturally to whichever CV or cover letter skill they have installed.
