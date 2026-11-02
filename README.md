# LegateAI

Graduated autonomy and approval for AI agents.

A legate acts under a bounded commission: free inside it, accountable for it, and obliged to come back when a decision falls outside it. LegateAI is the layer that decides **how an agent decides** and **who it asks** — so an owner can delegate work without losing the say on what matters.

## Role

1. **Small decisions are made alone.** The agent decides, tells the owner, and keeps the decision reversible. What makes a decision *small* is not yet defined — see [Open questions](#open-questions).
2. **Important decisions take the owner's choice.**
   1. The agent presents **options**.
   2. Each option carries its **grounds and trade-offs**.
   3. The agent **recommends** one.
   4. If it cannot recommend, the cause is a missing or conflicting *criterion*, so it asks about the criterion — not about the surface case.
   5. If the owner chooses something other than the recommendation, it asks for the criterion behind the choice — not for the surface reason.
3. **Criteria are managed, and kept aligned with the owner's judgment.** Recorded criteria and decision flows are checked against each other and conflicts are detected. The agent keeps working to adjust the criteria toward the owner's judgment, so they converge instead of drifting apart.

## Open questions

- **What is a small decision?** The line between deciding alone and asking decides everything else, so it needs a definition that can be checked, not a feeling. Candidates to settle: whether a way back is defined, whether the effect stays inside the commission, whether it is visible outside it, and whether recorded criteria already cover it without conflict.

## Scope

- LegateAI owns the *form* of a decision (what counts as important, how a choice is presented, how criteria are recorded and reconciled).
- It does not measure how far a judge, model or agent can be trusted. That evidence is read through a port, so any trust-measurement system can supply it.

## Status

Early design. There is no code yet.

## License

[MIT](LICENSE)
