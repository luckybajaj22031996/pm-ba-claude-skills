# PM/BA Skill Pack — Custom Claude AI Skills

**5 ready-to-use Claude skills for Product Managers and Business Analysts.**

These aren't prompts. They're permanent Claude skills you install once — Claude uses them automatically whenever you ask for a PRD, user stories, meeting notes, market research, or stakeholder updates.

---

## What's Inside

| Skill | What It Does |
|-------|-------------|
| **PRD Generator** | Generates Product Requirements Documents in .docx. Interactive section picker (15 sections). Flags missing info as placeholders instead of hallucinating. |
| **User Story Writer** | Creates user stories with acceptance criteria (Given-When-Then or checklist) and edge cases from feature descriptions, PRDs, or raw notes. |
| **Meeting Synthesizer** | Turns messy meeting notes into structured summaries — decisions, action items (with owners + deadlines), key points, and open questions. |
| **Market Research** | Uses live web search to pull real competitor data, market sizing (TAM/SAM/SOM), trend analysis, direct + indirect competitor breakdown, and SWOT. |
| **Stakeholder Updates** | Generates weekly sprint or monthly leadership updates with RAG status (Red/Amber/Green), blockers, upcoming milestones, and decision requests. |

## What Makes These Different

- **They generate actual .docx files** — not chat responses you copy-paste into a doc
- **They never fabricate content** — if context is missing, they mark it as `[PLACEHOLDER: what's needed]`
- **Interactive workflows** — section pickers, format choices, output options
- **Auto-triggering** — say "create a PRD" and Claude knows which skill to use
- **Install once, use forever** — no subscription, no recurring anything

## Requirements

- Claude **Pro**, **Max**, **Team**, or **Enterprise** plan
- **Code execution and file creation** enabled (Settings → Capabilities)

## Installation

### Option 1: Claude.ai (Recommended)

1. Download the `.skill` file(s) you want from the [`skills/`](./skills/) folder
2. Open Claude → Settings → Customize → Skills
3. Click **Upload Skill**
4. Select the `.skill` file
5. Toggle it **ON**

That's it. Start a new conversation and ask Claude to create a PRD, write user stories, etc.

### Option 2: Claude Code

```bash
mkdir -p ~/.claude/skills
unzip skills/prd-generator.skill -d ~/.claude/skills/prd-generator
# Repeat for each skill you want
```

## Quick Test

After installing, try these prompts:

```
"Create a PRD for a task management app for remote teams"

"Write user stories for a password reset feature"

"Summarize these meeting notes: [paste your notes]"

"Do market research for a food delivery app in India"

"Write a weekly stakeholder update for my project — we completed the API integration, 
but the design review is blocked waiting on the UX team"
```

## File Structure

```
skills/
├── prd-generator.skill
├── user-story-writer.skill
├── meeting-synthesizer.skill
├── market-research.skill
└── stakeholder-updates.skill
docs/
└── Setup_Guide.docx
```

## How Skills Work (For the Curious)

Each `.skill` file is a zip containing a `SKILL.md` — a markdown file with YAML frontmatter (name + description) and detailed instructions for Claude. When you install a skill, Claude reads the description to know *when* to use it, and reads the full instructions to know *how*.

You can open any `.skill` file as a zip and read the SKILL.md inside if you want to see exactly what it does. No hidden code, no API calls (except Market Research which uses Claude's built-in web search).

## Built By

**Lucky Bajaj** — Senior Business Analyst, 8+ years across insurance, healthcare, and SaaS.

These skills encode the document patterns I've used across real product teams — not generic templates.

- 🌐 [luckybajaj.com](https://luckybajaj.com)
- 💼 [LinkedIn](https://linkedin.com/in/luckybajaj)
- ☕ [Buy Me a Coffee](https://buymeacoffee.com/luckybajaj) — if these saved you time

## License

MIT — use them, modify them, share them. A star on the repo or a coffee is appreciated but never required.
