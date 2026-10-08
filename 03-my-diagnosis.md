# 03 — My diagnosis

> Numbers marked *(hyp.)* are hypothetical and only show the method. Anything with a link comes from a cited source.

## 1. Split the sentence: claims vs observations
| Fragment | Type | Status |
|---|---|---|
| "We need more AI workflows across the company" | **Goal / pre-chosen solution** | Untested. *More* is not the same as *more used* |
| "Most people don't know how to build them" | **Assumed cause** | Untested. It blames skills before ownership, trust, or fit have been ruled out |
| "The few engineers who do are completely bottlenecked" | **Observation** | The only thing actually seen: a queue |
| "Everything is slowing down" | **Undefined symptom** | Not tied to any cost yet |
| Slide: "Why has the team **stopped using** it?" | **Hidden clue** | Workflows already exist and are being abandoned |

**Reframe:** this is a solution plus two symptoms. The queue is real, but it's the *output* of the constraint, not the constraint itself.

## 2. Branch A: "Why does it matter that it's slow?"
1. **Slow how?** Ask-to-first-use lead time is longer than the time the need stays valid (its *half-life*). By Little's Law, lead time = WIP ÷ throughput. With 3 builders and a growing backlog, lead time keeps climbing *(hyp.: 40 open asks ÷ 4 shipped/week ≈ 10 weeks)*.
2. **Why does that matter?** A workflow that ships after its quarter close, campaign, or policy change has been **cancelled, not delayed**. The engineers' time went into it and nothing came back.
3. **Why does that matter?** People stop asking and either do the work by hand or use personal AI tools. The official queue **undercounts** real demand, and that demand moves into side channels (Slack DMs to one engineer, consumer LLMs).
4. **Hits:**
   - **Money:** scarce specialist hours spent on work that expires; manual work continues; cost grows with each request but value doesn't.
   - **Growth:** AI use can't spread faster than the 2–3 people who can build. Each new team adds demand but no throughput.

## 3. Branch B: "Why has the team stopped using it?"
Two different kinds of "stopped", which need to be separated:

**B1: they stopped using the request path**
1. The form is "where work goes to die", so people route around it.
2. Why does that matter? Real demand goes to individuals (key-person load) and to unsanctioned tools.
3. **Hits risk:** customer data in ungoverned tools; one engineer as a single point of failure. *(Context: IBM's 2025 Cost of a Data Breach report found 1 in 5 organisations reported a breach due to shadow AI, and high shadow-AI use added about USD 670K to breach costs. [source](https://newsroom.ibm.com/2025-07-30-ibm-report-13-of-organizations-reported-breaches-of-ai-models-or-applications,-97-of-which-reported-lacking-proper-ai-access-controls))*

**B2: they stopped using what shipped**
1. Shipped flows break (expired key, prompt drift), answer a slightly wrong question, or have **no owner after launch**.
2. Why does that matter? Users go back to the old spreadsheet. Trust drops and the next request starts from scepticism.
3. Why does that matter? Every unused flow is **sunk build cost plus ongoing maintenance** that pulls the same engineers back in.
4. **Hits money and risk:** more building produces more unused, unowned flows running in production. *(Context: MIT NANDA's 2025 "GenAI Divide" report puts most enterprise AI stalls down to brittle workflows that don't fit daily operations, not to model quality. Its sample is small and its figures directional. [source](https://virtualizationreview.com/articles/2025/08/19/mit-report-finds-most-ai-business-investments-fail-reveals-genai-divide.aspx), [caveat](https://aiunite.org/reports/mit-nanda-genai-divide-2025/))*

## 4. The named constraint (one sentence)
> **The constraint is conversion, not capacity: the company has no trusted path from a live business need to an owned, used workflow that doesn't run through a few specialists, so needs expire in the queue, shipped flows go unused, and demand leaks into ungoverned tools.**

In Theory of Constraints terms ([Goldratt's Five Focusing Steps](https://www.tocinstitute.org/five-focusing-steps.html)), the specialists are the visible bottleneck. The real constraint is a **policy constraint**: the rule that every workflow is custom engineering, built and maintained by those few people, with no owner, intake triage, or approved data path. Goldratt warns that most systems are limited mainly by policy constraints ([5FS PDF](https://northriverpress.com/wp-content/uploads/2018/01/Free-download-5FS.pdf)). Adding capacity (hiring, training) before checking this is skipping straight to step 4, *Elevate*.

## 5. Competing hypotheses and what would confirm or kill each
| # | Hypothesis | Confirms it | Kills it |
|---|---|---|---|
| H1 | **Conversion / trust** (my pick) | Lead time > need half-life for most asks; < 50% of shipped flows still run at day 30 *(hyp. threshold)*; much off-ticket demand | Shipped flows are used heavily and the only problem is queue length |
| H2 | **Pure capacity** (the stated belief) | Shipped flows are well used; backlog is current and valuable; lead time is the only complaint | Many open tickets are stale or dead; used-flow rate is low |
| H3 | **No prioritisation** | Asks are first-in-first-out with no value scoring; low-value asks take most builder hours | A value-ranked queue already exists and the top items still wait |
| H4 | **Hype-driven demand** | Asks are framed as "use AI for X" with no metric or owner; leadership mandate is the main source | Each ask has a named owner, a metric, and a deadline |
| H5 | **Skills gap** (the stated cause) | Owners and data paths exist, people want to build, and only know-how is missing | Trained people still don't build, or their flows still aren't used |

## 6. Evidence to gather (cheapest first)
1. **Ticket autopsy:** for the last 20 requests, record open date, ship date, first real use, and whether the need was still alive at ship. *(about 1 hour)*
2. **Day-30 survival:** what share of shipped flows still ran 30 days after launch, and who owns each one?
3. **Shadow demand:** a 5-question pulse survey asking "what did you use instead of filing a ticket?", plus SSO/expense logs for AI tools.
4. **Builder time split:** new builds vs fixing old flows vs triage meetings.
5. **Value tag:** for each open ask, the money, growth, or risk it touches and its deadline.

## 7. What I deliberately did *not* do
No platform pitch, no training plan, no hiring call. Each of those is a solution to a constraint we haven't confirmed yet. The diagnosis tells you **where to measure next**.
