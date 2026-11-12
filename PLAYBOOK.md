> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is the playbook for pre-run 15.** It is not Wednesday. It is not Tuesday. It is not pre-run 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, or 14. It does not start a machine and it does not arm one.

# Playbook

Who does what, and the gates before each machine may start. The plan is [plan/PLAN.md](plan/PLAN.md), the locks are [locks/LOCKED.md](locks/LOCKED.md), and the go files are the three GO pages. This page does not override them.

## Oversight

TN10 ops oversees this rehearsal end to end: Mini, the desk (Build), and the bot. TN10 only. Never mainnet. Do not edit the Tuesday repo, the Wednesday repo, or pre-run 1's to 14's go files. Do not write `REVIEW_CLOSED`.

For pre-run 15 the operator does not paste. On 2026-11-12 he asked TN10 ops for covenant pre-runs under congestion and competition, pre-run 11 and then 12, 13 or more as needed (voice, 09:06 and 09:09 Brussels time), and at 10:04 in chat said "Keep exploring". That is the arm. The agents start their runners once the gates are facts.

## Start gates

1. **Mini node synced.** Existing TN10 kaspad, existing data, no wipe. `isSynced` true, DAA moving.
2. **Desk node synced.** Existing private TN10 kaspad, existing data, loopback only, started with `pwsh`. No wipe. Synced, DAA moving.
3. **No other runner.** No earlier runner, waiter, or counter on any machine. Lane above the abort line. The desk's private candidate list is present and not empty (`HELD candidates-missing` otherwise).
4. **Hashes.** `hashes/SIXTEEN.md` with sixteen rows and an On origin line, from [tools/sixteen](tools/sixteen/README.md).
5. **Open.** The desk pushes `logs/PRE-RUN-OPEN.md`. Mini then pushes `logs/MINI-ARMED.md`.
6. **Counter, families, senders.** The desk runner starts the counter on its private node and waits for its start line (`HELD counter-down` otherwise). Then the genesis from the bundle that wrote `hashes/SIXTEEN.md`, the families, and the payment steps.

## Who does what

| Who | Role | What not to do |
|---|---|---|
| **Desk (Build)** | Sends the sixteen families (five fee tiers by node rate, one path, one build, kit22) and runs our own heavy lane (the operator's OK, calibrated first). No payments. Its private TN10 node counts what the chain accepted (lock line (iv)) and its probe reads the mempool (xii). Publishes `hashes/SIXTEEN.md`, `logs/PRE-RUN-OPEN.md`, `counts/desk/` per step, `counts/chain/TIMELINE.md` and `MEMPOOL.md` after the tail, and `logs/METHOD.md`. | Do not stop or wipe the desk node. No Windows PowerShell 5.1, no `KaspaPublicNode`, no miner, no devnet. No 8- or 32-family publisher. No second runner. Never restart the runner mid-run. No payment sender. No heavy lane other than the runner's own lane process. |
| **Mini** | Second chain read on its own node. Does not send, mine, or hold a key. Publishes `logs/MINI-ARMED.md`, then `counts/mini/` when the matching desk file is on origin. | Do not wipe. Do not repeat the desk's head as Mini's. |
| **Bot (TN10 ops)** | Sends payments in the HOLD-4 minute only, on a synced public kaspad that is not one the desk kept, or publishes a legal `NO SEND`. | Do not send in any other step. One waiter. No local node. |

## Status when this repo was opened

Not a gate. Read on 2026-11-12 between 20:13Z and 20:30Z. This is our own TN10 testing; status lines are what we read on our own machines.

- Mini: existing TN10 kaspad 2.1.0 up, no wipe. Pre-run 14's Mini runner ended on its own at 2026-11-12T20:07:43Z.
- Desk: existing private TN10 kaspad 2.1.0 up with `pwsh`, no wipe. It is not stopped for this pre-run. No pre-run 14 runner or child is running. `serve.mjs` and its keeper are not touched.
- Box: no local TN10 node. No bot waiter running.
- **Family lane** (key 0), 20:15:54Z: 5,005 coins over 3 tKAS, 126,748 usable tKAS, 2,239 coins of 3 tKAS or less. **Consolidated again** 20:16:26Z: 30 transactions, none rejected, those 2,239 coins (5,531 tKAS) into 205 coins of about 25 tKAS, 2.59 tKAS in fees. A refill from the payment key was not needed.
- Keys 1–15 got a fresh genesis coin from the family lane (15 transactions at 20:16:57Z, none rejected). Three of them came out a few thousandths of a tKAS under the 15 tKAS genesis line (the smallest source coins less the fee), so keys 1–3 were funded once more at 20:18:12Z from coins of 16 tKAS or more (3 transactions, none rejected); the funding script now takes only those. Amounts and ids are in private notes.
- **Hop calibration on the node** (kit22), 20:17:31Z: one calibration covenant on key 0 (launch path `…-p15-cal`, not one of the sixteen families and not in `SIXTEEN.md`), its genesis, then two hops built by the family path and submitted on the desk's private node, each read back from the desk mempool 2–3 ms after the submit:

| Hop | Builder bill rate (on 13,046) | kit22 storage mass | Node storage mass | Node compute mass | Fee, sompi | Node rate (fee ÷ node mass) |
|---|---:|---:|---:|---:|---:|---:|
| tier 100 | 316 | 41,126 | 41,126 | 9,123 | 4,122,536 | 100.24 |
| tier 450 | 1,426 | 41,317 | 41,317 | 9,123 | 18,603,596 | 450.26 |

  Storage mass matched to the unit, and both node rates were within 1 percent of the tier (and not under it), so the families may run on kit22.
- **Our heavy lane's calibration**, 20:17:35Z: one lane transaction as the lane builds it. SDK storage mass 266,671, node storage mass 266,671 (0.00 percent off), compute 2,036, node rate 100.00. The sink key is pre-runs 13–14's (it holds their parked outputs, not swept).
- Re-read before the hashes, 2026-11-12 20:20Z–20:24Z (read-only; nothing restarted): the desk's private node TN10, synced, UTXO index, DAA moving; no runner, waiter, probe or counter of ours up on the desk or Mini; Mini's TN10 node up. Family lane 5,192 coins over 3 tKAS, 131,430 usable tKAS, no coin of 3 tKAS or less; keys 1–15 each hold a genesis coin; payment key 7,722 coins. **The outside heavy stream was present but light:** nine reads of the desk mempool 20 seconds apart held 0 to 6 entries over 200,000 mass, every one at a fee rate of 100, none of them ours (our lane was not running). We do not say whose it is.
- Known risks, not fixed mid-run:
  - Our lane slows other TN10 users' transactions at fees up to about its own rate while it runs; at N = 60 and at 150 more than in pre-run 14. The operator OK'd that; the steps are bounded and the lane steps down to zero.
  - The outside heavy fee-100 stream may also be there; the probe counts it apart from ours.
  - About one heavy transaction fits a block, so heavies (ours and outside) together land at most near 600 a minute; N = 60 may not land more than N = 40 did.
  - With the hold at 80 blocks the ready mass may go higher than in any earlier pre-run; the mempool hold (90,000) stays.
  - Each family is a chain of hops, so a hop waits for its parent whatever its fee.
  - The probe reads the desk node's mempool and template, not a miner's.
  - Only two unique public kaspads answered in every check so far, and the desk keeps both, so the bot is expected to file `NO SEND no-free-node`.

## Offline rehearsal, recorded before `PRE-RUN-OPEN`

Rehearsal p15-a, on the desk, offline, 2026-11-12 20:26:52Z–20:43:01Z: a local bare origin with fake `SIXTEEN.md` rows (random ids, local only, never pushed to GitHub), a fake payment-key node (our lane's submits went only to it), the fake family sender with kit22's tier table, and this repo's runner, probe, counter and lane files byte for byte. Steps shortened to 1 minute each (RETURN 2). Result: `RUNNER_EXIT 0`. `FEE_SPLIT` verified on the submit rows for all five tiers (floor 100, r150 150, r200 200, r300 300, r450 450); the lane plan read `BASE N0 | HOLD-1 N60-r126 | HOLD-2 N0 | HOLD-3 N40-r150 + N60-r150 | drain`, and the lane took each N and rate on the minute boundary, including 150 (3,254 accepted by the stand-in, 0 rejected, 0 lost, no hold, `LANE_END` clean, nothing pending). Every step file, HOLD-4, RETURN, `TIMELINE`, `MEMPOOL` and `METHOD` rendered with the five new tier columns and the node-rate table. No runner, probe, counter, lane or builder of the rehearsal was left running. Nothing reached a real node except read-only reads.

## Status after the live run

Read on 2026-11-12 between 21:53Z and 22:15Z. Not a gate.

- **The run finished through RETURN.** The desk runner (started 20:45:18Z) ran BASE, HOLD-1, HOLD-2, HOLD-3, the pinned HOLD-4 minute (21:51Z) and RETURN without a repair or a restart, every whole minute kept pace, then stopped on its own (`RUN_STOP return-closed` 22:05:25Z, 5-minute counter tail, `RUN end` 22:10:44Z) and published `counts/chain/TIMELINE.md`, `counts/chain/MEMPOOL.md` and [logs/METHOD.md](logs/METHOD.md). No runner process was left on the desk. The private TN10 kaspad (2.1.0) was not stopped. No devnet, `KaspaPublicNode` or miner was started; `serve.mjs` and its keeper were not touched.
- Our heavy lane: `LANE_END` 22:05:25Z, 15,831 accepted of 15,831, 0 rejected, 0 lost, 6,005.60 tKAS fees, 593.66 tKAS parked on our sink key (not swept), nothing pending. The 80-block ready-mass hold never tripped.
- Mini: the runner (MINI-ARMED 20:44:39Z) published a second read for every step, each read in full, and matched the desk in 365 of 365 cohort cells with 0 late removals. Its TN10 kaspad was not wiped or restarted.
- Bot: **the box that runs the bot rebooted at about 21:30Z and its files rolled back to about 21:28Z.** The waiter and finisher were relaunched unchanged at 21:42:38Z, before HOLD-3. The waiter read HOLD-3 3 s after origin and pinned 21:51Z, but its free-node check crashed at pin − 40 s (a library it loads was missing after the rollback) and read no node. It decided no send at 21:50:21Z. The finisher could not render the file; it was written from the logs and pushed late (on origin 21:55:09Z), not backdated, as `NO SEND check-failed` — not a legal `no-free-node`. Nothing was sent by the bot. A read-only check after the minute found no free node (context only).
- Keys after the run (status read about 22:12Z): key 0 320 coins over 3 tKAS, 75,018 usable tKAS (abort line 18,000 never near), 4,872 coins of 3 tKAS or less; payment key 7,458 coins over 10 tKAS; keys 1–15 have no genesis coin left.
- The outside heavy fee-100 stream was present all run. We do not say who sends it.
- Results: [logs/LESSONS.md](logs/LESSONS.md), [logs/METHOD.md](logs/METHOD.md), and the pre-run 15 block in [locks/LOCKED.md](locks/LOCKED.md).

### Public statement

We run our own heavy lane on TN10 in this pre-run, with the operator's OK, at N = 60 at 126 and then N = 40 and 60 at 150 sompi/gram, for about 36 minutes in all. While it runs, other TN10 users' transactions paying up to about the lane's rate wait longer on the nodes that see it. In this run, in the 36 lane minutes, other traffic landed on our desk node fell by about 10–13 percent (median about 3,090–3,140 a minute against 3,490–3,570 with the lane at 0), the node's priority fee estimate read a median of 380–404 instead of 245–282, and the backlog of other users' transactions at 100 sompi/gram in the desk mempool grew, fastest while the lane ran (it also grew at N = 0, so not all of it is ours), and was still about 7,200 at the end. The lane was stepped down to zero at the end and its own 52 waiting transactions cleared within a minute. This is our own testing; tKAS has no value.

## When something breaks

Append a worked fix to [locks/LOCKED.md](locks/LOCKED.md) in the form that page shows, and a repair line to `logs/FIXES.md`. If the run dies before RETURN, write `logs/FAILED.md`, stop every runner, waiter, and counter, and do not resume. The next attempt is a new repo that starts from this repo's lock file.
