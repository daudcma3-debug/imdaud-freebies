# 5 free Claude skills for office & finance work (from awesome-claude-skills)

*21 Nov 2026 · By Abu Daud, CMA · WhatsApp +966 57 561 5384*

Five free skills worth trying first, picked from **[ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)** (~80k ⭐, a curated list by Composio). Each link goes to the author's own SKILL.md — nothing is copied here.

> **Licence:** the list's README says Apache 2.0, but GitHub shows no repo-level licence file and the README notes individual skills may differ. Check each skill before you use it.

| # | Skill | What it does | Free? | Author / licence | Link |
|---|---|---|---|---|---|
| 1 | **Invoice Organizer** | Reads messy invoices and receipts, renames them consistently and sorts them into folders for tax prep | Free | Composio list · Apache 2.0 per README | [invoice-organizer](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/invoice-organizer/SKILL.md) |
| 2 | **File Organizer** | Finds duplicates, suggests a better folder structure and cleans up | Free | Composio list · Apache 2.0 per README | [file-organizer](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/file-organizer/SKILL.md) |
| 3 | **Postgres (read-only)** | Runs read-only SQL against PostgreSQL; blocks INSERT, UPDATE, DELETE, DROP | Free | sanjay3290/ai-skills · Apache 2.0 | [skills/postgres](https://github.com/sanjay3290/ai-skills/blob/main/skills/postgres/SKILL.md) |
| 4 | **Meeting Insights Analyzer** | Reads meeting transcripts and gives feedback on speaking habits and communication patterns | Free | Composio list · Apache 2.0 per README | [meeting-insights-analyzer](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/meeting-insights-analyzer/SKILL.md) |
| 5 | **Content Research Writer** | Helps research, outline and draft content with citations and better hooks | Free | Composio list · Apache 2.0 per README | [content-research-writer](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/content-research-writer/SKILL.md) |

## How to add a skill to Claude (from Anthropic's help article)

1. Download the skill's folder and package it as a **ZIP** (the folder must contain the SKILL.md).
2. In Claude, go to **Customize → Skills**.
3. Click **+** → **Create skill** → **Upload a skill**, and upload the ZIP.
4. Toggle it on. Code execution must be enabled (Settings → Capabilities).

Skills are available on Free, Pro, Max, Ultra, Team and Enterprise plans. Skills enabled in Claude also sync to Claude Code when you sign in with the same account (run `/skills` to see them).
Source: [support.claude.com/en/articles/12512180](https://support.claude.com/en/articles/12512180)

## 5-point safety check before installing any community skill

1. **Read the SKILL.md** — know exactly what it tells Claude to do.
2. **Open every script** — look for network calls, installs or anything that sends data out.
3. **Check the licence** — per skill, not just the list.
4. **Limit data access** — databases read-only, folders you choose, no client files.
5. **Test on demo files first** — never on real ledgers or invoices on day one.

Anthropic's guidance: only install skills from trusted sources, and review less-trusted skills before enabling them (prompt injection and data exfiltration are the main risks).

**Free PDF version:** [Community Claude Skills Starter Guide](../freebies/Community-Claude-Skills-Starter-Guide.pdf)

## Sources (checked 21 Nov 2026)
- github.com/ComposioHQ/awesome-claude-skills — public, 79,985 stars, last push 18 Sep 2026
- github.com/sanjay3290/ai-skills — public, Apache 2.0, 457 stars, last push 2 Nov 2026
- support.claude.com/en/articles/12512180 — Using Skills in Claude

---
By **Abu Daud, CMA** · Finance & Accounting AI Agents and Automations · WhatsApp +966 57 561 5384 · Instagram [@imdaud](https://instagram.com/imdaud)
