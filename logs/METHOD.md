# Method, pre-run 15

> This is our own Kaspa Testnet-10 testing. What follows is what we observed in this run, on our own nodes; it is not a claim of how TN10 or Kaspa behave in general.

> Counts only. Desk side. Submit-OK is the desk sender log; included is the desk counter's read of what the desk's private TN10 node accepted on chain. Mini's files are a second read.

Steps (our own heavy lane on one absolute timeline): BASE = N0-control 12 min; HOLD-1 = N60-r126 12 min; HOLD-2 = N0-mid 12 min; HOLD-3 = N40-r150 12 min, N60-r150 12 min; then N0-drain through the HOLD-4 minute and RETURN 12 min, then a 5-minute counter tail.

Our heavy lane, from its own log: 15,831 transactions submitted OK of 15,831, 0 rejected, 0 chains lost to an orphan timeout, 6,006 tKAS of fees and 594 tKAS parked on our own sink key, 307 payment-pile coins taken, stop state none.

Accepted hops per cohort, as the desk's coordinator read them: floor 9,487, r150 9,481, r200 10,752, r300 11,787, r450 12,200.

Per step (all OBSERVATION, families plus our own heavy lane, no payment of ours):

- BASE: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r150/r200/r300/r450 2122/1688/1734/1789/1800; counter minutes not kept-pace 0 of 12.
- HOLD-1: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r150/r200/r300/r450 1025/1291/1591/1800/1894; counter minutes not kept-pace 0 of 12.
- HOLD-2: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r150/r200/r300/r450 1764/1628/1749/1851/1883; counter minutes not kept-pace 0 of 12.
- HOLD-3: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r150/r200/r300/r450 1843/2365/2970/3500/3705; counter minutes not kept-pace 0 of 24.
- HOLD-4: OBSERVATION, submit-OK 0; our payments included 0; hops included floor/r150/r200/r300/r450 132/129/131/139/146; counter minutes not kept-pace 0 of 1.
- RETURN: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r150/r200/r300/r450 1646/1500/1610/1703/1733; counter minutes not kept-pace 0 of 12.

Decent on the desk side: every step file reached origin.

## Selection rule, read before the run

The desk node and the kept public kaspads answered serverVersion 2.1.0 at the preflight. In rusty-kaspa tag v2.1.0 (commit 01b532e8b553523216471682649693af92f0fd16), `mining/src/mempool/model/frontier.rs` `build_selector` takes every ready transaction best-first while the ready set's mass fits one block, and otherwise samples at random with weight (fee/mass)^3 (`ALPHA = 3` in `mining/src/mempool/model/frontier/selectors.rs`, weight in `mining/src/mempool/model/frontier/feerate_key.rs`): `sample_inplace` above four blocks' mass, `MutatingTreeSelector` between one and four. Only a transaction with no parent in the mempool is in the ready set (`mining/src/mempool/model/transactions_pool.rs`), so a chained hop is not a candidate until its parent is out of the mempool. Against an outside stream at 100, the weights are 1.00 (100), 2.00 (126), 3.38 (150), 8.00 (200), 27.0 (300) and 91.1 (450), per unit of mass; against our lane at 150 they are 0.30, 1.00, 2.37, 8.00 and 27.0 for the tiers 100, 150, 200, 300 and 450. A higher fee raises the odds; it does not buy a place in a queue. This is the source's rule, read from the code; the run does not see a miner's template.

Hop rates per hop, one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r150 (families 5–7) 150 sompi/gram on the desk's private node, r200 (families 8–10) 200 sompi/gram on the desk's private node, r300 (families 11–13) 300 sompi/gram on the desk's private node, r450 (families 14–16) 450 sompi/gram on the desk's private node. Payments 150. The funding coins were not one size, so the fee is not called the whole cause. Every tier was read and submitted on the desk's private TN10 node, which also ran the counter. No payment sender was started; 2 unique public kaspads were read for sync only.

## Misses

- none

## Fixes

- none

## On origin

- counts/desk/BASE.md: 2026-11-12T20:59:22Z
- counts/desk/HOLD-1.md: 2026-11-12T21:11:22Z
- counts/desk/HOLD-2.md: 2026-11-12T21:23:22Z
- counts/desk/HOLD-3.md: 2026-11-12T21:47:22Z
- counts/desk/HOLD-4.md: 2026-11-12T21:52:22Z
- counts/desk/RETURN.md: 2026-11-12T22:05:22Z
- counts/chain/TIMELINE.md: 2026-11-12T22:10:37Z
- counts/chain/MEMPOOL.md: 2026-11-12T22:10:39Z
