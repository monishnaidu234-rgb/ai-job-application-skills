---
name: cover-letter-writer
description: Writes a tailored cover letter for a specific job description, with built-in rules against generic AI-sounding openers and structure, and honest handling of skill gaps. Use whenever the user asks for a cover letter for a role, or after tailoring a CV when they say yes to one.
---

# Cover Letter Writer

Read `references/profile.md` before doing anything. This skill relies on Sections A, C,
E, I, and J specifically — identity, genuine/volume default, evidence bank, writing
voice, and application-answer preferences. Never ask the user for information already in
that file.

**Whenever the user corrects a fact — their real reason for wanting a role, a detail
they don't want mentioned — update `profile.md` immediately in that turn.**

## First-Run Setup (mandatory before first use)

If `references/profile.md` doesn't exist yet or is essentially empty, work through
`references/PROFILE_TEMPLATE.md` Sections A, C, E, I, and J with the user first — a few
questions at a time. This prevents a letter that sounds nothing like them, or that
raises something they'd rather leave out. If the user is also using a fit-analyzer or CV
skill from this set, the remaining sections get filled in through those.

## Before Writing

Confirm (or infer from context if already established in the conversation) whether this
application is genuine or volume:

- **Genuine:** a real, specific reason for wanting this company that would survive an
  interview follow-up question. Ask the user for their honest personal reason if it
  isn't already evident — their real words outperform an inferred motivation, worth the
  one-question pause.
- **Volume:** an honest, general motivation, no fabricated company-specific passion.
  Write directly without pausing to ask, unless the user's profile says otherwise.

## Length

Shorter is winning. 200-300 words, one page, three short paragraphs. Recruiters and
screening tools both penalise long, story-heavy letters — one relevant detail, one real
metric, one specific point beats exhaustive coverage.

## Addressing

Always try for a named contact. Check the JD, then suggest the user checks LinkedIn or
calls the company to ask who's handling recruitment. "Dear Hiring Team" only as a last
resort.

## Vary the Structure Every Single Time

This is the actual fix for AI-sounding output, not a style note. The single biggest
tell isn't any one phrase, it's *sameness across letters* — the same opener, the same
paragraph order, the same rhythm, repeated. Before writing, deliberately choose a
different entry point than the last few letters used: lead with a number, a direct
question, a specific product/detail, a short anecdote, or a plain statement of fact
about the company. Never the same formula twice in a row.

## Banned Phrases

"I am writing to express my interest," "detail-oriented professional," "proven track
record," "passionate about," "What appealed to me about this role is..." as a default
opener. General banned AI vocabulary still applies throughout (see Writing Rules).

## One Real Detail Beats General Enthusiasm

Name one specific thing — a number from the JD, a product, a client type, a detail only
someone who actually read this posting would know — rather than a general statement
that could apply to any similar company.

## Structure — Loose, Not a Fixed Template

- The one honest, specific reason for this company (genuine) or the one honest
  structural reason (volume) — stated plainly, not padded
- One real piece of evidence from the evidence bank, chosen for actual relevance, with
  a number attached
- A closing line that's forward-looking, not a repeated formula

## Handling Gaps Honestly

If the JD names a requirement the user's profile confirms is a real gap, name it
plainly and briefly rather than either overclaiming or avoiding it entirely — one
sentence stating it directly reads as more credible than working around it. Follow
immediately with what the user does bring instead.

## Personal Voice

Draw on the user's own stated voice or stories (profile.md Sections E and I) when
genuinely relevant to the JD's own language — not automatically in every letter.

## Read-Aloud Test

Before finalising: would the user actually say this sentence to someone in
conversation? If not, rewrite it plainer.

## Writing Samples or Portfolio

Only offer to mention these if the user's profile confirms they have something genuinely
ready to show an employer — an unfinished personal project can work against the
applicant if linked before it's presentable.

## Self-Check Before Finalising

Silently confirm: under 300 words, no banned phrase, opener genuinely different from
recent letters, named contact attempted, one real specific detail present, no em dash,
correct English variant. Only surface this checklist visibly if something fails it —
otherwise just deliver the corrected letter.

## Writing Rules — Non-Negotiable

- No em dashes ever.
- No AI vocabulary: transformative, leverage, spearhead, navigate, foster, champion,
  cutting-edge, dynamic, innovative, passionate, dedicated, results-oriented, delve,
  robust, seamless, holistic, synergy, and anything similar.
- No over-polishing. Write like a well-educated human, not a PR agency.
- Correct English variant always (profile.md Section I).
- Specific beats general. Real numbers, real names, real timeframes.
