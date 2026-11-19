# human-please 🙋

**Write customer-service emails that get past the AI support bot and reach a human on the first try.**

Companies now put AI agents in front of every support inbox. Ask a real question and you get help-article steps you already tried. Push back and you get a "just checking in" follow-up. It took me three rounds with an AI note-taker company before a person looked at a bug that was obvious from the start.

What actually got me to a human wasn't anger. My angry email got another canned reply. It was **hitting the conditions the company's own system escalates on.** This tool writes messages that hit those conditions in the first two lines, honestly.

## What it does

1. **Interviews you** (or reads a support thread you paste): what broke, what you tried, ticket numbers, what you want
2. **Flags missing evidence** the company will demand before escalating, like a screen recording or an order number, so you don't lose a round
3. **Picks the escalation triggers** that are true for you: repeat failure, defect-not-how-to, refund/cancel, card dispute, regulator, by industry
4. **Writes the email:** a subject line and opening built for the bot's triage, a fact block written for the human who reads it next
5. **Gives you a follow-up plan** if nobody answers

See a real before/after: [`examples/software-bug.md`](examples/software-bug.md)

## Install

**Any chatbot (ChatGPT, Gemini, Claude):** copy the prompt in [`PROMPT.md`](PROMPT.md) into a new chat.

**Claude Code and other agents that support Agent Skills:**
```bash
npx skills add Dainthediver/human-please --skill escalate
```
Or copy `skills/escalate/` into `~/.claude/skills/`.

**Claude app:** zip the `skills/escalate` folder and upload it as a custom skill.

Then just say something like: *"I need to escalate a problem with my internet provider"* or paste the support thread.

## The rules it follows

- **Only true leverage.** It asks before mentioning cancellation, a chargeback, or a regulator. Bluffing burns your credibility with the human who finally reads it.
- **No tricks.** No prompt injection, hidden text, or bot-confusing garbage. It doesn't work reliably and gets you flagged.
- **No venting.** Bots strip out emotion and answer the keyword. Firm and factual is what gets routed up.

## What's inside

```
PROMPT.md                         copy-paste version
skills/escalate/SKILL.md          the agent skill
skills/escalate/references/
  triggers.md                     what forces a handoff, by industry
  evidence.md                     what each company type requires before escalating
examples/                         real before/after cases
```

## Help make it better

The most valuable part is [`triggers.md`](skills/escalate/references/triggers.md): what actually works at specific kinds of companies. If this got you to a human (or didn't), [open an issue](../../issues/new) or see [CONTRIBUTING.md](CONTRIBUTING.md).

## Disclaimer

Not legal advice. Consumer-protection rules vary by country and state, so check that a rule applies before citing it.

## License

MIT
