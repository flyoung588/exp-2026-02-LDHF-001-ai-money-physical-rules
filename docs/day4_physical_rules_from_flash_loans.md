Day 4 — Physical Rules Derived from Flash Loans

Flash loan incidents are often discussed as financial exploits or protocol-specific failures.
However, when abstracted from individual cases, they reveal deeper physical rules that apply to all autonomous systems interacting with capital.

Physical Rule 1: Time Is a First-Class Variable, Even When the System Ignores It

Rule Statement

If a system evaluates critical decisions based solely on instantaneous state,
then any actor capable of temporarily manipulating that state can influence irreversible outcomes.

System Explanation

Flash loans allow large amounts of capital to exist for a single transaction.
During this short time window, prices, balances, and governance thresholds can be altered.

From the system’s perspective:

the state is valid,

the inputs satisfy all conditions,

and execution proceeds.

The system does not model how long the state existed.
It treats a one-block condition as equivalent to a long-term equilibrium.

As a result, time becomes an unmodeled variable —
and unmodeled variables become attack surfaces.

Physical Rule 2: Price Is Not Truth, It Is a Snapshot

Rule Statement

Any system that treats price as objective truth, rather than a time-dependent signal,
is vulnerable to state distortion under sufficient capital pressure.

System Explanation

On-chain prices are typically derived from liquidity pools or oracles at a specific moment.
These prices reflect the current state of the pool, not the stability or origin of that state.

Flash loan capital can:

overwhelm liquidity,

shift prices dramatically,

and then exit within the same transaction.

The system records the price, not the process that produced it.

When downstream logic relies on that price to trigger:

liquidations,

collateral valuations,

or governance decisions,

the system converts a transient snapshot into a permanent consequence.

Summary

Flash loan incidents do not break rules.
They expose missing ones.

When time and price dynamics are excluded from system constraints,
capital will naturally exploit the gap.
