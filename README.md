# Arrows Sales Skills

**Built for Claude. Works with any AI.**

Sales workflows that handle the work around every deal — daily briefs, pre-call prep, post-call execution, deal nudges — so you can focus on the human part of selling.

These are the same workflows as the Arrows Sales Skills MCP ([skills.arrows.to](https://skills.arrows.to)), packaged as plain markdown so they work anywhere.

## What's in here

One folder per skill. Each folder has a `SKILL.md` file with the instructions and a description that any LLM can use to load the right skill at the right time.

Current skills:
- **arrows-setup** — Arrows Sales Skills setup.
- **arrows-daily-brief** — Arrows daily brief.
- **arrows-pre-call-prep** — Arrows pre-call prep.
- **arrows-post-call** — Arrows post-call workflow.

## How to use these

### If you use Claude

The easiest path is the MCP at [skills.arrows.to](https://skills.arrows.to). Updates ship automatically, no download required.

If you can't install MCPs (admin-blocked, company policy, etc.), use this repo instead:

1. In Claude Desktop, open Settings and find Skills (location varies by version — if you don't see it, check under Capabilities or contact your admin).
2. Upload the `SKILL.md` file for each skill you want.
3. Start a new chat. Claude will load the skill when you say something that matches its description (e.g. "run my daily brief").

### If you use ChatGPT, Copilot, Gemini, or anything else

The content inside each SKILL.md is plain markdown. It works anywhere.

1. Open the SKILL.md file you want (e.g. `arrows-daily-brief/SKILL.md`).
2. Copy everything **after** the frontmatter block (skip the `---` lines and the `name:` / `description:` fields).
3. Paste it into your tool's equivalent of "instructions":
   - **ChatGPT:** Create a Custom GPT and paste into Instructions. Or paste into a Project's Instructions.
   - **Copilot:** Create a custom Agent and paste into the system prompt.
   - **Gemini:** Create a Gem and paste into the Gem instructions.
4. Start a new chat inside that GPT / Agent / Gem. It runs the same workflow.

The outputs will vary by model, but the instructions are identical. If an output feels off, paste more context (your deals, your meeting transcript, etc.) into the chat directly.

## Questions or feedback

Find us in the AI for Closers Slack community, or reach out at [arrows.to](https://arrows.to).
