---
name: check-resume
description: Compare the user's résumé with one specific job description using Seeker (seekerscore.com), showing skill overlap, matched skills, missing required and preferred skills, and experience-level fit. Use when the user asks how well they fit a job, what is missing for a role, or whether to tailor their résumé for a posting.
---

# Check a résumé against one job

1. Get both texts: the résumé (plain text, or read a local file the user names) and the full job description
   (pasted, or a local file). If the user only gives a job URL, ask them to paste the description; do not fetch it.
2. Call the `check_resume_against_job` tool from the `seekerscore` MCP server with `resume_text` and
   `job_description`.
3. Report the skill overlap, matched skills, missing required skills, missing preferred skills, and the
   experience-level note, then the Seeker checker link.
4. If the user wants to improve the résumé for this job, suggest changes using only experience the résumé already
   shows. Never add skills, employers, dates or results the user has not stated; ask them instead.

Rules:
- The result is a skills comparison, not a prediction of interviews or hiring.
- Seeker does not apply to jobs from here.
