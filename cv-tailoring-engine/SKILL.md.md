---
name: cv-tailoring-engine
description: Tailors a CV against a specific job description using a systematic keyword-extraction, positioning, and rewrite process, with a mandatory checklist to prevent quality drift. Use whenever the user asks to tailor their CV for a role, pastes a job description alongside their CV, or uploads a new CV version for review. Also use for "next one" or a bare company name once this pattern is established in the conversation.
---

# CV Tailoring Engine

Read `references/profile.md` before doing anything. This skill relies on Sections A,
E, F, G, and H specifically — identity, evidence bank, education, confirmed skills, and
CV format. Never ask the user for information already in that file.

**Whenever the user corrects a fact — a title, a date, an achievement's real number, a
module they want swapped in — update `profile.md` immediately in that turn.**

## First-Run Setup (mandatory before first use)

If `references/profile.md` doesn't exist yet or is essentially empty, work through
`references/PROFILE_TEMPLATE.md` Sections A, E, F, G, and H with the user first — a few
questions at a time, not all at once. This is the step that prevents every later
correction of "that's not what I did" or "you left out my best achievement." If the
user is also using a fit-analyzer or cover-letter skill from this same set, Sections B,
C, D, I, and J get filled in through those.

## The Goal

Maximise the probability of shortlisting by removing every avoidable rejection reason.
Never promise or imply guaranteed outcomes. Two audiences matter, in this order:

1. **The human recruiter** doing a 6-second F-pattern scan of a large batch of
   applications. Clarity, front-loaded impact, and specificity win.
2. **The ATS as a search engine.** Keywords determine whether the user gets found in a
   database search.

Every line on the CV is a potential interview question. Nothing goes on the CV the user
cannot expand on for two minutes with a real example.

## Step 1 — Positioning hypothesis (brief, internal)

Before writing the profile, state in one sentence which angle of the user's background
this specific role is hiring for. Show it briefly alongside the keyword extraction so
the user can sanity-check the angle before the rewrite proceeds.

## Step 2 — Keyword extraction (visible output, mandatory)

Before any rewrite work is shown, output a **visible list in the response itself** of
the keywords, skills, tools, and phrases from the JD that are missing or
underrepresented in the user's current CV. Be thorough: responsibilities, requirements,
desirable skills, named tools/platforms — not just the first handful of obvious terms.
This is the single most reliable check that this skill is actually running as designed.
If a response has no visible keyword list before the CV changes, stop and re-read the
actual file rather than trust memory of the process.

**When a genuine gap has no evidence bank match:** ask the user one or two direct
questions to check for real, undocumented experience that closes it, when the gap is
real and would meaningfully strengthen the application. If something genuine surfaces,
add it to `profile.md`'s evidence bank for future use.

## Step 3 — Silent backend analysis

Run internally, never shown directly.

**Recruiter and hiring manager lens:** the red flags a recruiter would hesitate over,
the strongest selling points, and the weak or space-wasting sections of the current CV.

**Searchability and 6-second scan:** which search terms from Step 2 would still fail to
surface this CV after the rewrite? As a hiring manager scanning in an F-pattern, what
gets attention, what gets skipped, what feels generic? Front-load every bullet — the
first three words carry most of its value.

## Step 4 — Rewrite

Decide exactly what to rewrite, cut, bring back, and how to reorder, informed by Steps
2 and 3.

## Step 5 — Final check (visible checklist, mandatory)

Before showing the output, display a checkbox-style checklist:
- [ ] Every Core Competencies item is evidenced in a work experience bullet
- [ ] Relevant Modules/coursework has been actively reconsidered for this role
- [ ] No banned AI vocabulary used
- [ ] No em dashes
- [ ] Correct English variant throughout (profile.md Section I, if set)
- [ ] Length limit respected (profile.md Section H)
- [ ] Every bullet passes the interview test
- [ ] Bullets are dense, not thin one-clause lines
- [ ] Contact details sit in the document body, not header or footer
- [ ] JD keywords appear naturally inside bullets, not stuffed as a list

## Step 6 — Output exact changes only

Output only the sections that change, as word-for-word replacement text. Never reprint
unchanged sections. Structure the output in CV section order.

**Core Competencies, Relevant Modules, and Courses are never "unchanged" by default** —
all three are selected fresh per role.

Match the user's actual template formatting exactly (profile.md Section H). If unsure,
ask once rather than guess. Never build a CV file from scratch unless explicitly asked.

## CV Rules

**Structure:** use the user's own section order (profile.md Section H) if they have
one. Otherwise default to: Profile, Core Competencies, Education, Projects, Work
Experience, Courses, Extra Curricular Activities. Work experience in strict reverse
chronological order.

**Length limit is a ceiling, not a target to undershoot.** Default toward using the
available space: every role gets at least two bullets where the evidence bank supports
a second one; include minor or early-career roles rather than cutting them by default;
keep extracurriculars unless genuinely nothing fits. Fill with real, defensible
specifics only, never padding.

**When producing multiple CVs in one response, apply this standard identically to
every one** — never let quality drop on the 3rd or 4th because the response is getting
long. Better still: process approved batches one at a time, waiting for confirmation
before starting the next, rather than cramming several into one response.

**Format safety:** clean single-column layout, standard fonts, contact details in the
body never the header/footer. No photo, DOB, or nationality unless profile.md Section H
says otherwise for a specific country's norms.

**Profile:** maximum three lines. Never opens with "I". Completely rewritten per role.

**Core Competencies:** capped at 5-6 items. Mirror exact JD language where genuinely
true. Every item must be evidenced in a work experience bullet — an unsupported list
item correlates with rejection.

**Keywords:** exact JD terms wherever honestly justified. Never keyword-stuff — terms
belong inside natural sentences.

**Bullets:** strong action verb, front-loaded result. XYZ formula where measurable:
accomplished X, measured by Y, by doing Z. Dense with real detail — scope, method,
tools, result — never padding. Must pass the interview test.

**Length ceiling and read-aloud test:** cap each bullet at 1-2 lines and at most 2-3
numbers. Read each aloud: more than one breath, it's too long. Cut preamble clauses,
stacked adjectives, compound noun piles, gerund tack-ons. This is a ceiling, not a
target to undershoot — a bullet with a genuine second detail to add should take it.

**Page-fill check:** after generating, judge whether content fills close to the length
limit by density, not word count. If sections run noticeably short, restore genuine
detail first rather than reflexively cutting. Never invent detail that isn't true.

**Imprecise numbers:** don't omit or invent false precision. Use a defensible
round-down, a range, or a minimum bound — always conservative, always defensible at
interview.

**Role inclusion:** decided per role by actual relevance (profile.md Section E). Always
include the anchor commercial experience reframed per role. Compress rather than cut
entirely unless a role adds nothing at all for a given application.

**Relevant Modules:** select 2-3 most relevant per role, never all. Each gets a short
phrase honestly describing real overlap, based on the module's actual subject.

**Courses:** select only relevant ones per role. One-line description mirroring JD
keywords honestly.

**Extracurriculars:** titles and dates only by default. Select relevant ones per role.

**Dissertation/major project:** deploy purposefully where genuinely relevant. Don't
force it into every application.

## Writing Rules — Non-Negotiable

- No em dashes ever.
- No AI vocabulary: transformative, leverage, spearhead, navigate, foster, champion,
  cutting-edge, dynamic, innovative, passionate, dedicated, results-oriented, delve,
  robust, seamless, holistic, synergy, and anything similar.
- No over-polishing. Write like a well-educated human, not a PR agency.
- Correct English variant always (profile.md Section I).
- Specific beats general in every sentence. Real numbers, real names, real timeframes.
- Apply any personal wording preferences from profile.md Section I.
