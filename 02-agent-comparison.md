# 02 — Agent comparison: Claude vs Grok vs Gemini

Inputs: the three answers Tom pasted, plus the HTML artefacts attached to the chat:
- `55ed…html`: **Gemini**'s "Root-Constraint Diagnosis" dialogue (VP Ops stakeholder, diagnostician's notebook).
- `0c51…html`: a 10-minute two-person tape (Mira Chen, diagnoser; Ellen Voss, GM of a 400-person company). Its reasoning and wording match the **Grok** answer.
- `3a56…html`: a COO/diagnostician dialogue (Priya Shah and Dan Okafor) with a "why ladder" and the note *"Figures in this scenario are illustrative."* Its framing matches the **Claude** answer.

## Summaries
### Claude: 5 Whys, facilitator style
- Calls out "we need more AI workflows" as a **solution already chosen**. Bottleneck and slowness are symptoms.
- Example chain: ops requests wait → manual invoice reconciliation → billing errors → **cash flow and customer trust**.
- Spots the **"stopped using it"** clue: workflows exist but aren't adopted (unreliable, wrong problem, no owner), so *more builders = more unused workflows*.
- Raises other branches: no prioritisation, and demand driven by hype.
- Ends by offering to run it interactively. **No final named constraint**, so it isn't ready to hand in.

### Grok: constraint as conversion, timed run
- Splits the sentence into 4 claims. Only the bottleneck is observed.
- **Need half-life:** if a request waits longer than the business need lasts, the work is effectively *cancelled*, not delayed. The queue looks full, but throughput of **used** workflows is near zero.
- Splits "stopped using" into two cases: people **abandon the request path** (go to shadow tools or manual work), or they **abandon shipped flows** (poor fit, broken, nobody owns them).
- Money, growth, and risk are each named. Constraint: *turning business intent into a trusted, reusable workflow without a specialist in the loop.*
- Gives **confirming metrics**: ask-to-first-use time vs need half-life, % of flows still running at day 30, demand that never becomes a ticket, reuse across teams.
- The HTML tape invents scenario figures ("5 of 12 still run", six-week queue) but presents them inside an obvious role-play. It doesn't label them illustrative as clearly as Claude's artefact does.

### Gemini: stakeholder role-play to a platform directive
- Strong storytelling and a clear table of symptom vs terminal constraint.
- **Invents specifics and treats them as findings**: 3-month backlog, expired API key, **-14% enterprise lead conversion**, **$200k engineers spending 30% on prompt tweaks**, shadow SaaS with PII → GDPR/SOC2.
- **Breaks the main rule.** It ends with *"Stop hiring more AI engineers. Deploy a governed self-service AI platform…"*, which is a solution and a vendor-category pitch.
- Root-cause framing ("treating ops automation as custom engineering, not enablement") is useful but stated as fact without saying how to test it.

## Scorecard (1–5)
| Criterion | Claude | Grok | Gemini |
|---|:-:|:-:|:-:|
| Rigour (claims vs evidence, branching) | 4 | **5** | 3 |
| Follows the rules (diagnose, don't solve) | **5** | **5** | 1 |
| Reaches money / growth / risk | 4 (money and risk) | **5** (all three) | 4 (all three, but on invented data) |
| Testability (kill/confirm metrics) | 2 | **5** | 1 |
| Honesty about data | **5** (labels illustrative) | 4 | 1 (fabricated stats shown as fact) |
| Hand-in readiness (<5 min) | 2 (asks to continue) | 4 (a bit long) | 3 (readable, but wrong deliverable) |
| **Total /30** | **22** | **28** | **13** |

## Where each one solved instead of diagnosed
- **Claude:** briefly ("maybe the fix is a single billing workflow"), offered as a reframe, not a recommendation. Acceptable.
- **Grok:** doesn't. It explicitly refuses to pitch a fix at 9:35 in the tape.
- **Gemini:** the whole final section is a fix ("Core Actionable Directive"). Not acceptable.

## Fabricated data audit
| Agent | Invented numbers | Labelled? |
|---|---|---|
| Claude | 3 people × 20 h/wk invoice recon; HTML scenario figures | Yes ("say…", "illustrative") |
| Grok | Tape: 6-week queue, 12 shipped / 5 still run / 4 broke | Inside the role-play, not labelled |
| Gemini | −14% conversion, $200k salaries, 30% of sprints, 3-month backlog | **No.** Presented as the diagnosis's evidence |

## What I took from each
- From **Claude**: "solution wearing a problem's coat", the adoption branch, the hype and prioritisation branches, and labelling numbers honestly.
- From **Grok**: the claim split, need half-life, the two kinds of "stopped using", and the kill/confirm metrics.
- From **Gemini**: the shadow-AI risk branch and the symptom-vs-constraint table format. Not taken: its numbers or its directive.

## Verdict
1. **Grok** gave the best diagnosis: it can be tested, it reaches all three of money, growth, and risk, and it proposes no fix.
2. **Claude** has the best instincts and the most honest data, but it never commits to a constraint, so it isn't ready to hand in.
3. **Gemini** is the most persuasive and the least valid. It solves instead of diagnosing and backs that up with numbers it invented.
