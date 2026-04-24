# Arrows Sales Skills

**Built for Claude. Works with any AI.**

Sales workflows that handle the work around every deal, so you can focus on the human part of selling. Built by the team at [Arrows](https://arrows.to). Same workflows as the [Arrows Sales Skills MCP](https://skills.arrows.to), packaged as plain files so they work with Claude, ChatGPT, Copilot, Gemini, or any other AI tool.

---

## What's a skill?

A skill is a file with instructions your AI tool follows when you ask for something specific. Say "run my daily brief" and Claude loads the Arrows daily brief skill and produces the output.

Skills save you from typing the same long prompt every time you want to do a task you do often. Install them once, then just ask for what you need.

---

## Start here: run the setup skill first

Before anything else, run the **Arrows setup** skill. It builds your sales profile: how you sell, how you write, who your typical buyers are, what your sales process looks like, and what tools you have connected. Every other skill uses what setup learns to tailor its output to you.

Setup takes about 5 minutes. Do it once, and the rest of the skills get smarter automatically.

---

## The skills

| Skill | What it does |
|-------|--------------|
| **Arrows setup** (run first) | Builds your sales profile by scanning your CRM, call recordings, and email. Captures how you sell, your voice, your typical buyers, and your sales process. Every other skill uses this context. |
| **Arrows daily brief** | A scannable overview of your day: today's calls with attendee and deal context, messages waiting for a reply, pipeline alerts, and open time. Pulls from your calendar, CRM, email, chat, and call recordings. |
| **Arrows pre-call prep** | Before a specific meeting, gives you what you need in 60 seconds: who you're meeting, what they want to solve, what happened last time, what to push on, what might go sideways, and open discovery questions. |
| **Arrows post-call** | Right after a call, produces a follow-up email draft, a copyable CRM note, and relevant resources to send. Every fact comes from the actual call. |
| **Arrows deal nudge** | Finds a stalled deal and drafts a specific play to reactivate it (send a resource, tap into something mentioned before, loop in a stakeholder, own a broken commitment). Scans your whole pipeline and surfaces candidates, or nudges a specific deal you name. |
| **Arrows weekly pipeline review** | Full pipeline scan for your manager 1:1 or weekly planning: what's closing this week, what's at risk, and a deal-by-deal rollup grouped by stage. Can also generate a live visual you can share. |
| **Arrows help** | Prints a reference of every available Arrows skill and its trigger phrase. Useful when you forget what's installed or what to say. |

---

## How the skills work together

Run setup once.

Every morning, or whenever you need a pulse on your day, run your daily brief.

Before a specific call, run pre-call prep on that meeting. Right after the call, run post-call. When a deal goes quiet, run deal nudge.

Each skill knows about the others. When you finish post-call, it offers to prep you for the next call with the same buyer. When you finish the daily brief, it can suggest running deal nudge on a deal that went dark. You don't have to remember which skill to run next. The tool tells you.

---

## Two ways to install

### Option 1: Easiest (if you use Claude)

This is the recommended path. One URL, about 30 seconds. All the skills appear in Claude automatically, and updates ship automatically too, so you always have the latest version.

1. Open Claude Desktop and click your name in the bottom left corner.
2. Click **Settings**.
3. Click **Connectors**.
4. Scroll to the bottom and click **Add custom connector**.
5. Name it **Arrows Sales Skills**.
6. Paste this URL: `https://skills.arrows.to`
7. Click **Add** and restart Claude Desktop.

Done. Start a new chat and type "run the Arrows setup" to begin.

### Option 2: If your admin blocked that, or you use a different AI

If your company doesn't allow custom connectors, or you use ChatGPT, Copilot, Gemini, or another AI tool, you can download the skills directly and upload them.

1. Pick a skill. The folders above this README (arrows-setup, arrows-daily-brief, arrows-pre-call-prep, arrows-post-call, arrows-deal-nudge, arrows-weekly-pipeline-review, arrows-help) each contain a SKILL.md file.
2. Click into the folder, then click on the SKILL.md file.
3. Click the **Raw** button at the top right to see the plain text, or click **Download raw file** to save it.
4. Upload it to your AI tool:
   - **Claude Desktop:** Settings, then Skills, then Upload.
   - **ChatGPT:** Create a Custom GPT and paste the contents into the Instructions field.
   - **Microsoft Copilot:** Create a custom Agent and paste into the system prompt.
   - **Google Gemini:** Create a Gem and paste into the Gem instructions.

Start with Arrows setup first, same as Option 1. Then install the others in whatever order you like.

---

## How to use each skill

Once installed, trigger a skill by typing one of these phrases into your AI tool:

- **Setup:** "Build my Arrows sales profile"
- **Daily brief:** "Run my Arrows daily brief"
- **Pre-call prep:** "Prep me for my call with [company]" or "Pre-call prep on [company]"
- **Post-call:** "Run my Arrows post-call" or "Run post-call on [company]"
- **Deal nudge:** "Nudge [company]" or "Which deals need a nudge?"
- **Weekly pipeline review:** "Run my weekly pipeline review" or "Show me my pipeline"
- **Help:** "Arrows help" or "What can you do?"

You can also invoke skills directly:

```
/arrows-setup
/arrows-daily-brief
/arrows-pre-call-prep
/arrows-post-call
/arrows-deal-nudge
/arrows-weekly-pipeline-review
/arrows-help
```

---

## About

Built by the team at [Arrows](https://arrows.to), an AI-powered selling platform that does all this for you automatically across every deal so you can focus on closing.
