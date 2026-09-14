# Job Application Skills

A set of AI assistant skills for tailoring CVs, writing cover letters, screening job
listings for red flags, and answering application form questions — built for use with
Claude Skills, and adaptable to ChatGPT Custom GPTs or Gemini Gems.

## What's here

- **job-application-protocol/** — the full compiled system, everything in one skill
- **job-fit-flag-analyzer/** — screens a job description for red flags and dealbreakers before you invest time
- **cv-tailoring-engine/** — rewrites your CV against a specific job description
- **cover-letter-writer/** — writes a tailored, non-generic-sounding cover letter
- **application-qa-assistant/** — answers open-text application questions in your own voice

## Setup

Each skill needs your own profile filled in before it can do anything useful. Copy
`references/PROFILE_TEMPLATE.md` from any of the folders above, and either:

1. Paste it into a new conversation with the AI assistant and answer its questions, or
2. Fill it in yourself first, then upload it alongside the skill.

None of these skills come with anyone's personal data pre-filled — the template is
blank by design.

## Using with Claude

Upload the whole folder (containing `SKILL.md` and a `references/` folder) as a Skill
in Claude's settings.

## Using with ChatGPT or Gemini

Use the files in `other-ai-versions/` — paste the `_INSTRUCTIONS.md` content into the
Instructions field when building a Custom GPT or Gem, and upload the matching
`PROFILE_TEMPLATE` (and, for the compiled version, `_FULL_REFERENCE.md`) as a Knowledge
file.
