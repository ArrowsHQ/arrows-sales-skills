# Sales Skills by Arrows

**Free Claude sales skills, plus the same skills for ChatGPT, Copilot, and Gemini.**

Turn the AI you already have into a sales assistant that knows your deals. These skills run your daily sales work using what's in your CRM, email, calendar, and call recordings: morning briefs, meeting prep, follow-up emails, deal nudges, and pipeline reviews.

Built by the team at [Arrows](https://arrows.to). If you use Claude, the easiest install is the [Sales Skills by Arrows connector](https://skills.arrows.to): one URL, two minutes. This repo has the same workflows as plain files, so they also work with ChatGPT, Copilot, Gemini, or any other AI tool. It's also a Claude plugin marketplace, so you can add every skill to Claude as one plugin.

If these skills help you, star this repo so other sellers can find it.

## Quick facts

| | |
|---|---|
| **What it is** | 7 free AI skills for sales reps and sales leaders |
| **Works in** | Claude (connector, plugin, or skill upload), ChatGPT, Microsoft Copilot, Google Gemini |
| **Works with** | Any CRM, email, calendar, and call recorder your AI tool can connect to. No connection? Paste in a CSV export or your notes. |
| **Price** | Free. No signup, no email gate. |
| **License** | Apache 2.0 |
| **Made by** | [Arrows](https://arrows.to) |

---

## What's a skill?

A skill is a file with instructions your AI tool follows when you ask for something specific. Say "Run my Arrows daily brief" and Claude loads the Arrows daily brief skill and produces the output.

Skills save you from typing the same long prompt every time you want to do a task you do often. Install them once, then just ask for what you need.

---

## Start here: run the setup skill first

Before anything else, run the **Arrows setup** skill. It reads your CRM, calls and email, shows you what it learned, asks a couple of quick questions, and saves your sales profile as a few short files: how you write, your sales process, your buyers and competitors, and how you work. Every other skill uses them. Sales leaders also get team files their reps can add, so the whole team follows one process while each rep keeps their own voice.

Setup takes about 5 to 10 minutes. Do it once, and the rest of the skills sound like you.

---

## The skills

| Skill | What it does |
|-------|--------------|
| **Arrows setup** (run first) | Builds your sales profile from your CRM, calls and email: your voice, your sales process, your buyers and competitors, and how you work. Leaders also get team files for their reps. Every other skill uses it. |
| **Arrows daily brief** | A scannable overview of your day: today's calls with attendee and deal context, messages waiting for a reply, pipeline alerts, and open time. Pulls from your calendar, CRM, email, chat, and call recordings. |
| **Arrows pre-call prep** | Before a specific meeting, gives you what you need in 60 seconds: who you're meeting, what they want to solve, what happened last time, what to push on, what might go sideways, and open discovery questions. |
| **Arrows post-call** | Right after a call, produces a follow-up email draft, a copyable CRM note, and relevant resources to send. Every fact comes from the actual call. |
| **Arrows deal nudge** | Finds a stalled deal and drafts a specific play to reactivate it (send a resource, tap into something mentioned before, loop in a stakeholder, own a broken commitment). Scans your whole pipeline and surfaces candidates, or nudges a specific deal you name. |
| **Arrows weekly pipeline review** | Your whole open pipeline on one shareable page, the same layout every week: what's moving forward, what's at risk and why, what to do this week, and what's expected to close. Sales leaders get a rollup by rep with what to raise in each 1:1. Can run itself every Monday. |
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
5. Name it **Sales Skills by Arrows**.
6. Paste this URL: `https://skills.arrows.to`
7. Click **Add** and restart Claude Desktop.

Done. Start a new chat and type "Build my sales profile" to begin.

### Or: add them as a Claude plugin

This repo is also a Claude plugin marketplace. Adding the plugin installs all seven skills at once, and they update when this repo does.

- **Claude (web or desktop):** go to **Customize**, then **Plugins**, then **Add**, then **Add marketplace**, and enter `ArrowsHQ/arrows-sales-skills`. Then add the **Sales Skills by Arrows** plugin.
- **Claude Code:** run `claude plugin marketplace add ArrowsHQ/arrows-sales-skills`, then `claude plugin install arrows-sales-skills@arrows`.

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

- **Setup:** "Build my sales profile"
- **Daily brief:** "Run my Arrows daily brief"
- **Meeting prep:** "Run the Arrows meeting prep for [company]"
- **Post-call:** "Run my Arrows post-call" or "Run the Arrows post-call on [company]"
- **Deal nudge:** "Run the Arrows deal nudge on [company]" or "Run the Arrows deal nudge on my pipeline"
- **Weekly pipeline review:** "Run my Arrows weekly pipeline review"
- **Help:** "Arrows help"

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

## Common questions

### What are Claude skills for sales?

Claude skills are instruction files that teach Claude to do a specific job the same way every time. Sales skills turn everyday sales work into one-line requests: "Run my Arrows daily brief" gets you today's calls, replies you owe, and pipeline alerts, using what's in your CRM, email, calendar, and call recordings. Sales Skills by Arrows is a free set of 7 of them.

### How do I use Claude for sales?

Connect Claude to your sales tools (CRM, email, calendar, call recorder), then install these skills so it knows how to run real sales workflows instead of just answering questions. The full walkthrough: [How to set up Claude for sales in 15 minutes](https://arrows.to/guide/how-to-set-up-claude-for-sales-in-15-minutes). For what to connect, see [every sales tool that connects to Claude](https://arrows.to/resources/every-sales-tool-that-connects-to-claude-2026).

### How do I use ChatGPT (or Copilot, or Gemini) for sales?

Same workflows, different install. Each skill in this repo is a plain text file. Paste it into a Custom GPT (ChatGPT), a custom Agent (Copilot), or a Gem (Gemini) and trigger it the same way. See "Two ways to install" above. For the full ChatGPT walkthrough: [How to set up ChatGPT for sales in 15 minutes](https://arrows.to/guide/how-to-set-up-chatgpt-for-sales-in-15-minutes).

### What's the difference between the connector and this repo?

The [connector](https://skills.arrows.to) is for Claude: install once, every skill shows up automatically, and updates ship to you. This repo is the same skills as portable files for every other AI tool, or for Claude users whose company blocks custom connectors.

### Does it work with my CRM?

It works with any CRM your AI tool can connect to. In Claude, check the [connector directory](https://claude.ai/directory). If yours isn't there, export a CSV or paste in deal notes and the skills still run.

### Is my deal data safe?

The skills are instructions, not a pipe to us. Your CRM, email, and calls stay connected through your AI tool's own connectors, and the files in this repo don't send anything anywhere. If you use the Claude connector, Arrows only sees that a skill was run, not the contents of your deals. Check that your company's AI account is set so your data isn't used for training.

### Can my whole sales team use this?

Yes. Each rep installs the skills and runs them in their own AI account. They still prompt it themselves, and setups drift between reps over time. When you want one playbook running on every deal for the whole team without anyone prompting, see [how Arrows compares to Claude for sales teams](https://arrows.to/arrows-vs-claude/).

### Is it really free?

Yes. No signup, no email gate. We build [Arrows](https://arrows.to), a sales execution platform that takes this much further. If these skills are useful, you're who we built Arrows for.

---

## License

Apache 2.0. See [LICENSE](LICENSE). You're free to use, change, and share these skills. The license doesn't give rights to the Arrows name or logo.

---

## About

Built by the team at [Arrows](https://arrows.to), an AI-powered selling platform that does all this for you automatically across every deal so you can focus on closing.
