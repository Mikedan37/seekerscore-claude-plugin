---
description: Check your résumé against one job description with Seeker (skill overlap and what is missing)
argument-hint: "[résumé file] [job description file]"
---

Compare the user's résumé with one job description using Seeker.

Inputs: $ARGUMENTS

1. If two file paths were given above, the first is the résumé and the second is the job description; read both.
   If one is missing, ask the user to paste it. If the user only has a job URL, ask them to paste the description
   instead of fetching it.
2. Leave out the phone number and home address from the résumé. Both texts need at least 200 characters.
3. Call `check_resume_against_job` from the `seekerscore` MCP server once, with `resume_text` and `job_description`.
4. Report the skill overlap percentage, the matched skills, missing required skills, missing preferred skills, the
   experience-level note, and the Seeker checker link.
5. If the user wants to tailor the résumé, suggest changes using only experience the résumé already shows. Never add
   skills, employers, dates or results the user has not stated; ask them instead.

Rules: this is a skills comparison, not a prediction of interviews or hiring. Seeker does not apply to jobs from here.
