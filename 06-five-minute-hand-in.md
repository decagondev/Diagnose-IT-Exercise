# 06 — Five-minute hand-in

**Diagnosis: AI workflow bottleneck**

"We need more AI workflows" is a solution someone has already picked. The only thing actually observed is a queue in front of a few engineers. "People can't build" is an assumed cause, and "everything is slowing" isn't tied to any cost yet.

**Why does slow matter?** Requests wait longer than the need lasts. A churn brief that arrives after quarter close has been cancelled, not delayed. Specialist hours go into work that expires, so cost grows with each request while value doesn't (**money**). AI use can't spread faster than three people (**growth**).

**Why has the team stopped using it?** There are two kinds of stopping. Some people abandon the *request path*: demand moves to Slack DMs and personal AI tools, so customer data leaks and one engineer becomes a single point of failure (**risk**). Others abandon *what shipped*: flows break, answer the wrong question, or have no owner, which means sunk build cost and unused flows still running in production (**money and risk**).

**Constraint:** conversion, not capacity. The company has no trusted path from a live business need to an owned, used workflow that doesn't run through a few specialists. More builders or more training would just feed more work into the same broken path.

**What would confirm or kill this:**
1. Ask-to-first-use time vs how long each need stays valid.
2. Share of shipped flows still running at day 30, and whether each has an owner.
3. Demand that never became a ticket (shadow tools, DMs).

If shipped flows are well used and the backlog is still current, I'm wrong and it really is capacity.
