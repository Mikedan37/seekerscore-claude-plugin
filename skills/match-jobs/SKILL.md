---
name: match-jobs
description: Find live, open jobs that fit the user's résumé using Seeker (seekerscore.com). Use when the user shares a résumé or CV (pasted text or a local file) and asks which jobs fit them, what to apply to, or to search jobs for their background.
---

# Match a résumé to live jobs

1. Get the résumé as plain text. If the user points to a local file (.md, .txt), read it. For a PDF or DOCX, read it
   if you can extract text; otherwise ask the user to paste the text. Ask before reading any file they did not name.
2. Leave out the phone number and home address; they are not needed.
3. Call the `match_resume` tool from the `seekerscore` MCP server with `resume_text`. Matching can take up to a minute.
4. Show each match: title, company, location, fit label, the short reason, and the posting link. Then the
   "See all your matches on Seeker" link.

Rules:
- Never invent jobs, companies or links. Show only what the tool returned.
- Fit labels describe how well the résumé matches a posting. Never call them interview or hiring odds.
- Seeker does not apply to jobs from here. If the user wants to apply, point them to the posting link or to Seeker.
- A first match on a new résumé can take longer than one call allows. If the tool says it "could not finish the match
  right now", call it once more with the same résumé: the second call picks up the finished result. If that fails
  too, or the tool says it is busy or at a limit, tell the user and give the Seeker link it returned. Never call it a
  third time.
