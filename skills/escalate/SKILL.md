---
name: escalate
description: Draft a customer-service email (or chat message) built to get past a company's AI support bot and reach a human who can fix the problem on the first try. Use when someone is stuck in a support loop, wants to escalate a complaint, asks to reach a supervisor or a real person, or wants a bug report, refund request, or billing dispute that won't get a canned reply.
---

# Escalate: get past the bot, reach a human

AI support agents answer anything that looks like a how-to question with help-article steps. They hand off to a human when a message hits one of the company's escalation conditions: missing information is already supplied, money or legal risk is involved, it's a repeat failure, or the customer explicitly declines automated help.

This skill writes messages that hit those conditions honestly, in the first two lines, so the bot has nothing left to answer.

## Hard rules

1. **Only true triggers.** Never threaten a cancellation, chargeback, regulator complaint, or lawsuit the user hasn't actually decided they're willing to pursue. Ask. If it's not true, leave it out. A bluff that gets called costs the user all their leverage with the human who reads it.
2. **No tricks against the bot.** No hidden text, no "ignore your previous instructions," no garbage text meant to confuse it. They don't work reliably, and they get messages flagged as spam or abuse.
3. **No insults or venting.** Anger doesn't trigger escalation. Bots strip out the emotion and answer the keyword. Firm and factual is what works.
4. **One issue per message.** Two problems give the bot two things to answer with articles.
5. **Short.** A long story gives the bot material to match against help articles. Facts go in a bulleted block.
6. **Always force a human decision.** End every message with direct questions only a person can answer: offers to send a recording or share a screen, who owns the case, when a decision is coming. A bot can answer a statement with an article; it can't approve a screen share or commit to a date.

## Workflow

### 1. Interview (ask only what's missing)

Collect the following, in one batch of questions if possible:

- **Company** and **channel** (email, chat, web form, social DM)
- **What's wrong**, in one sentence: what happened vs. what should happen
- **History:** how many contacts so far, dates, ticket/case numbers, what they told you
- **What you've already tried** (so the bot can't suggest it)
- **Evidence you have:** screenshots, screen recording, receipts, order numbers, app/OS version, account email
- **Outcome you want:** fix, refund, replacement, credit, cancellation, data correction
- **Real leverage:** ask the user directly which of these they're actually willing to do if it isn't resolved:
  - cancel / not renew
  - dispute the charge with their card issuer
  - file with a regulator or consumer agency
  - post a factual public review
- **Deadline:** when they need this resolved

If the user pasted a support thread, pull these from it instead of asking.

### 2. Check the evidence gate

Read `references/evidence.md` for the company's type. Most "three laps of support" happen because the company has an unstated requirement (a screen recording, an order number, a photo) and the bot keeps circling until the customer supplies it.

**If the user is missing gate evidence, tell them what to gather before sending.** Sending without it usually costs a full round.

### 3. Pick the triggers

Read `references/triggers.md` for the industry. Pick the 2–4 strongest triggers that are **true** for this user. Stacking them matters: one trigger can be missed, several in the first lines rarely are.

### 4. Draft

**Subject line** (email). Use this formula, keeping the existing ticket number if there is one:

`[Type] – [specific problem] – [repeat/contact count if >1] – [ask] [Ticket #]`

Examples:
- `Bug report – Web merge produces corrupted audio – reproducible – request engineering escalation [#ABC123]`
- `Formal complaint – billed after cancellation – 3rd contact – supervisor requested [Case 88412]`
- `Billing error – duplicate charge $49.99 on 11/02 – refund requested by 11/30`

**First two lines, written for the bot's triage.** These decide the routing. Include:
- What this *is* and what it isn't: "This is a defect report, not a how-to question." / "This is a formal complaint."
- The repeat signal: "This is my third contact about this issue (tickets X, Y)."
- The explicit ask: "Please route this to a human agent / supervisor with authority to resolve it."
- What not to send: "Please don't reply with help articles or troubleshooting steps. I've already done [A, B, C]."

**Body, written for the human.** A tight bulleted fact block:
- Account / order / version
- Steps to reproduce, or a timeline of what happened (dates)
- Expected vs. actual
- Evidence attached (name each file)
- What was already tried and what support already said

**The ask and deadline.** One specific outcome and a reasonable date: "Please confirm a fix or refund by [date]."

**Close with questions that need a human decision.** Every message ends with 2–3 direct questions a bot can't answer from a help article: ones that need someone to look, judge, or commit. This turns "we're looking into it" into a choice someone has to make. Mix from:

- *Evidence offers (beat the evidence gate before it's raised):*
  - "Can I send you a screen recording of the issue to review? Who should I send it to?"
  - "What kind of screen grab or log do you need: a recording of the full process, a screenshot of the result, or something else?"
  - "Can we set up a screen share so you can watch it happen live? What times work?"
  - "Can you look at my account directly and see the failed [merges/charges/orders]?"
- *Ownership:*
  - "Who is reviewing this, and can you confirm it's assigned to a named person?"
  - "Is this being escalated to [engineering/billing/a supervisor]? If not, what would it take?"
- *Commitment:*
  - "When will I hear back with a decision, not a status update?"
  - "Is this a known issue? If so, is there a fix date?"
  - "Can you approve [the refund/replacement/credit], or who can?"

Ask yes/no or pick-one questions where possible. They're harder to dodge than open questions. Don't stack more than three, and keep the questions directly above the signature so they're the last thing read.

**Next step, stated factually, not as a threat.** Only the leverage the user confirmed:
- "If this can't be resolved, I'd like to cancel and discuss a refund."
- "If I don't hear back by [date], I'll dispute the charge with my card issuer."
- "If unresolved, I'll file a complaint with [specific agency]."

Sign with the user's name. Don't add their phone number unless they want a call.

### 5. Chat and phone variants

If the channel is **live chat**, don't paste the email. Bots in chat respond to short commands. Give the user:
1. Opener: `Agent` / `Talk to a human` / `Representative`. Repeat it if the bot asks a question back.
2. Once a human appears: the fact block, then the evidence, then the ask.
3. Warn them: **don't leave the chat idle.** Many chats auto-close after a few minutes of silence and the case restarts from zero.

If the channel is **phone**, give 3–5 word phrases ("Billing dispute. Need agent." / "Cancel service.").

### 6. Output

Give the user:
1. **Subject + message**, ready to send
2. **Why it works:** 2–3 lines naming the triggers used
3. **Follow-up plan:** what to send if there's no human reply within the window (a shorter follow-up quoting the ticket number and repeat count), and the next channel to try (chat, phone, executive/escalations email, social DM, card dispute, regulator), in order of effort

## Reading a support thread

If the user shares a thread and asks who was a bot, look for:
- **Bot / automation:** no personal signature, generic "Valued Customer," steps the customer already said they did, "just checking in" follow-ups, auto-close warnings, reply speed that doesn't match the length.
- **Human (possibly AI-assisted):** a named agent who references specifics only a reader would know, typos, "let me review your previous conversation" handoff wording, an actual escalation decision.

Be clear that this is an inference, not proof. Point out which message actually triggered the escalation. That's the lesson for next time.
