# Capacity Staking

## Basic information  
About [The Capacity Economic Model here](https://github.com/LibertyDSNP/frequency-docs/blob/editing-session/pages/Basics/CapacityModel.md)

## Purpose of Capacity for Frequency

**By Use Case**

* Create an [MSA](#2-message-source-account-msa)
* Add a key to an MSA
* Delegate permissions to another MSA
* Update [Delegate Permissions](#delegate-verb-ie-to-delegate)
* Send a [message](#message)
* Send a [batch message](#batch-message)

**By User Type**

* **Providers:**
Utilize Capacity to put towards user transitions for provider applications and services.
This allows applications to increase their users by reducing costs.
[Maximized Capacity Staking](#2-maximized-capacity-staking-for-applications-and-services) allows Providers to use FRQCY tokens as efficiently as possible, optimizing their Generated Capacity.

* **End Users:**
Do not need to have Capacity directly.
They can delegate to Providers who generate Capacity for them.
Users can participate in [Rewards Capacity Staking](#1-rewards-capacity-staking-for-users) to support services and participate in on-chain governance with Capacity.

## Capacity Implementation Functionality
Capacity is only effective through the technologies of batching, and parallelization of [source-dependent messaging](https://forums.projectliberty.io/t/04-batching-source-dependent-messages-with-delegation/216).
These allow Capacity to play three primary roles in the Frequency ecosystem: incentive alignment, cost management, and volume regulation.

1. **Incentive Alignment:** Capacity works to align independent actors toward increasing the value of the network.
Network value prioritizes the possibilities for connection and the data flowing through them.
Capacity focuses on outcomes instead of testing each message for value.

	* **Penalties and Incentives:**
Those who use Capacity as a utility receive the benefit from it.
Those who dump the token after abusing the network will receive a natural market penalty.
Network and token values are correlated, encouraging those with Capacity to align in the goal of a successful and well-functioning network.

2. **Cost Management:** Capacity acts as an asset, like that of [capital expenditure](https://en.wikipedia.org/wiki/Capital_expenditure), in the sense that it fulfills long-term value.
The FRQCY tokens that generate Capacity are locked, but Generated Capacity is usable again and again.
Regular message sending is allowed without additional costs.

	* **Short-term vs long-term value:**
	Blockchains primarily interact using short-term, per transaction operation expenses, where efficiency demands as few transactions as possible.
	Capacity optimizes flow-through pricing a continuous stream of messages/transactions together rather than as individual transactions.
	This supports the collective value of the messages, in other words, the whole is greater than the sum of its parts.

3. **Volume Regulation:** Frequency has limited space that it needs to allocate.
Capacity Epochs allow for expansion of that space where a Capacity holder can add to the "mempool" (the transaction queue) as many transactions as they have Capacity to cover at the time in the Capacity Epoch cycle.
	* **Rate Limiting:**
	Limiting the rate of transactions ensures a proportional volume of transactions to the amount of Capacity.

	* **Batching and Capacity:**
	More messages require more Capacity.
	Batching requires less Capacity to send messages, part of Frequency’s marginal cost structure.
	When batching, adding one additional message has a tiny marginal cost.
	A batched message is one on-chain message that acts as an anchor tied to a large amount of off-chain data from various MSA accounts.

**Validation protects the integrity of the batch from being manipulated.**
Cryptographic technology protects the integrity of messages through the use of hashes and signatures.
Validation occurs at write time for non-batched messages and at read time for batched messages.
An example from the [DSNP Frequency Implementation](https://spec.dsnp.org/Frequency/Validation.html).

## Capacity Refill
Capacity refills at the start of each Capacity Epoch.
The refillable nature incentivizes services to use Capacity to the best of their user’s needs.
Capacity encourages continual use and sharing; increasing the quantity of data available and thus the value of the network.

**Dynamic Capacity Epoch Development**
These "epochs" form a meta-block that may slowly grow over time.
The growth is a predictable depreciation of Capacity, but rather than influencing price, it increases the lag between refills.
Providers may increase Capacity or allow a minor increase in lag through sending messages.

## Network Costs
Frequency uses minting and burning of FRQCY tokens to manage token supply.
Fees paid in FRQCY tokens are burned and the collators are rewarded by minting new FRQCY tokens.
While generally inflationary, it is required for the network to continue operating and acceptable to token holders.
Collator and token holder values are aligned economically in support of a healthy network.

## Prioritization of Capacity Transactions


Substrate default prioritization is composed of the transaction length, weight, and tip. Adding a tip allows you to increase your priority and thus increases the chance that your transaction is added to the next block.

Capacity transactions do not have the ability to tip, unlike token transactions. This puts Capacity transactions at a disadvantage because in times of high congestion tokens transactions can prevent Capacity transactions from being included in a block.

Initially Capacity transactions are expected to make up the majority of transactions on Frequency.  However, to prevent token transactions from dominating block space in the future, alternate techniques may be used to prioritize Capacity transactions over token transactions. Additionally, a limit may be imposed on the amount of block space Capacity transactions can consume. 