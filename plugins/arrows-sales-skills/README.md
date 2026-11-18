# Sales Skills by Arrows

Free sales skills for Claude, from the team at [Arrows](https://arrows.to). They turn Claude into a sales assistant that knows your deals and works the way you sell.

## The skills

| Skill | What it does |
|---|---|
| Setup (run first) | Builds your sales profile from your CRM, calls, and email: your voice, your sales process, your buyers and competitors, and how you work. |
| Daily brief | Your day on one page: what to do first, what changed, today's calls, replies waiting, and deals at risk. |
| Pre-call prep | A 60-second brief for one upcoming call. |
| Post-call | Drafts the follow-up email in your voice and the CRM update from your last call. Nothing changes in the CRM until you approve it. |
| Deal nudge | Picks one move for a stalled deal and drafts a short nudge, or scans your pipeline for deals that need one. |
| Weekly pipeline review | Every open deal on one page: what's moving, what's at risk and why, and what's closing. |
| Process gaps report | What's falling through the cracks, measured against your own sales process. |
| CRM guide and hygiene check | Learns how your CRM is used, then finds missing or wrong data and suggests fixes for you to approve. |
| Win-loss analysis | Why you win and why you lose, from your closed deals. |
| Objective forecast | How likely each deal closing this period really is, judged only from what the buyer said and did. |
| Agentic playbook builder | Writes down how your team runs its sales process, play by play, from your real deals and calls. |
| Sales methodology | Puts your methodology (such as MEDDPICC, BANT, or SPICED) into Claude and shows how deals follow it. |

## Use it

Start with setup: say "Build my sales profile" and Claude builds your sales profile from the tools you've connected. Then ask for what you need. For example:

- "Build my sales profile"
- "Run my Arrows daily brief"
- "Run the Arrows meeting prep for [company]"
- "Run the Arrows post-call on [company]"
- "Run my Arrows weekly pipeline review"
- "What's falling through the cracks?"

Each skill also runs as /arrows-sales-skills:<skill-name>.

No CRM connected? Every skill also works from a CSV export of your deals. To try one without connecting anything, upload the made-up pipeline in this plugin's examples/sample-pipeline.csv file and say, for example, "Run my Arrows weekly pipeline review on this export."

## Data

The skills are instructions and report templates only. The plugin bundles no connectors, runs no code, and loads nothing from the web, and it sends nothing to Arrows.

Reports are pages Claude builds in your chat from the template in each skill's folder. They load no fonts, images, or scripts from other sites.

When you run a skill, Claude reads deal data, including names and email addresses, from the connectors you've already added yourself, such as your CRM, email, calendar, call recorder, and Slack. Some skills also use Claude's web search to look up public information, like a meeting attendee's LinkedIn profile or a company's website. If you ask, Claude can send a skill's output to you through your own connected tools, like a Slack message, or save it where you say, like a Google Doc or a Notion page.

Nothing in your CRM, email, or calendar changes unless you approve the exact change first.

When you run setup, it saves your sales profile as a few short Markdown files (named arrows-*.md) in your own Claude project. Some other skills, like the CRM guide or the sales methodology, save what you set up the same way, so every skill works from it. These files describe how you and your team sell, never buyer names or deal details. They're plain files you can read, edit, or delete at any time, and nothing is stored outside your Claude account.

More at [skills.arrows.to](https://skills.arrows.to) and [github.com/ArrowsHQ/arrows-sales-skills](https://github.com/ArrowsHQ/arrows-sales-skills).
