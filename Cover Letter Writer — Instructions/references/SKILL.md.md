# Job Application Profile — Template

This file is both a **template** (the structure a filled-in profile follows) and an
**onboarding script** (the questions Claude should ask to fill it in). Every section
below has a short "Ask:" note showing what to ask the user if that section is empty.

**How this file gets used:** the first time any skill in this set is run and this file
is empty or missing, Claude should not proceed with flagging, CV, cover letter, or
application-answer work. Instead, work through the sections below in a handful of short
rounds — 3-5 questions per round, not forty at once — confirming and saving progressively.
The goal is that once this is filled in properly, the user should never have to come back
later and say "that's wrong" or "you assumed something I didn't say." Every fact this
profile is missing is a fact Claude will otherwise have to guess, and a guess is exactly
what causes rework.

Do not invent, infer, or upgrade anything the user hasn't stated. If a section is
optional and the user has nothing to add, leave it explicitly marked "Not provided" —
don't skip it silently, since a silent gap looks identical to "asked and got nothing."

---

## A. Identity & Contact

- Full name:
- Email:
- Phone (with country code if applying internationally):
- Current location (city, country):
- LinkedIn URL (if any):
- Portfolio/personal site (if any, and whether it's ready to be shown to employers or still in progress):

**Ask:** "What's your name, email, phone number, and current city? Do you have a LinkedIn
profile or personal site you want linked on applications — and if you have a site, is it
finished enough to show an employer, or still a work in progress?"

## B. Right to Work & Location

- Country/countries you're applying in:
- Right-to-work status (citizen / permanent resident / current visa route and what it allows / would need employer sponsorship):
- If on a visa: what it currently allows (full-time work? a future date when that changes, e.g. a post-study work route?) and any date that status changes:
- Willing to relocate: (not at all / within one region / nationwide / internationally — specify)
- Any locations that are a hard no regardless of the role:

**Ask:** "What country or countries are you applying in? What's your right-to-work
status there — are you a citizen, permanent resident, or on a visa? If on a visa, what
does it currently let you do, and is there a date when that changes? Are you open to
relocating, and if so how widely?"

**Why this matters:** this is what lets Claude tell the difference between a role that
genuinely can't sponsor you and one that's simply badly worded, and stops Claude from
either wrongly flagging a non-issue or wrongly ignoring a real one.

## C. Career Target

- Job titles / functions you're targeting (list several — search terms vary a lot for the same real job):
- Target seniority (internship / placement / graduate entry-level / 1-3 years experience / more senior):
- Industries or sectors you want, if you have a preference:
- Industries, sectors, or company types that are an automatic no, regardless of the specific role or salary (e.g. gambling, defence, tobacco, alcohol, adult content, a specific competitor, animal testing, fast fashion — whatever is genuinely true for you, not a guess Claude makes):
- Default classification: do you generally want to apply broadly to many roles (a shorter, honest, general cover letter each time) or more selectively to fewer roles you're genuinely excited about (deeper research, a more specific letter)? This can be overridden per application, but needs a sensible default.

**Ask:** "What job titles are you targeting? What level — internship, graduate,
early-career? Any industries you want to work in, or any you want to rule out
completely regardless of how good the role looks otherwise? And by default, do you want
to apply broadly and quickly to lots of roles, or more selectively to fewer roles you
research properly?"

## D. Standing Hard Exclusions

This is the single most important section for making sure Claude never has to be told
"you got this wrong" twice. List anything that should cause a role to be skipped
outright, regardless of how good it otherwise looks, and regardless of what the job
title says.

- Driving licence: do you hold one for the country you're applying in? (if not, any
  role requiring one is an automatic skip)
- Tools/platforms/software you do **not** have real experience in, that commonly show
  up as requirements (name specific ones — e.g. a specific CRM, a specific analytics
  tool, a specific design suite, a specific ad platform):
- Types of work you will not do regardless of job title (e.g. hands-on video/photo
  production, cold calling, door-to-door or street canvassing, night shifts, physical
  labour, roles requiring a background check you can't pass):
- Sectors that are an automatic exclusion (see also Section C — list here if it's about
  the *type of work* rather than the *type of company*, e.g. "nothing healthcare-adjacent"
  vs "nothing in the gambling industry"):
- Security clearance limitations:
- Minimum acceptable salary, if you have one:
- Contract type constraints (must be permanent / open to fixed-term / must be full-time / open to part-time):
- Working pattern constraints (must be remote / hybrid is fine / on-site is fine /
  cannot work certain days or hours):
- Years-of-experience honesty check: what's your actual total experience, broken down
  by discipline (e.g. "17 months paid media, 3 months SEO" rather than one combined
  number) — this lets Claude tell a narrow, unmatched requirement apart from a broad one
  you're genuinely close to.

**Ask:** "Let's make sure I never send you something you'd reject on sight. Do you have
a driving licence? Are there any tools or platforms you know come up a lot in job ads
that you genuinely don't have experience with? Any type of work — regardless of title —
you won't do? Any sectors that are a hard no? Any salary floor, contract type, or
working-pattern requirement I should treat as non-negotiable?"

## E. Evidence Bank — Work History

For each role, in reverse chronological order: employer, title, dates, location, and
3-5 real achievements with numbers wherever the user can honestly attach one. If a
number isn't exact, use the estimation guidance below rather than either inventing false
precision or dropping the number entirely.

*(repeat this block per role)*
- Employer:
- Title:
- Dates:
- Location:
- Achievements (what you actually did, what changed because of it, any number attached):

**Ask, per role:** "Walk me through this role — what did you actually do day to day,
and what's the best evidence you have that it worked? Any numbers — even rough ones?"

**If a number isn't exact:** ask "roughly how much/many was it?" and use a defensible
round-down ("75+ hours" if they think it was around 100), a range ("8-12 accounts"), or
a minimum bound ("400+ engagements") — always conservative, always something the user
could justify if asked to explain it at interview. Never invent a number they haven't
given some basis for.

**Ask for standalone stories** that don't map to one specific job but come up across
many applications regardless of the specific role:
- A time you found and fixed a real problem, especially one nobody asked you to fix
- A time you negotiated or persuaded someone, and what specifically worked
- A time you solved something creatively — not a textbook answer, an actual workaround
- A time you worked well as part of a team, or led one
- A time something went wrong and you were the one who dealt with it
- Their proudest achievement, in their own words, before Claude reshapes it

Don't force every category — some people won't have a clean story for all of them.
Capture what's genuinely there rather than manufacturing an answer to fit the list.

## F. Education

- Degree, institution, dates, subject (repeat per qualification):
- Grade/classification, and whether the user wants it stated on applications (don't
  assume either way — ask explicitly):
- Dissertation/thesis topic and methodology, if relevant to any target roles:
- Full list of modules/coursework completed (used to select 2-3 relevant ones per
  application, never all of them):
- Courses, certifications, or short programmes completed: name, provider, dates, and a
  one-line honest description of what it actually covered:

**Ask:** "What's your education history — degree, institution, dates, subject? Do you
want your grade included, or would you rather leave it off applications? Any
dissertation or major project worth using for relevant roles? What modules did you
study, and any short courses or certifications outside your degree?"

## G. Confirmed Skills vs Gaps

- Tools/platforms/skills you're confident and evidenced in (list specifically, not
  vaguely — "Google Ads and Meta Ads Manager, hands-on for 17 months" not "digital
  marketing"):
- Tools/platforms/skills that come up often in job ads that you do **not** have —
  distinct from Section D's hard exclusions, this list is for things that are a
  *gap to name honestly*, not an automatic skip:
- Anything you're actively developing and would rather have named as "developing" than
  either overclaimed or hidden:

**Ask:** "What tools or platforms are you genuinely confident in, with real experience
behind them? Separately, what comes up a lot in job ads that you don't have — things
that are a real gap worth naming honestly, but not a dealbreaker on their own?"

## H. CV Format

- Do you already have a CV template with a fixed layout and section order Claude should
  edit within, or do you want one designed from scratch?
- If you have one: section order, and how each section is actually formatted (bulleted
  list vs plain paragraph, etc. — ask once rather than guess and cause reformatting work)
- Length constraint (one page / two pages / other):
- Personal details you do or don't want included (default to excluding photo, date of
  birth, nationality, marital status unless the user says otherwise for a specific
  country's norms):

**Ask:** "Do you already have a CV template I should be editing inside, or should I help
build the structure from scratch? What's your length limit? Anything you specifically
want left off — like a photo or date of birth — or included?"

## I. Writing & Tone

- English variant (UK / US / Australian / Canadian / other):
- Words or phrases the user personally dislikes, or that don't sound like them:
- How the user would describe their own natural writing voice (formal, conversational,
  dry, warm, direct, other):
- Cover letter length preference, if different from a skill's default:

**Ask:** "Which English spelling convention do you want — UK, US, or something else? Is
there any wording you specifically don't want used, or that doesn't sound like you? How
would you describe how you naturally write or talk?"

## J. Application Answer Preferences

- How personal should application-form answers get by default — fully tailored with
  real personal stories each time, or safer and more general while still honest?
- Any topics the user would rather Claude not raise even if technically relevant (a
  specific past employer, a gap period, a personal circumstance)?

**Ask:** "For open-text application questions — like 'tell us about a time you...' —
do you want me to draw on real personal stories every time, or keep things a bit more
general by default? Is there anything you'd rather I never bring up, even if it's
technically relevant?"

## K. Tracking Preferences

- Keep a running log of every role processed (company, role, date, status)? Defaults to
  yes — this is what stops the same JD getting reprocessed from scratch and lets the
  user ask "did I already do this one?"
- Keep a private log of listings that were flagged as scam-pattern or otherwise
  untrustworthy, for the user's own future reference? Defaults to yes, but never
  publish this log anywhere public — see the note on this in each skill file.

---

## Notes for Claude, Not for the User

- This file is filled in progressively, not all at once. If the user answers Section A
  and B and then moves on to pasting a job description, that's fine — proceed with what
  exists, and pick up the remaining sections naturally as they become relevant (e.g. ask
  Section E's questions the first time a CV rewrite actually needs a specific role's
  detail, rather than insisting on a full interview before any use is possible).
- Never publish, quote, or export this file, or any specific fact from it, into a public
  repository, a shared skill, or anywhere outside this user's own private storage. If
  the user asks to publish or share the skill itself, the shared version must ship
  empty, using this template file itself, never their filled-in answers.
- If the user corrects a fact here later, update this file immediately in that turn.
  Don't wait to be asked twice.
