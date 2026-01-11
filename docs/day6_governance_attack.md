Day 6 — Governance Attacks: When Systems Decide Against Themselves

Decentralized governance is designed to replace trusted decision-makers with transparent, rule-based voting mechanisms.
In theory, this allows protocols to evolve according to the collective will of their stakeholders.

In practice, multiple incidents have shown that governance systems can make decisions that are fully valid, fully authorized, and yet systemically destructive.

Incident Overview

In a typical governance attack, an actor temporarily acquires a large amount of voting power, often through mechanisms such as:

token borrowing,

flash loans,

or low-liquidity accumulation.

With sufficient voting weight, the actor proposes or votes on a governance action that benefits themselves while harming the protocol, such as:

redirecting funds,

changing critical parameters,

or granting privileged permissions.

All steps follow governance rules.
All votes are counted correctly.
All thresholds are met.

The system accepts the outcome as legitimate.

How the System Made a “Wrong” Decision Legally

The governance system did not fail at execution.
It failed at interpretation.

The system assumes that:

voting power represents long-term alignment,

voters bear the consequences of their decisions,

and majority approval implies collective benefit.

However, the system does not verify:

how long voting power was held,

whether voters are exposed to long-term outcomes,

or whether incentives are aligned beyond the voting window.

As a result, governance becomes a momentary state evaluation rather than a reflection of durable consensus.

System-Level Insight

Governance mechanisms do not reason about intent, trust, or sustainability.
They only verify:

balance snapshots,

vote weights,

and rule satisfaction.

When temporary control is sufficient to pass irreversible decisions,
the system can legally authorize actions that undermine its own survival.

This is not a bug.
It is a consequence of how authority is modeled.
