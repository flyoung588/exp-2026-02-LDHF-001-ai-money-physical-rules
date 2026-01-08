Incident ②: Flash Loans — What Actually Happened
1. Design Purpose of Flash Loans

Flash loans were introduced to enable advanced financial operations without requiring upfront capital.
They allow users to borrow large amounts of assets on the condition that the loan is repaid within the same transaction.

The design goal is efficiency:

enabling arbitrage,

collateral swaps,

debt refinancing,

and atomic multi-step operations.

From the system’s perspective, a flash loan is safe because:

either all steps succeed and the loan is repaid,

or the entire transaction is reverted.

There is no partial state.
No long-term credit risk.

2. The Attacker’s Legal Operation Sequence

In typical flash loan attacks, the attacker performs the following steps within a single transaction:

Borrow a large amount of assets using a flash loan.

Use the borrowed assets to manipulate on-chain conditions:

liquidity pools,

price oracles,

or governance thresholds.

Execute actions that depend on the manipulated state:

under-collateralized borrowing,

forced liquidations,

or protocol parameter changes.

Repay the flash loan before the transaction ends.

Every step is valid.
Every call respects permissions.
Every repayment condition is met.

The system executes the transaction exactly as specified.

3. Why the System Did Not Stop It

The system failed to stop the attack because it was not designed to reason about economic intent or temporal manipulation.

Smart contracts typically validate:

balances,

permissions,

and local conditions at the moment of execution.

They do not validate:

whether prices were momentarily distorted,

whether capital was temporarily borrowed,

or whether the economic context is “normal.”

From the system’s point of view:

the inputs were valid,

the conditions were satisfied,

therefore execution proceeded.

The attack did not exploit a broken rule.
It exploited the absence of a rule.
