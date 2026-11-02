# LegateAI

Graduated autonomy and approval for AI agents.

A legate acts under a bounded commission: free inside it, accountable for it, and obliged to come back when a decision falls outside it. LegateAI is the layer that decides **how an agent decides** and **who it asks** — so an owner can delegate work without losing the say on what matters.

## Role

1. **Small decisions are made alone.** The agent decides, tells the owner, and keeps the decision reversible.
2. **Important decisions ask for a choice.** The agent presents options, each with its grounds and trade-offs, and recommends one. If it cannot recommend, it asks about the *criterion*, not the case. If the owner picks something other than the recommendation, it asks for the underlying criterion rather than the surface reason.
3. **Decision processes are kept consistent.** Recorded criteria and decision flows are checked against each other. When they conflict, the agent asks the owner to align them, so the criteria converge instead of drifting apart.

## Scope

- LegateAI owns the *form* of a decision (what counts as important, how a choice is presented, how criteria are recorded and reconciled).
- It does not measure how far a judge, model or agent can be trusted. That evidence is read through a port, so any trust-measurement system can supply it.

## Status

Early design. There is no code yet.

## License

[MIT](LICENSE)
