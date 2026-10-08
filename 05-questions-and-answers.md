# 05 — Questions and answers

## A. The two required facilitator questions
**Q1. Why does it matter that it's slow?**
**A.** Because lead time is longer than the life of the need. A workflow that ships after the quarter close, campaign, or policy change it was meant for has been cancelled, not delayed. That costs money (specialist hours on expired work, manual work carrying on) and limits growth (AI use can't spread faster than the specialist pool).

**Q2. Why has the team stopped using it?**
**A.** First, separate two meanings of "it". Some people stopped using the **request path** because tickets disappear, so they go to Slack DMs or personal AI tools. That's risk: data leakage and key-person dependency. Others stopped using **what shipped** because it broke, didn't fit the job, or had nobody maintaining it. That's money (sunk cost plus maintenance) and risk (unowned flows in production).

## B. Follow-up questions a good diagnoser asks
| Question | Why ask it | Model answer (hypothetical scenario) |
|---|---|---|
| Which part of that sentence have you actually *seen*? | Separates evidence from belief | "The queue. The rest is what I believe." |
| Slow compared to what clock? | Turns "slow" into something measurable | "Six weeks *(hyp.)* to ship; the need lasted three." |
| Give me one request that died in the queue. | Gets something concrete | "Renewals' churn brief arrived after quarter close." |
| Of what you shipped, what still runs at day 30? | Decides capacity vs conversion | "Fewer than half *(hyp.)*." |
| Who owns a workflow after launch? | Tests the ownership hypothesis | "Nobody. The engineer, in theory." |
| What do people do instead of filing a ticket? | Surfaces shadow demand and risk | "Message Priya, or paste data into ChatGPT." |
| How is the queue prioritised? | Tests H3 | "First come, first served." |
| Where did the 'we need more AI' push come from? | Tests H4 (hype) | "A board slide." |
| What would make you believe this is purely capacity? | Makes the diagnosis falsifiable | "Shipped flows used heavily, backlog still current." |

## C. Likely interviewer pushbacks, with strong replies
**"Isn't it obvious? Hire more engineers."**
→ That's step 4 in Theory of Constraints, *elevate*. You exploit and subordinate first. If half of what ships goes unused, doubling the builders doubles the unused flows. Show me the day-30 usage figure first.

**"So your answer is a self-service platform?"**
→ No. That's a solution, and the brief says diagnose. A platform might help, or it might spread unowned flows faster. The diagnosis tells us what to measure before choosing a fix.

**"You made up the six-week number."**
→ Yes, and it's labelled hypothetical. What matters is the comparison: lead time against how long the need stays valid. I'd get the real figures from the last 20 tickets.

**"5 Whys is too simplistic."**
→ Agreed. It tends to follow a single line of cause. That's why I branch twice and test five competing hypotheses, not one chain.

**"Where's the money? 'Slow' isn't a cost."**
→ Three places: specialist hours spent on requests that expire, manual work continuing, and maintenance of unused flows. Each can be measured in hours times cost per hour *(hyp.)*.

**"Isn't the risk branch speculative?"**
→ It's a hypothesis, but a well-supported one. IBM's 2025 breach report found 1 in 5 organisations had a breach involving shadow AI. Here I'd check SSO and expense logs for AI tools before claiming it.

**"What if people really just can't build?"**
→ Then trained people would build flows that get used. If they're trained and the flows still sit unused, the cause is ownership or trust, not skill. That's H5, and it's testable.

**"Name the constraint in one sentence."**
→ The company has no trusted path from a live business need to an owned, used workflow that doesn't run through a few specialists.

## D. Self-check before handing in
- [ ] No solution language ("deploy", "implement", "hire", "train")
- [ ] Both branches end at money, growth, or risk
- [ ] Invented numbers are labelled hypothetical
- [ ] One-sentence constraint
- [ ] At least one kill condition
