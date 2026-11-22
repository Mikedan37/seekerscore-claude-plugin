---
description: Match your résumé to live job postings on Seeker (top 5 fits with links)
argument-hint: "[path to résumé file, or leave empty to paste it]"
---

Match the user's résumé to live jobs with Seeker.

Résumé source: $ARGUMENTS

1. If a file path was given above, read that file as the résumé. For a PDF or DOCX, extract the text if you can;
   otherwise ask the user to paste it. If nothing was given, ask the user to paste their résumé text and stop there.
2. Leave out the phone number and home address before sending; they are not needed.
3. If the résumé text is under 200 characters, ask for the full résumé instead of calling the tool.
4. Call `match_resume` from the `seekerscore` MCP server once, with `resume_text`. It can take up to a minute;
   tell the user it is checking live jobs.
5. Show each match as a short list: title, company, location, fit label, the reason, and the posting link.
   End with the "See all your matches on Seeker" link the tool returned.

Rules: show only jobs the tool returned, never invent jobs, companies or links. Fit labels describe how well the
résumé matches a posting; never call them interview or hiring odds. Seeker does not apply to jobs from here. If the tool
says it "could not finish the match right now", call it once more with the same résumé (the second call picks up the
finished result). If that fails too, or the tool reports a limit or that it is busy, say so and give the link it
returned. Never call it a third time.
