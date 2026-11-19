# Example: AI note-taker app, broken merge feature

## What happened (3 rounds to reach a human)

| # | Customer sent | Support replied | Who (best guess) |
|---|---|---|---|
| 1 | Chat: "Merge is not working" | Asked app version, then pasted mobile-app merge instructions | Bot |
| 2 | Chat: "I know how to merge. It doesn't work. Let me talk to a human" | "Allow us a few minutes while we review your conversation…" then asked for a screenshot + **screen recording** | Human (handoff wording, a typo), ~2 min after asking |
| — | Customer stepped away | "Are you still there?" ×2 → chat auto-closed | Timed macros |
| — | — | Next day: "Just checking in, ticket will close in 48h" | CRM automation |
| 3 | Long angry email: insults, "AI slop," threat to tell everyone to use a competitor | Unsigned reply with the **same merge steps** the customer already did | AI agent (or unread AI draft) |
| 4 | "That's exactly how I did it. Do you need a video?" | Named agent apologizes, asks for a screen recording | Human, AI-assisted |
| 5 | Sends the recording | **Escalated to senior support 7 minutes later** | Human |

**Lessons**
- Anger got another canned reply. "Talk to a human" in chat worked in 2 minutes.
- The real gate was a **screen recording**, which support asked for on day 1. Everything after that was circling until it arrived.
- Leaving the chat idle reset the case.

## The first email that should have been sent

> **Subject:** Bug report – Web app merge produces corrupted audio – reproducible – request engineering escalation [#TICKET]
>
> This is a software defect report, not a how-to question. Please don't send merge instructions. I've merged correctly from both the Home page and the Library, three times.
>
> - **Platform:** Web app (app version 4.0.1)
> - **Steps:** Sync recordings → select 2+ on Home → Merge
> - **Expected:** Playable merged file
> - **Actual:** Merged file is unlistenable. The source recordings play fine.
> - **Evidence:** Screen recording attached (merge-bug.mp4) showing the full process and the result
> - **Account:** [email]
>
> Please route this to a human on the technical team. If it can't be fixed, I'd like to discuss a refund.
>
> - Can someone review the attached recording, or would a live screen share be more useful? I'm available [times].
> - Can you look at my account directly and see the failed merges?
> - Who is this assigned to, and when can I expect a decision on a fix?
>
> [Name]

**Why it works:** labels itself as a defect (not how-to), refuses the canned steps up front, supplies every piece of gate evidence, asks for a human by role, adds a true money trigger (refund), and ends with questions only a person can answer: review this, look at the account, name an owner and a date.
