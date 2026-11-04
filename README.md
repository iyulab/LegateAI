# LegateAI

Graduated autonomy and approval for AI agents.

A legate acts under a bounded commission: free inside it, accountable for it, and obliged to come back when a decision falls outside it. LegateAI is the layer that decides **how an agent decides** and **who it asks** — so an owner can delegate work without losing the say on what matters.

## Role

1. **Small decisions are made alone.** The agent decides, tells the owner, and keeps the decision reversible. What makes a decision *small* is a fixed floor plus a range that is earned per kind of decision — see [the method](docs/method.md#three-weights); how far the range reaches is still open ([Open questions](#open-questions)).
2. **Important decisions take the owner's choice.**
   1. The agent presents **options**.
   2. Each option carries its **grounds and trade-offs**.
   3. The agent **recommends** one.
   4. If it cannot recommend, the cause is a missing or conflicting *criterion*, so it asks about the criterion — not about the surface case.
   5. If the owner chooses something other than the recommendation, it asks for the criterion behind the choice — not for the surface reason.
3. **Criteria are managed, and kept aligned with the owner's judgment.** Recorded criteria and decision flows are checked against each other and conflicts are detected. The agent keeps working to adjust the criteria toward the owner's judgment, so they converge instead of drifting apart.

## Direction

LegateAI is meant to grow from a set of working rules into a **method** that other products can adopt: how an owner and an agent bring their judgment into line, and keep it there. The rules it starts from are the ones already used when delegating work to coding agents — deciding at different weights, recording a decision together with the way back, asking for a criterion instead of a verdict. The aim is to make them systematic and independent of any one product.

The method is a flywheel, not a checklist. Where trust is measured — for example by re-judging a sample of the agent's own decisions without showing it the agent's answer, and recording the odds of being drawn — autonomy can widen exactly where agreement has been shown, and the owner's corrections become criteria that make the next decision easier. LegateAI owns the form of that loop; the measurement comes in through the port described under Scope.

What a criterion *says* belongs to whoever adopts the method. LegateAI carries no organization's rules.

It is meant to be a **core capability built into agents that decide on their own**, across several products, rather than something each product writes for itself.

The method itself, with diagrams and its starting decisions: [docs/method.md](docs/method.md).

## Open questions

- **How far does a kind of decision earn?** The floor is settled in [the method](docs/method.md#three-weights): a decision with no named way back, or one visible outside the commission, is always asked, and above the floor recorded criteria must cover it without conflict. What a decision *earns* beyond that is counted per kind, from measured agreement with the owner. Open: the first threshold, how agreement is measured, what a "kind" is, and the shape of the port that supplies the measurement.
- **How is it built in?** Agents that would embed it are written in different languages and run in different processes. The record shapes (a decision, a criterion, a recheck) may be best kept as a language-neutral specification with a reference implementation, rather than as one library. Open.
- **Which way does the trust port point?** A system that measures trust may itself be a consumer of this method. The port should be defined here and implemented on the other side, so this repository depends on no measurement system and a measurement system can depend on this one without a cycle.
- **Three weights.** Deciding alone and asking are the ends; between them the method names a middle: act on the recommendation, record the way back, and let the owner correct it afterwards — the owner's corrections here are what feed the loop. Open: its name and exactly where it borders the other two.

## Scope

- LegateAI owns the *form* of a decision (what counts as important, how a choice is presented, how criteria are recorded and reconciled).
- It does not measure how far a judge, model or agent can be trusted. That evidence is read through a port, so any trust-measurement system can supply it.

## Status

Early design. There is no code yet.

## License

[MIT](LICENSE)
