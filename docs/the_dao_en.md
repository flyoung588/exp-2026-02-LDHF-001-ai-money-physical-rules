# Incident ① — The DAO (2016): The Beginning of Rules Being Legally Exploited

**Short description**

The DAO was a decentralized investment fund deployed on Ethereum. Its goal was to let participants decide on funding allocations via smart contracts without trusting a central manager. Participants contributed ETH to the contract to receive DAO tokens, then used those tokens to vote on investment proposals. In design, The DAO aimed to replace traditional fund managers with code and thus reduce the risk of human malfeasance.

**What went wrong**

The flaw appeared in the withdrawal mechanism. When a user chose to withdraw, the contract would send the corresponding ETH to the user's address based on token holdings, and then update the user's balance in the contract state.

An attacker discovered that ETH was sent **before** the contract updated its internal state. Exploiting this, the attacker created a contract address that, upon receiving ETH, recursively called the withdrawal function again. Because the system had not yet updated the attacker's balance, it still "believed" the attacker retained the original balance and therefore repeatedly executed legitimate transfers.

During the entire sequence:
- There was no breach of cryptography,
- There was no privilege escalation,
- No rule of the contract was violated.

The contract simply and correctly executed the logic it had been written with. In the end, roughly 3.6 million ETH were moved into attacker-controlled child DAOs, causing the largest systemic incident in the Ethereum ecosystem at that time.

---

# Extracted physical rules from The DAO incident

## Physical Rule 1 — Before state is updated, the system cannot perceive that a fact has already occurred

**Rule statement**

> If an external call occurs before an internal state update,  
> then in a reentrant execution environment,  
> the system will repeatedly perform legally-correct actions based on stale state.

**System-facing explanation**

When The DAO executed its withdrawal logic, it sent ETH to an external address before updating the user's balance. From the system's perspective, until the state variable is modified, the fact "user balance unchanged" still holds. Therefore, when the attacker re-entered the same function via an external contract call, the system had no indication that ETH had already been transferred and continued execution according to the old state.

---

## Physical Rule 2 — Code is not accountable for overall outcomes; it is only accountable for the current instruction

**Rule statement**

> If a system is designed to guarantee correctness of individual steps but does not enforce cross-step, global consistency,  
> then the system may reach catastrophic results entirely through legally-correct executions.

**System-facing explanation**

Each individual transfer executed by The DAO was legal and conformed to contract logic. The system was never required to determine whether that particular execution would lead to the total depletion of funds. It was only required to execute current instructions when the present conditions were met. The final loss was not due to a "bug" in the single-step logic but due to the faithful and literal execution of the written rules.

