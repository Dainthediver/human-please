# Escalation triggers by industry

AI triage systems generally escalate on four things:

1. **Severity keywords**, read in context: *refund, cancel, complaint, dispute, chargeback, legal, regulator, escalate*
2. **Repeat failure**: the same issue, multiple contacts, ticket numbers cited
3. **Money or legal risk** the bot isn't allowed to decide: refunds above a limit, retention offers, disputes, compliance
4. **Explicit refusal of self-service**: "don't send articles, I need a human"

Use only what's true for the user. Rules and agencies change, so check current rules for the user's country/state before citing one.

---

## Software / SaaS / apps / devices with cloud features
- **Strongest:** "This is a reproducible defect report, not a how-to question" + full repro steps + recording (see evidence.md)
- Repeat contact with ticket numbers
- "Request escalation to engineering / technical team"
- Refund request if the feature was a reason for purchase
- Data loss or privacy/security exposure: say so explicitly. These are usually mandatory escalations.

## Subscriptions & memberships (streaming, gyms, software plans)
- **Strongest:** "I want to cancel" / "Please cancel effective today." Retention teams are usually human.
- Billed after cancellation: "billing error," with dates and amounts
- Card dispute, if the user is willing
- In the US, the FTC and many states have rules about making cancellation easy. Mention a specific rule only if the user has checked that it applies.

## Telecom / internet / phone carriers
- "Cancel service" / "Port out my number": retention routing
- Repeat outage or billing error with ticket numbers
- Formal complaint request
- US: FCC informal complaint (fcc.gov/complaints). Carriers typically must respond to these.

## Banks, credit cards, payments, fintech
- **"Billing error dispute"** / **"unauthorized transaction"** are terms banks have to process under specific rules
- "Please log this as a formal complaint"
- US: CFPB complaint (consumerfinance.gov/complaint). Companies respond through a portal.
- Card disputes for billing errors have time limits (US: generally 60 days from the statement). Note dates.

## E-commerce / retail / marketplaces
- Order number + "item not received" / "not as described" + photos
- Return or refund refused: "requesting a supervisor review"
- Card dispute / payment-platform claim if the user is willing
- Marketplace A-to-Z or buyer-protection claim where offered

## Airlines & travel
- Cancelled or significantly changed flight: "requesting a refund to original form of payment"
- Cite passenger-rights rules that apply: US DOT refund rules, EU261/UK261 compensation for eligible delays and cancellations. Check eligibility first.
- US: DOT complaint (transportation.gov/airconsumer)
- Lost baggage: file the report number in the subject line

## Utilities (power, gas, water)
- Billing error with meter readings / dates
- Formal complaint request
- State public utility commission complaint (US)

## Insurance
- Claim number in subject
- "Requesting a written explanation of the denial" / "requesting supervisor review of the claim decision"
- State insurance department complaint (US)

## Healthcare billing
- "Requesting an itemized bill"
- "Disputing this charge. Please hold from collections while under review."
- Insurance EOB reference numbers

## Any company: universal triggers
- Subject line with ticket # + "3rd contact" + "supervisor requested"
- "Please log this as a formal complaint"
- "Please don't reply with help articles. I've already done [X, Y, Z]."
- A specific deadline
- Factual public review, *only if the user actually plans to*. Weakest lever; bots often ignore it.
