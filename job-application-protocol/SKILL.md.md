---
name: job-application-protocol
description: A complete job application system for tailoring a CV, writing cover letters, and answering application form questions against real job descriptions. Use this skill every time the user shares a job description, job advert, or vacancy link, asks to tailor their CV, asks for a cover letter, asks for help with application form questions, or asks for interview preparation. Trigger even if they just paste a JD with no instructions, or say "next" or name a company. Also use when they upload a new version of their CV for review.
---

# Job Application Protocol

Read `references/profile.md` before doing anything. It holds the user's fixed CV data,
established facts, evidence bank, module list, writing-voice notes, application tracker,
and any running logs (flagged listings, sector-collision notes, genuine-applications
log). Never ask the user for information that's already in that file.

**Whenever the user corrects a fact** — a wrong title, a gap that turns out to be
covered, a tracker entry that's actually sent not pending, a grade, anything — update
`profile.md` immediately in that turn, not just when explicitly asked to. The file is
only useful if it stays accurate.

## First-Run Setup (mandatory before Step 0, only when profile.md is empty or missing)

If `references/profile.md` doesn't exist yet, or exists but is essentially empty, do not
attempt to flag, tailor a CV, or write anything against a job description yet. Instead,
work through `references/PROFILE_TEMPLATE.md` with the user — a handful of questions per
round, not all at once — and save their answers into `references/profile.md` as you go,
using the template's own structure. This one-time setup is what prevents every later
correction of "that's wrong" or "you assumed something I didn't say."

If the user pastes a JD before setup is complete, it's fine to do a first pass with what
profile data exists and flag clearly which sections are still missing, rather than
blocking them entirely — but say plainly that the result will improve once the profile
is complete, and don't let an incomplete profile become the permanent state.

## The Goal

Maximise the probability of shortlisting by removing every avoidable rejection reason.
Never promise or imply guaranteed outcomes. Two audiences matter, in this order:

1. **The human recruiter** doing a 6-second F-pattern scan of a large batch of
   applications per vacancy. This person decides shortlisting. Clarity, front-loaded
   impact, and specificity win.
2. **The ATS as a search engine.** ATS platforms rarely auto-reject on content alone.
   Recruiters use keyword search to pull candidates from the database. Keywords
   determine whether the user gets found. Knockout questions (work authorisation,
   licences, location) are the real auto-filters.

Every line on the CV is also a potential interview question. Nothing goes on the CV
that the user cannot expand on for two minutes with a real example.

## Workflow — Follow In Order, Steps 0 Through 10

### Step 0 — Country mode (mandatory, before any other step)

Determine which country the JD is for, and check `profile.md` Section B for whether
that's the user's primary target country or a secondary one with its own rules (see the
Additional Country Mode section near the end of this file for how to build one). State
which mode is active. If a secondary-country JD gets processed with no mode
announcement, that's a drift signal — stop and re-check the file.

### Step 1 — Flag check

Before anything else, check the Application Tracker in `profile.md` for a matching
company and role. If this JD has already been processed, say so immediately and show
what happened last time rather than repeating the work from scratch.

Check the JD for genuine blockers before any work begins.

**Flag only these, checked against the user's own Standing Hard Exclusions
(`profile.md` Section D) — never against a generic assumption:**
- Hard skill/tool gaps the user has named as non-negotiable
- Driving licence requirements, if the user doesn't hold one for that country
- Security clearance requirements the user can't meet
- An explicit, structured years requirement in a *specific named sub-discipline* that
  doesn't match the user's actual specific background (e.g. "B2B marketing: 2 years
  (required)" when their real experience is a different specific area) — skip outright,
  these function as literal ATS knockout questions. This is different from a broad,
  generic "X years marketing experience" requirement the user is genuinely close to
  (per profile.md Section D's experience breakdown) — that stays a flagged, workable
  gap, not an automatic exclusion. The test is specificity: a narrow named sub-field
  they don't have vs. a general bar they're close to.
- Roles where the actual body text and duties are majority a different function (sales,
  reception, admin, operations) despite a matching-sounding title — skip outright, don't
  present as viable even if the title matched the search term.
- Sectors or work types on the user's own exclusion list (profile.md Sections C and D)
- Listings that appear to be scams, data harvesting, or a different job dressed up as
  the target role (see pattern below)
- Recruitment agency posts with no named employer (note it, don't block on it alone)
- Notably low review-site ratings if known
- Internships or fixed-term roles with a start date that collides with a deadline the
  user has told Claude about (dissertation, notice period, another commitment)
- Toxic-culture language: repeated "fast-paced" (3+ uses), "wear many hats," "like a
  family," "rockstar/ninja/guru," "unlimited vacation," or "competitive salary"/"DOE"
  with genuinely no figure anywhere. Note it briefly, don't auto-exclude on this alone
  unless combined with other flags.

**Never flag:** anything the user has explicitly said is settled (visa route already
confirmed workable, relocation already agreed, degree title already covers a stated
requirement) — see `profile.md`. Exception: a role requiring "permanent right to work
without restriction" as a *current-tense* eligibility gate (not a future start-date
question) is a genuine blocker if that's true of the user's actual status — flag these
explicitly, cross-checked against Section B.

**Field-sales-as-marketing (or similar bait-and-switch) pattern:** watch for vague
culture language with no named clients or sectors, phrases like "brand representation"
or "live campaign activity," multiple near-identical job titles from the same company, a
narrow or absent base salary paired with vague "performance-based progression," and
sometimes a long list of unrelated entry-level job titles pasted at the bottom of the
listing for SEO keyword capture. Two or more of these signs on a new listing → flag
hard, do not do CV work on it, verify with a quick web search for "[company] reviews."
Log confirmed instances in `profile.md`'s private tracking log (never in anything that
gets published or shared) so the same company doesn't need re-investigating next time.

**Scraped or reposted listings:** if the JD body text names a different employer than
the one listed on the posting, that's scraped content, not a real route to a job.
Redirect the user to search for the legitimate employer directly.

**Deadline collisions:** if the user has a known hard deadline (see `profile.md`), flag
any role whose start date or timeline would collide with it, and ask the user to check
the live listing directly rather than assume it's fine either way.

**Knockout question awareness:** if the JD or application form implies knockout
questions (work authorisation, licence, location, certifications), remind the user to
answer them accurately. These, not keywords, are what auto-reject.

If nothing to flag, say so in one line and proceed. If flagging, keep it brief and
direct, then wait for the user's go-ahead.

### Step 2 — Timing check

If the posting date is visible or findable, check it. Applications submitted within
48-72 hours of posting have materially better odds — many recruiters review in arrival
order and pause postings after a large volume of applications. If the posting is fresh,
tell the user to prioritise speed over extended polishing. If it's older than a week,
note that odds are reduced and the application should still be sent, but calibrate
expectations.

### Step 3 — Genuine-or-volume check

Classify the application as genuine or volume before any cover-letter or
application-answer work begins, and state the classification to the user.

**Genuine:** a real, specific reason for wanting this company that would survive an
interview follow-up question. Check `profile.md` for any standing genuine-category note
the user has set (e.g. a dissertation topic that's a real differentiator for certain
sectors) — deploy it prominently and honestly where it's a real fit, never force it
elsewhere.

**Volume:** an honest, general motivation (building experience, structural fit) with no
fabricated company-specific passion. This is the default for most applications unless
the user's profile sets a different default — it needs to stay honest, not invent
enthusiasm that wouldn't survive a follow-up question.

This classification drives cover letter tone in Step 10 if a cover letter follows.

**Reference benchmarking (genuine applications only, skip for volume):** for a role the
user has confirmed as genuinely wanted, search for 1-2 LinkedIn profiles of people who
hold or recently held a similar role, ideally at the same or a comparable company. Note
what language they use for skills, what they lead with, what they leave out. Use this
only to sanity-check word choice and structure, never copy content. Skip entirely for
volume applications.

**Company research (genuine applications only, skip for volume):** a quick web search
for recent news, mission, or a specific product/initiative beyond what's already in the
JD. The goal is one real detail for the cover letter that only someone who actually
looked the company up would know. Skip entirely for volume.

### Step 4 — Positioning hypothesis (brief, internal)

Before writing the profile, state in one sentence which angle of the user's background
this specific role is hiring for (e.g. "commercial/performance-focused" vs "structured
coordinator/operator" vs "content and research-minded generalist"). This stays a
one-line internal note, not a lengthy exercise. Show it briefly alongside the keyword
extraction so the user can sanity-check the angle before the rewrite proceeds. Its only
job is to stop the Profile, Core Competencies, and bullet choices from pulling in
slightly different directions within the same CV.

### Step 5 — Keyword extraction (visible output, mandatory)

Before any rewrite work is shown, output a **visible list in the response itself** — not
folded into silent analysis — of the keywords, skills, tools, and phrases from the JD
that are missing or underrepresented in the user's current CV. Be thorough: work through
the JD systematically (responsibilities, requirements, desirable skills, named
tools/platforms) rather than stopping at the first handful of obvious terms. This is the
single most reliable check that this skill is actually running as designed. If a
response involving this skill has no visible keyword list before the CV changes, stop
and re-read the actual file content rather than trust memory of the process.

**When a genuine gap has no evidence bank match:** before writing it off as permanent,
ask the user one or two direct questions to check whether there's real, undocumented
experience that closes it. Don't force this for every minor gap — use it when the gap is
real and would meaningfully strengthen the application. If something genuine surfaces,
add it to `profile.md`'s evidence bank for future use, not just this one CV.

### Step 6 — Silent backend analysis

Run the remaining analysis internally. Never show this output; feed the findings into
the rewrite.

**Recruiter and hiring manager lens:** identify the red flags a recruiter would hesitate
over, the strongest selling points that make the user competitive for this specific
role, and the weak, vague, repetitive, or space-wasting sections of the current CV.
Estimate interview likelihood honestly.

**Searchability and 6-second scan:** first, as a recruiter running keyword searches —
which search terms from the JD (including the Step 5 list) would still fail to surface
this CV after the rewrite? Second, as a hiring manager scanning in an F-pattern (across
the top, then down the left edge): what gets attention, what gets skipped, what feels
generic. Front-load every bullet with the strongest information — the first three words
carry most of its value.

### Step 7 — Rewrite

Decide exactly what to rewrite, cut, bring back, and how to reorder courses, informed by
Steps 5 and 6.

### Step 8 — Final check (visible checklist, mandatory)

Before showing the CV output, run through and **display a checkbox-style checklist in
the response**:
- [ ] Every Core Competencies item is evidenced in a work experience bullet
- [ ] Relevant Modules/coursework under Education has been actively reconsidered for
      this specific role, not left as a default
- [ ] No banned AI vocabulary used
- [ ] No em dashes
- [ ] Correct English variant throughout (per profile.md Section I)
- [ ] Length limit respected (per profile.md Section H)
- [ ] Every bullet passes the interview test (the user could talk through it for two
      minutes with a real example)
- [ ] Bullets are dense — scope, method and result packed in, not thin one-clause lines
- [ ] Contact details sit in the document body, not header or footer
- [ ] JD keywords appear naturally inside bullets, not stuffed as a list

This checklist's absence is itself the drift signal — if it's missing, the process
skipped a step.

### Step 9 — Output exact changes only

Output only the sections that change, as word-for-word replacement text. Never reprint
unchanged sections. Never explain changes unless flagging a concern. Structure the
output in CV section order so the user can work through their template top to bottom.

**Core Competencies, Relevant Modules, and Courses are never "unchanged" by default** —
all three are selected fresh per role by design, so all three belong in every single
output alongside Work Experience and Profile. A section is only genuinely "unchanged"
when nothing in the rules calls for it to be reselected.

**Match the user's actual template formatting exactly**, per `profile.md` Section H. If
unsure how a given section is formatted, ask once rather than guess and force the user
to reformat on their end.

Never build the CV file from scratch unless the user explicitly asks for a file — by
default, edit within their existing template.

### Step 10 — Offer the next artefact

After CV changes, ask one question only: whether the user needs a cover letter or
application form answers for this role. Do not write them unprompted.

Log this JD in the Application Tracker (`profile.md`) with today's date, company, role,
and status (Sent / Skipped — reason / Pending decision). A role flagged and skipped at
Step 1 gets logged immediately rather than waiting to reach this step.

## Sourcing Mode — Using a Connected Job-Search Tool

When the user asks to search for roles rather than pasting a specific JD, and a
connected search tool is available, use it without dumping full descriptions on them:

1. Run a search with relevant keywords (per `profile.md` Section C) and the user's
   target location(s).
2. Pull full details on every result in the batch before presenting anything — title
   alone is not a reliable signal. Apply the user's standing exclusions at this stage,
   before they ever see the list.
3. Present the full batch as a triage list — role, company, salary, link, and a status
   (Viable / Excluded — reason / Already in tracker), one line each. Show all of them,
   including exclusions and duplicates, not just the survivors. Never full job
   descriptions at this stage.
4. Wait for the user to say which ones to pursue. Never run the full workflow
   automatically.
5. For each one picked, the user checks the link themselves and confirms it's live
   before Claude runs the full Steps 0-10 workflow, including the Application Tracker
   check in Step 1.

**Sourcing Mode overrides to Step 9 and Step 10 — apply only to search-sourced JDs, not
directly pasted JDs:**
- Deliver the cover letter automatically, in the same response as the CV rewrite, using
  the Step 3 classification. Exception: for a genuine application, still ask for the
  user's actual personal reason first if it isn't already evident, per Cover Letter
  Rules.
- If the search tool has a platform-specific "relevant experience" or similar field,
  state the recommendation for it after every CV rewrite.

For directly pasted JDs, Step 10's normal behaviour applies.

**Standing search parameters** — pull from `profile.md` Section C and D rather than
guessing: target job titles, exclusions (tools, sectors, work types), visa/sponsorship
stance, location breadth, and whether these are volume applications by default.

## CV Rules

**Structure:** use the section order in `profile.md` Section H if the user has one.
Otherwise default to: Profile, Core Competencies, Education, Projects, Work Experience,
Courses, Extra Curricular Activities. Work experience in strict reverse chronological
order, never reordered by relevance.

**Length limit** (per `profile.md` Section H) is a ceiling to stay under, not a target
to undershoot. Default toward using the available space:
- Every role gets at least two bullets where the evidence bank actually supports a
  second one — a one-bullet role should be the rare exception, not the default.
- Include minor or early-career roles by default rather than cutting them, bringing in
  whichever is most relevant to the JD even for more senior-sounding roles — only leave
  one out when it genuinely fits nowhere.
- Keep extracurriculars unless genuinely nothing in them fits the role.
Same density rule as Bullets below applies throughout — fill with real, defensible
specifics only, never padding or filler. If a rewrite genuinely runs long, trim by
cutting the least relevant role or bullet first and say so.

**When producing multiple CVs in one response (a batch), this density and role-coverage
standard applies identically to every single one** — never let quality quietly drop on
the 3rd or 4th application because the response is getting long.

**Better still, avoid the batch problem entirely:** when the user approves several
applications at once, process them one per response, not crammed together — do the
first one properly, then wait for confirmation before starting the second.

**Format safety:** clean single-column layout, standard fonts, contact details in the
document body, never in the header or footer (parsers often skip headers and footers).
No photo, no date of birth, no nationality, unless `profile.md` Section H says
otherwise for a specific country's norms.

**Profile:** maximum three lines. Never opens with "I". Completely rewritten per role.
References the role context naturally, carries one or two exact JD keywords. Short,
sharp, specific.

**Core Competencies:** capped at 5-6 items. Mirror exact JD language where the user
genuinely has the skill. No invented skills. Every competency listed must also be
evidenced inside at least one work experience bullet — a skill that exists only as a
list item reads as an unsupported claim.

**Keywords:** use exact JD terms wherever experience honestly justifies them; mirror
closely where exact use is impossible. Never keyword-stuff — terms belong inside
achievement bullets in natural sentences, not in dense strings.

**Bullets:** every bullet starts with a strong action verb and front-loads the result or
the most impressive element. Use the XYZ formula where measurable: accomplished X,
measured by Y, by doing Z. Bullets should be dense with real detail — scope, method,
tools, and result — not thin single-clause statements, but density is not padding: no
filler adjectives, nothing added that the user couldn't defend in an interview. Every
bullet must pass the interview test: can the user talk about this for two minutes with a
real example? If not, it does not go on the CV.

**Length ceiling and read-aloud test:** cap each bullet at 1-2 lines and at most 2-3
numbers. Before finalising, read each bullet aloud: if it takes more than one breath,
it's too long, split or trim it. Cut preamble clauses ("Leveraging strong analytical
skills, managed..." → "Managed..."), stacked adjectives, compound noun piles, and
gerund clauses tacked onto the end. This ceiling caps how long a bullet may run — it is
not a target to undershoot. A bullet that's clearly under 2 lines but has a second true,
defensible detail to add should take it.

**Page-fill check (run after Step 8's checklist):** after generating, judge whether the
total content will fill close to the length limit — not by word count, but by density:
has real detail been trimmed away where a second true clause could have stayed in? If
sections are running noticeably short, that's underfilling, not good editing. Restore
genuine detail first rather than reflexively cutting. Only pad with vaguer language as
an absolute last resort, and never invent detail that isn't true.

**When an achievement is real but the exact number isn't certain:** don't omit the
number or invent false precision. Use a defensible round-down, a range, or a minimum
bound — always conservative, always something the user could defend if asked to justify
it at interview.

**Role inclusion:** decided per role using the user's own judgement of relevance (see
`profile.md` Section E) — always include the anchor commercial experience reframed per
role; include supporting roles for roles where they're genuinely relevant; compress or
reduce to one line elsewhere rather than cutting entirely, unless a role adds nothing
at all for a given application.

**Relevant Modules/coursework (under Education):** select 2-3 most relevant per role
from the full list in `profile.md`, never all of them. Each selected module gets a short
phrase honestly describing its real overlap with the role, based on the module's actual
subject — never inventing specific coursework or content it didn't cover.

**Courses:** select only relevant ones per role, never all by default. Each selected
course gets a one-line description mirroring JD keywords honestly.

**Extracurriculars:** titles and dates only, no descriptions by default unless the
user's template uses more. Select relevant ones per role.

**Dissertation/major project:** a strategic asset for roles where it's genuinely
relevant (per `profile.md`). Deploy purposefully with reframed bullets. Do not force it
into every application.

## Writing Rules — Non-Negotiable, All Outputs

- No em dashes ever. Commas, full stops, or restructure.
- No AI vocabulary. Banned: transformative, leverage, spearhead, navigate, foster,
  champion, cutting-edge, dynamic, innovative, passionate, dedicated, results-oriented,
  delve, robust, seamless, holistic, synergy, and anything similar. If about to use one,
  stop and rewrite.
- No over-polishing. Write like a well-educated human, not a PR agency. Recruiters
  actively reject applications that read AI-generated, so this is a survival rule, not a
  style preference.
- Correct English variant always, per `profile.md` Section I.
- Specific beats general in every sentence. Real numbers, real names, real timeframes.
- Apply any personal wording preferences from `profile.md` Section I.

## Cover Letter Rules

**Length:** shorter is winning. 200-300 words, one page, three short paragraphs.
Current research shows recruiters and screening tools both penalise long, story-heavy
letters — the signal that matters is one relevant detail, one real metric, and one
specific point, not exhaustive coverage.

**Addressing:** always try for a named contact. Check the JD, then suggest the user
checks LinkedIn or calls the company to ask who is handling recruitment. "Dear Hiring
Team" only as a last resort.

**Vary the structure every single time — this is the actual fix, not a style note.**
The single biggest tell of generic AI output isn't any one phrase, it's *sameness
across letters*: the same opener, the same paragraph order, the same rhythm, repeated.
Before writing, deliberately choose a different entry point than the last few letters
used — lead with a number, a direct question, a specific product/detail, a short
anecdote, or a plain statement of fact about the company, never the same formula twice
in a row.

**Banned phrases:** "I am writing to express my interest," "detail-oriented
professional," "proven track record," "passionate about," "What appealed to me about
this role is..." as a default opener. Already-banned AI vocabulary (Writing Rules)
still applies throughout.

**One real detail beats general enthusiasm.** Name one specific thing — a number from
the JD, a product, a client type, a detail only someone who actually read this posting
would know — rather than a general statement that could apply to any similar company.

**Structure, loosely, in whatever order fits the specific role — not a fixed template:**
- The one honest, specific reason for this company (genuine) or the one honest
  structural reason (volume) — stated plainly, not padded
- One real piece of evidence from the evidence bank, chosen for actual relevance to
  this JD, with a number attached
- A closing line that's forward-looking, not a repeated formula

**Personal voice:** draw on the user's own stated voice or stories (profile.md Sections
E and I) when genuinely relevant to the JD's own language — not automatically in every
letter.

**Read-aloud test before finalising:** would the user actually say this sentence to
someone in conversation? If not, rewrite it plainer.

**Before writing any cover letter,** ask the user for their genuine personal reason for
wanting the role if it isn't already evident, for genuine applications. Volume
applications write directly.

**For roles requesting writing samples or a portfolio:** only offer this if
`profile.md` confirms the user has one ready to show.

**Before finalising, self-check silently:** under 300 words, no banned phrase, opener
genuinely different from recent letters, named contact attempted, one real specific
detail present, no em dash, correct English variant. Only surface this checklist
visibly if something fails it; otherwise just deliver the corrected letter.

## Application Form Answers

First person, the user's voice, all writing rules apply. Use evidence bank stories where
relevant rather than generic claims. Hit word or character limits as closely as possible
without exceeding. For motivation questions, ask the user for their honest answer first,
then shape it — unless `profile.md` Section J says to draft directly for volume
applications. For competency questions, structure as STAR without labelling the parts.
For "top skills" selection questions, choose only skills defensible with a real example
at interview.

## Interview Preparation

When the user gets an interview or phone screen: identify what stage it is and what it
actually tests, predict the likely questions from the JD and their application, and
draft answers grounded in the evidence bank and profile. Answers are scripts to
internalise, not recite. For "tell me about yourself," lead with who they are as a
person, not a CV readout. Research the company with current sources before prepping
them. Flag logistics: quiet location, CV in hand, save the caller's number, pause before
answering.

## Additional Country Mode — Template for a Secondary Target Country

If the user is applying to more than one country, build one of these blocks per
secondary country, sourced from the user directly or current research at the time,
never assumed:

- Language fluency requirements as a current-tense gate (flag like a right-to-work
  exception, not a soft nice-to-have)
- Visa/sponsorship mechanics specific to that country, and any minimum salary threshold
  tied to a sponsored route
- Any country-specific CV or cover letter norms (photo expectations, personal detail
  norms, tone conventions)
- A standing note that the user's source material for these facts should be checked
  against the employer's own stated policy if the two ever conflict — flag the
  conflict rather than silently picking one, and re-verify country-specific rules
  periodically since they change.
