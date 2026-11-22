# Seeker for Claude

Match your résumé to live job postings and check it against a specific job description, inside Claude Code,
claude.ai and Cowork. Powered by [Seeker](https://www.seekerscore.com).

## Install (Claude Code)

```
claude plugin marketplace add Mikedan37/seekerscore-claude-plugin
claude plugin install seekerscore@seekerscore
```

Then, in any project:

```
/seekerscore:match ~/resume.md              # top 5 live jobs for your résumé, with links
/seekerscore:check ~/resume.md ~/job.txt    # skill overlap and what is missing for one job
```

You can also just ask ("which open jobs fit my résumé in resume.md?") and the plugin's skills call Seeker for you.

Or add the connector directly (any Claude plan, Settings → Connectors → Add custom connector):
`https://www.seekerscore.com/mcp`

## What it does

| Tool | What you get |
|---|---|
| `match_resume` | The 5 live postings that best fit your résumé, from Seeker's 350,000+ jobs: title, company, location, fit label, reason, link. Takes up to a minute; the first match for a new résumé can need a second call, which the plugin makes once. |
| `check_resume_against_job` | Skill overlap with one job description, matched skills, missing required and preferred skills, experience-level fit. |

Both tools are **read-only**. Seeker never applies to jobs from here and needs no account.
Fit labels and overlap describe how well a résumé matches a posting; they are not interview or hiring odds.

## Privacy

Your résumé text (and the job description, for the check) is sent to Seeker only when you ask, to compute the
result. It is handled the same way as a résumé uploaded on seekerscore.com, as described in the privacy policy.
Leave out your phone number and home address; they are not needed. Full policy:
https://www.seekerscore.com/legal/privacy

## Limits

A few matches per person every 10 minutes and a daily cap, so the service stays fast for everyone.

## Support

https://www.seekerscore.com/legal · support@seekerscore.com
