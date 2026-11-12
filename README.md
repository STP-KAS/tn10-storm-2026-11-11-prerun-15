> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 15.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, or 14. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-15

**Pre-run 15 of the Wednesday neuron.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo, does not write `REVIEW_CLOSED`, and does not set or move a clock for it. [tn10-storm-2026-11-10](https://github.com/STP-KAS/tn10-storm-2026-11-10) (Tuesday) is not edited from here either.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

**Where this starts.** Pre-runs 1 to 4 failed and are closed. Pre-runs 5 to 12 finished through RETURN and are closed. Pre-run 13 ran through the pinned HOLD-4 minute and failed in RETURN on its coin-count abort line; it is closed. Pre-run 14 finished through RETURN and is closed. The index of all of them is the [pre-run 2 README](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-2#pre-runs-in-this-rehearsal); the cumulative findings are in [tn-master](https://github.com/STP-KAS/tn-master). This repo starts from [pre-run 14's locks/LOCKED.md](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-14/blob/53e1036/locks/LOCKED.md) at commit 53e1036, copied here as [locks/LOCKED.md](locks/LOCKED.md), with a pre-run 15 section added at the end.

## What pre-run 14 left open

[Pre-run 14](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-14) was the first run with every covenant hop priced on the node's own mass (tiers 100, 126, 150, 200, 300 by node rate) against our own heavy lane at N = 20 and 40, at 100 and at 126. As we observed it there: a hop at the lane's rate lost 12–24 percent of its BASE rate, at about 1.6–2 times the lane's rate it stayed within about 4 percent, and at 2.4–3 times it held. Two things limited that reading: the lane's own ready-mass hold (45 blocks) capped N = 40, because the outside heavy stream's ready entries counted too, and the competitor was never above 126. One run, one node.

## What pre-run 15 tries

The question: **does the "about twice the competitor's rate" protection seen in pre-run 14 hold (a) when our heavy lane is not capped by its own hold, and (b) at a higher competitor level (150)?**

> **We run our own heavy lane on TN10 again, and it slows other TN10 users' transactions.** In this pre-run we submit our own bounded stream of heavy transactions (about 266,670 storage mass each, at 126 and then at 150 sompi/gram, up to 60 at a time) from our own test coins. While it runs, other TN10 users' transactions paying up to about the lane's rate wait longer. The operator gave the explicit OK for the lane (2026-11-12) and said tKAS is not a limit. It is calibrated on the node first, capped by ready count, by a per-minute submit cap and by a spend cap, stepped down to zero at the end, and every step is in this repo. This is our own testing; tKAS has no value.

- **Tiers (kit22 = kit21 with a new table), by node rate:** floor (families 1–4) 100, r150 (5–7) 150, r200 (8–10) 200, r300 (11–13) 300, r450 (14–16) 450 sompi/gram. Against the lane at 126, r300 is about 2.4 times and r450 about 3.6 times; against the lane at 150, r300 is 2 times and r450 3 times. Every hop priced on the node's mass as in pre-run 14; one build, one builder, every tier on the desk's private node. No payment load of ours.
- **Calibrated on the node before the open.** One calibration covenant (not one of the sixteen families), one hop at 100 and one at 450, read back from the desk mempool: see [PLAYBOOK.md](PLAYBOOK.md#status-when-this-repo-was-opened).
- **Our heavy lane** as in pre-runs 13–14, with three changes on purpose: the ready-mass hold is raised from 45 to **80 blocks**, the submit cap from 600 to **1,200 a minute**, and the lane may run at 150. Calibrated again before the open.
- **Steps on one timeline, 12 whole minutes each:** BASE (N = 0), HOLD-1 = N = 60 at 126 (the lane uncapped: its ready-mass hold raised from 45 to 80 blocks), HOLD-2 = N = 0 (the middle control), HOLD-3 = N = 40 then 60 at 150, then N = 0 (the drain) through the pinned HOLD-4 minute and RETURN (12 minutes), and the counter's 5-minute tail. All are `OBSERVATION`. The HOLD file names are kept so the bot's and Mini's gates read as before.
- **Guards.** The lane's other guards are pre-run 14's (N + 2 pause, hold at mempool 90,000, stop at 16,000 tKAS of fees or 20,000 tKAS moved or the pile under 100,000 tKAS, stop on a non-timing rejection or a drift from the calibration). The family lane's abort line stays **18,000 usable tKAS**. The bot waiter keeps pre-run 14's fetch handling.

All locked lines from earlier pre-runs stay, except where the pre-run 15 block in [locks/LOCKED.md](locks/LOCKED.md) says what changes and why.

## Machines

| Machine | Go file | First sentence |
|---|---|---|
| Desk | [GO-DESK.md](GO-DESK.md) | DESK. I send and count on pre-run 15. This is not Wednesday. |
| Mini | [GO-MINI.md](GO-MINI.md) | MINI. I count pre-run 15 as the second read. I do not send. This is not Wednesday. |
| Bot | [GO-BOT.md](GO-BOT.md) | GROKBOT. I send payments on the pre-run 15 HOLD-4 only. I do not count. This is not Wednesday. |

The operator does not paste. On 2026-11-12 he asked TN10 ops for covenant pre-runs under congestion and competition, pre-run 11 and then 12, 13 or more as needed (voice, 09:06 and 09:09 Brussels time), and at 10:04 in chat said "Keep exploring". For our own heavy lane he gave the explicit OK in chat at about 11:08 and 11:10 Brussels time ("Do whatever you think is needed", then "No need to keep it short. Tn is for testing. Test at will"), and at 15:19 he said tKAS is not a limit ("Use all the tkas you want"). That is the arm for pre-run 15 and its heavy lane. The agents start the runners once the gates are facts. [GO.md](GO.md) is the map, [PLAYBOOK.md](PLAYBOOK.md) has the roles and gates, and [plan/PLAN.md](plan/PLAN.md) has the targets and the reasons.

## Gates, in order

No clock. Each gate is a fact read from a node or from origin.

1. Mini's TN10 node is up from its own data, synced, DAA moving.
2. The desk's private TN10 node is up from its own data (PowerShell 7), synced, DAA moving.
3. No other runner or waiter is up. The family lane is above its abort line (18,000 usable tKAS). The desk's private candidate list is present.
4. `hashes/SIXTEEN.md` is on origin: sixteen rows and an On origin line, from the sixteen-family path.
5. The desk pushes `logs/PRE-RUN-OPEN.md`; Mini pushes `logs/MINI-ARMED.md`.
6. The probe and the desk counter are up. Then the families, our heavy lane at N = 0, and the observation steps on the lane's timeline.

Before the open: the hop calibration (node rate within 1 percent of 100 and of 450) and the lane's calibration passed.

## What a decent result is

- `hashes/SIXTEEN.md` on origin before the first family submit.
- Every step file on origin, each with hops per minute for all five tiers (floor, r150, r200, r300, r450), each tier's node rate, the lane's N and rate, our heavy and the outside heavy apart, and the probe's table for the same minutes.
- `counts/chain/TIMELINE.md` and `counts/chain/MEMPOOL.md` after the tail, and RETURN on origin.
- An answer to the question, or an honest "not answered" with the reason.
- A HOLD-4 desk file, a bot file or a legal `NO SEND`, and a Mini file.
- The spend and the leftovers (the parked sink outputs, not swept) stated in the write-up.
- No id, txid, key, address, host, or port in this repo.

A miss stays in this repo. A next attempt is a new repo and starts from this repo's lock file.

**Part of [tn-master](https://github.com/STP-KAS/tn-master).** The rule is [docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md). This pre-run is its own row. It is not row 47.
