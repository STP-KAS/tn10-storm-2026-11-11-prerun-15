> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> Our own testing. What we observed in this run, on our own nodes. Not a claim about how TN10 or Kaspa behave in general. No key, seed, txid, covenant id, address, host or port.

# Lessons, pre-run 15

Written after the run, 2026-11-12, from the files on origin and the desk's own logs (read-only). Times are UTC unless marked Brussels.

## The question

Pre-run 14 read, with hops priced on the node's own mass, that a covenant hop at our heavy lane's rate kept 76–88 percent of its BASE rate and that about twice the lane's rate kept it within about 4 percent. That lane was capped by its own 45-block ready-mass hold. Pre-run 15 asks whether "about twice the competitor's rate" still holds with the lane uncapped (hold raised to 80 blocks on purpose) and with the competitor at 150 instead of 100–126, with tiers up to 450.

## What happened

- Before the open: key 0 consolidated (2,239 small coins into 205), keys 1–15 funded, hop calibration at 100 and 450 (node rates 100.24 and 450.26, node storage mass equal to the builder's), lane calibration (266,671 storage mass, node rate 100.00). Offline rehearsal p15-a exited 0.
- Live run: desk runner 20:45:18Z to `RUN end` 22:10:44Z. BASE 20:47–20:58 (N = 0), HOLD-1 20:59–21:10 (N = 60 at 126), HOLD-2 21:11–21:22 (N = 0), HOLD-3 21:23–21:34 (N = 40 at 150) and 21:35–21:46 (N = 60 at 150), then N = 0 (drain) through the pinned HOLD-4 minute 21:51 and RETURN 21:53–22:04. Every step file, RETURN, TIMELINE, MEMPOOL and METHOD is on origin; every whole minute kept pace; no repair, no restart, nothing killed.
- Every OK family hop was included (counter = submit-OK per tier: 9,492 / 9,484 / 10,755 / 11,790 / 12,203). Every lane transaction was included (15,831 of 15,831, 0 rejected, 0 lost).
- The outside heavy fee-100 stream was present the whole run. We do not say who sends it.
- **The box that runs the bot rebooted at about 21:30Z** and its files rolled back to about 21:28Z. The bot's waiter and finisher were gone. They were relaunched unchanged at 21:42:38Z, before HOLD-3. After the rollback a Node module the bot's free-node check loads was missing, so the check crashed at the pin. See [Bot](#bot).

## The lane

Our own heavy lane (operator's OK, 2026-11-12), about 266,670 storage mass per transaction, chained, one ready transaction per chain.

| Lane step | Minutes | Submits OK | Rejected | Holds (80-block line) | Fees, tKAS |
|---|---:|---:|---:|---:|---:|
| HOLD-1, N = 60 at 126 | 12 | 5,116 | 0 | 0 | 1,726.09 |
| HOLD-3, N = 40 at 150 | 12 | 4,989 | 0 | 0 | 2,004.25 |
| HOLD-3, N = 60 at 150 | 12 | 5,686 | 0 | 0 | 2,275.26 |
| Drain (N = 0) | — | 40 waiting ones landed | 0 | — | — |
| **All** | | **15,831** | **0** | **0** | **6,005.60** (593.66 parked on our sink key, not swept) |

The 80-block hold never tripped, so this lane was not capped by its own hold, unlike pre-run 14's. Median ready mass in the desk mempool was 52.9 blocks at N = 60 @ 126, 47.9 at N = 40 @ 150 and 59.4 at N = 60 @ 150 (BASE 9.9, HOLD-2 23.1). The block template still held a median of one of our heavies.

## Hops per family, per lane step

Median hops per family per minute, and that as a share of BASE (floor has four families, the other tiers three).

| Step | Lane | floor (100) | r150 (150) | r200 (200) | r300 (300) | r450 (450) | Ready mass, blocks (range) | Outside at 100 in mempool, median | Fee estimate, priority |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| BASE 20:47–20:58 | 0 | 44.2 (100%) | 46.8 (100%) | 47.8 (100%) | 49.3 (100%) | 50.0 (100%) | 9.9 (1.3–13.8) | 15 | 245 |
| HOLD-1 20:59–21:10 | 60 @ 126 | 21.6 (49%) | 35.3 (75%) | 44.0 (92%) | 48.8 (99%) | 51.3 (103%) | 52.9 (50.9–56.2) | 1,796 | 384 |
| HOLD-2 21:11–21:22 | 0 | 36.5 (82%) | 44.2 (94%) | 47.3 (99%) | 50.0 (101%) | 50.7 (101%) | 23.1 (22.1–24.8) | 2,483 | 282 |
| HOLD-3a 21:23–21:34 | 40 @ 150 | 21.4 (48%) | 34.7 (74%) | 42.8 (90%) | 48.5 (98%) | 51.3 (103%) | 47.9 (46.1–49.7) | 3,094 | 380 |
| HOLD-3b 21:35–21:46 | 60 @ 150 | 17.0 (38%) | 30.3 (65%) | 38.3 (80%) | 46.8 (95%) | 48.8 (98%) | 59.4 (55.4–62.6) | 6,997 | 404 |
| HOLD-4 21:51 (1 min) | 0 | 33.0 (75%) | 43.0 (92%) | 43.7 (91%) | 46.3 (94%) | 48.7 (97%) | 25.7 | 8,439 | 275 |
| RETURN 21:53–22:04 | 0 | 34.6 (78%) | 41.7 (89%) | 44.3 (93%) | 47.2 (96%) | 48.5 (97%) | 24.4 (23.5–25.7) | 7,823 | 277 |

BASE was light (ready 9.9 blocks); the later N = 0 minutes sat at 23–26 blocks because the outside stream's backlog grew. Against the middle N = 0 control (HOLD-2) instead of BASE, the lane steps read: N = 60 @ 126 60 / 80 / 93 / 98 / 101; N = 40 @ 150 59 / 79 / 91 / 97 / 101; N = 60 @ 150 47 / 69 / 81 / 94 / 96.

## Does about twice the competitor's rate keep a hop's pace?

Share of BASE by hop rate ÷ lane rate:

| Hop rate ÷ lane rate | Lane 60 @ 126 | Lane 40 @ 150 | Lane 60 @ 150 |
|---|---|---|---|
| below 1 (floor) | 0.79: 49% | 0.67: 48% | 0.67: 38% |
| about 1 | 1.19: 75% | 1.0: 74% | 1.0: 65% |
| 1.3–1.6 | 1.59: 92% | 1.33: 90% | 1.33: 80% |
| about 2–2.4 | 2.38: 99% | 2.0: 98% | 2.0: 95% |
| 3–3.6 | 3.57: 103% | 3.0: 103% | 3.0: 98% |

What we observed: with the lane uncapped and the competitor at 150, a hop at about twice the lane's rate kept 95–98 percent of BASE (94–97 against HOLD-2), and 3 times kept 98–103. That is about the pre-run 14 picture (2x: 96–104), slightly weaker at the heaviest step (N = 60 @ 150, ready about 59 blocks), where 2x lost about 5 percent and only 3x held. A hop at the lane's own rate did worse than in pre-run 14 (65–74 against 76–88), as expected with a bigger lane. So, in this run, "about twice the competitor's rate" held as a rough rule up to about 50 blocks of ready mass and needed about 3 times at about 60. One run, one node, 12-minute steps, the outside stream present throughout; we are just testing. Every hop that was submitted OK landed.

## Drain and recovery

The lane went to 0 at 21:47:00Z. Its 52 waiting transactions landed in that minute; from 21:48 none were left. Ready mass fell from 62.0 blocks (21:46) to 29.3 (21:47) and 25.5–27.1 (21:48–21:50), the outside stream's level. Floor hops were 128 in 21:47 and 141–155 in 21:48–21:50 (about 80–88 percent of BASE). RETURN read 78 / 89 / 93 / 96 / 97 percent of BASE, a little under the HOLD-2 control (82 / 94 / 99 / 101 / 101). We read that gap as the outside stream's larger backlog (median 7,823 entries at 100 in RETURN against 2,483 in HOLD-2), not as our lane; we cannot separate the two cleanly.

## Our lane slowed other TN10 users

In the 36 lane minutes, other traffic landed on our desk node had a median of 3,087–3,139 a minute against 3,488–3,567 with the lane at 0, about 10–13 percent lower. The node's priority fee estimate read a median of 380–404 instead of 245–282. The backlog of other transactions at 100 sompi/gram in the desk mempool grew from a median of 15 (BASE) to 1,796 (HOLD-1), 2,483 (HOLD-2), 3,094 and 6,997 (HOLD-3), peaked at about 9,000 just after the lane stopped and was still about 7,200 at the end of the counter's tail; it grew fastest while the lane ran, and it also grew at N = 0, so not all of it is ours. We did this on purpose, with the operator's OK, in bounded steps, and stepped the lane to zero at the end. This is stated in this repo's [public statement](../PLAYBOOK.md#public-statement).

## Bot

The bot sent nothing. Its file, [counts/bot/HOLD-4.md](../counts/bot/HOLD-4.md), says `NO SEND check-failed`, and it was pushed late (on origin 21:55:09Z). Plainly:

- The box that runs the bot rebooted at about 21:30Z and its files rolled back to about 21:28Z. The waiter and finisher were relaunched unchanged at 21:42:38Z with a note in their log.
- The waiter read HOLD-3 3 s after its On origin time (21:47:25Z) and pinned 21:51.
- At pin − 40 s the free-node check crashed: the websocket library it loads from another box folder was gone after the rollback. It read no node. The waiter logged an empty free list and decided no send at **21:50:21Z**, 39 s before the minute. That stands as the decision time.
- The finisher could not render the file (21:52:03Z), because the check's output was an error. The file was written by hand from the logs and pushed at 21:55:09Z. It is not backdated.
- Because no node was read, this is **not** a legal `no-free-node`. The paste's four words do not cover a check that did not run, so the file says `check-failed`.
- After the module path was fixed, the same check run read-only at 21:53:39Z (after the minute) found the kept nodes as 2 distinct kaspads and every other answering node the same kaspad as a kept one: no free node. That is context, not the decision.

Fix kept for the next repo: the check loads its library from a path that survived the reboot, the renderer takes the last line that is a check result and stops with a clear message when there is none, and the bot's setup must run the free check once, read-only, before arming (it would have caught a missing module).

## Mini

Mini read every minute in full (12 / 12 / 12 / 24 / 1 / 12) and matched the desk in **365 of 365** cohort cells, with 0 late removals (pre-run 14: 422 of 425, 42 late removals). Its TN10 kaspad was not wiped or restarted.

## Spend

| Item | tKAS |
|---|---:|
| Our heavy lane, fees | 6,005.60 (593.66 parked on our sink key, not swept) |
| Family hops, fees (floor / r150 / r200 / r300 / r450) | 5,673.43 (397.53 / 595.59 / 900.33 / 1,481.25 / 2,298.73), node mass about 41,800 a hop |
| Consolidation before the open | 2.59 |
| Bot | 0 |
| **About** | **11,680** |

Family submit results other than OK were `already_spent` 48,984 and `orphan` 10,707 (the builder's waiting retries); 0 rate or full rejects. tKAS is not a limit (operator, 12 Nov).

Key 0 after the run (read-only status, about 22:15Z): 320 coins over 3 tKAS, 75,018 usable tKAS (abort line 18,000 never near; 131,430 before the run), 4,872 coins of 3 tKAS or less; keys 1–15 have no genesis coin left. A next run must consolidate first.

## Quirks

- The bot's box reboot and rollback (above). The desk and Mini were not affected.
- BASE was lighter than every later N = 0 minute (ready 9.9 against 23–26 blocks) because the outside stream's backlog grew all run; shares against HOLD-2 are given too.
- The outside stream's backlog in our mempool did not drain by the end of the tail.

## What this seems to show

- With hops priced on the node's mass, paying about twice a heavy competitor's rate kept a covenant hop within about 5 percent of its BASE pace with the competitor uncapped at 126 or 150; at about 60 blocks of ready mass, about 3 times was needed to hold fully.
- Under-pricing hurts much more than over-pricing helps: floor fell to 38–49 percent while r450 never went below 98.
- A big lane at 150 does visible collateral damage to other TN10 users on our node (about 10–13 percent less of their traffic landed, a higher fee estimate, a growing backlog).

## Every minute: hops per family, the lane, the outside stream

| Minute (UTC) | Step | Lane N @ rate | Floor | R150 | R200 | R300 | R450 | Our heavy in mempool | Our heavy landed | Outside heavy at 100 in mempool / ready | Ready mass, blocks | Fee estimate, priority |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 20:47Z | BASE | 0 @ 100 | 46.8 | 50.3 | 52.0 | 52.3 | 52.0 | 0 | 0 | 4 / 4 | 1.98 | 199.5 |
| 20:48Z | BASE | 0 @ 100 | 48.2 | 48.0 | 49.0 | 49.3 | 47.7 | 0 | 0 | 2 / 2 | 1.31 | 231.2 |
| 20:49Z | BASE | 0 @ 100 | 44.0 | 46.3 | 46.7 | 47.3 | 49.7 | 0 | 0 | 9 / 9 | 6.10 | 257.3 |
| 20:50Z | BASE | 0 @ 100 | 46.8 | 45.0 | 47.3 | 50.7 | 50.0 | 0 | 0 | 7 / 7 | 5.11 | 242.6 |
| 20:51Z | BASE | 0 @ 100 | 46.5 | 48.7 | 50.0 | 50.7 | 49.0 | 0 | 0 | 8 / 8 | 3.02 | 232.7 |
| 20:52Z | BASE | 0 @ 100 | 43.5 | 47.0 | 48.3 | 49.3 | 49.0 | 0 | 0 | 18 / 16 | 10.51 | 195.2 |
| 20:53Z | BASE | 0 @ 100 | 42.0 | 45.7 | 47.0 | 49.3 | 50.3 | 0 | 0 | 17 / 16 | 11.28 | 255.9 |
| 20:54Z | BASE | 0 @ 100 | 41.0 | 44.0 | 44.7 | 47.3 | 47.3 | 0 | 0 | 15 / 13 | 9.75 | 233.4 |
| 20:55Z | BASE | 0 @ 100 | 40.8 | 47.0 | 46.7 | 48.7 | 50.0 | 0 | 0 | 35 / 19 | 13.41 | 329.5 |
| 20:56Z | BASE | 0 @ 100 | 40.5 | 45.3 | 47.0 | 48.3 | 50.3 | 0 | 0 | 21 / 18 | 13.82 | 265.8 |
| 20:57Z | BASE | 0 @ 100 | 46.0 | 46.7 | 49.0 | 51.0 | 52.0 | 0 | 0 | 15 / 13 | 10.09 | 270.7 |
| 20:58Z | BASE | 0 @ 100 | 44.5 | 48.7 | 50.3 | 52.0 | 52.7 | 0 | 0 | 17 / 13 | 10.57 | 247.2 |
| 20:59Z | HOLD-1 | 60 @ 126 | 22.2 | 34.3 | 44.7 | 52.3 | 54.0 | 58 | 397 | 212 / 32 | 50.94 | 385.5 |
| 21:00Z | HOLD-1 | 60 @ 126 | 21.8 | 35.3 | 43.0 | 48.0 | 49.3 | 58 | 411 | 596 / 32 | 52.14 | 381.3 |
| 21:01Z | HOLD-1 | 60 @ 126 | 21.8 | 39.7 | 48.3 | 58.0 | 62.0 | 54 | 423 | 947 / 32 | 51.38 | 389.5 |
| 21:02Z | HOLD-1 | 60 @ 126 | 20.8 | 35.3 | 41.3 | 47.0 | 49.3 | 57 | 431 | 1,199 / 32 | 53.64 | 372.5 |
| 21:03Z | HOLD-1 | 60 @ 126 | 21.5 | 35.0 | 41.3 | 45.0 | 48.7 | 56 | 410 | 1,411 / 32 | 52.90 | 342.3 |
| 21:04Z | HOLD-1 | 60 @ 126 | 21.0 | 35.0 | 43.3 | 48.3 | 49.7 | 56 | 445 | 1,675 / 32 | 52.23 | 383.0 |
| 21:05Z | HOLD-1 | 60 @ 126 | 22.0 | 34.3 | 41.7 | 48.0 | 50.7 | 57 | 418 | 1,917 / 32 | 52.83 | 387.4 |
| 21:06Z | HOLD-1 | 60 @ 126 | 21.8 | 36.0 | 49.7 | 54.0 | 57.3 | 57 | 425 | 2,156 / 32 | 54.42 | 387.5 |
| 21:07Z | HOLD-1 | 60 @ 126 | 20.5 | 35.7 | 44.7 | 52.3 | 54.3 | 55 | 402 | 2,407 / 32 | 54.15 | 379.5 |
| 21:08Z | HOLD-1 | 60 @ 126 | 20.5 | 37.3 | 46.3 | 51.3 | 54.3 | 55 | 452 | 2,627 / 32 | 52.89 | 395.2 |
| 21:09Z | HOLD-1 | 60 @ 126 | 23.0 | 39.0 | 44.7 | 49.3 | 52.0 | 60 | 443 | 2,870 / 32 | 56.18 | 353.5 |
| 21:10Z | HOLD-1 | 60 @ 126 | 19.5 | 33.3 | 41.3 | 46.3 | 49.7 | 57 | 423 | 3,108 / 32 | 55.11 | 389.1 |
| 21:11Z | HOLD-2 | 0 @ 100 | 33.5 | 42.7 | 47.7 | 51.3 | 52.3 | 0 | 56 | 3,183 / 32 | 24.82 | 293.6 |
| 21:12Z | HOLD-2 | 0 @ 100 | 37.5 | 43.7 | 49.0 | 50.3 | 50.0 | 0 | 0 | 3,157 / 32 | 23.03 | 265.8 |
| 21:13Z | HOLD-2 | 0 @ 100 | 38.0 | 46.0 | 48.7 | 50.0 | 50.7 | 0 | 0 | 3,127 / 32 | 23.29 | 280.7 |
| 21:14Z | HOLD-2 | 0 @ 100 | 38.2 | 46.7 | 47.0 | 50.0 | 50.7 | 0 | 0 | 3,087 / 32 | 23.09 | 298.6 |
| 21:15Z | HOLD-2 | 0 @ 100 | 36.8 | 44.7 | 46.3 | 48.7 | 48.3 | 0 | 0 | 2,885 / 32 | 22.09 | 281.7 |
| 21:16Z | HOLD-2 | 0 @ 100 | 35.0 | 43.3 | 47.0 | 48.3 | 49.0 | 0 | 0 | 2,631 / 32 | 22.84 | 300.1 |
| 21:17Z | HOLD-2 | 0 @ 100 | 40.0 | 54.3 | 62.0 | 66.3 | 68.7 | 0 | 0 | 2,334 / 32 | 23.28 | 287.1 |
| 21:18Z | HOLD-2 | 0 @ 100 | 35.2 | 40.7 | 44.0 | 48.7 | 48.0 | 0 | 0 | 2,032 / 32 | 22.91 | 281.5 |
| 21:19Z | HOLD-2 | 0 @ 100 | 35.8 | 43.7 | 47.0 | 49.3 | 51.3 | 0 | 0 | 1,798 / 32 | 22.50 | 298.0 |
| 21:20Z | HOLD-2 | 0 @ 100 | 36.2 | 45.3 | 48.7 | 51.7 | 52.3 | 0 | 0 | 1,731 / 32 | 23.74 | 267.0 |
| 21:21Z | HOLD-2 | 0 @ 100 | 35.8 | 43.7 | 45.0 | 47.7 | 50.7 | 0 | 0 | 1,636 / 32 | 23.35 | 265.6 |
| 21:22Z | HOLD-2 | 0 @ 100 | 39.0 | 48.0 | 50.7 | 54.7 | 55.7 | 0 | 0 | 1,591 / 32 | 22.66 | 257.6 |
| 21:23Z | HOLD-3 | 40 @ 150 | 23.2 | 35.0 | 43.3 | 47.7 | 49.7 | 39 | 430 | 1,740 / 32 | 46.07 | 385.9 |
| 21:24Z | HOLD-3 | 40 @ 150 | 23.2 | 35.0 | 44.7 | 53.7 | 58.3 | 39 | 393 | 2,081 / 32 | 47.88 | 399.9 |
| 21:25Z | HOLD-3 | 40 @ 150 | 19.0 | 42.3 | 51.0 | 64.3 | 67.7 | 40 | 413 | 2,411 / 32 | 47.46 | 386.5 |
| 21:26Z | HOLD-3 | 40 @ 150 | 21.5 | 33.3 | 41.7 | 49.3 | 52.0 | 39 | 423 | 2,685 / 32 | 47.84 | 391.0 |
| 21:27Z | HOLD-3 | 40 @ 150 | 20.0 | 35.7 | 42.3 | 46.3 | 48.0 | 40 | 407 | 2,891 / 32 | 49.13 | 383.3 |
| 21:28Z | HOLD-3 | 40 @ 150 | 22.5 | 34.0 | 42.0 | 46.7 | 51.0 | 36 | 408 | 3,014 / 32 | 48.53 | 393.0 |
| 21:29Z | HOLD-3 | 40 @ 150 | 20.0 | 35.0 | 44.3 | 53.3 | 55.7 | 34 | 394 | 3,173 / 32 | 46.77 | 327.5 |
| 21:30Z | HOLD-3 | 40 @ 150 | 23.2 | 36.3 | 43.3 | 48.0 | 50.7 | 40 | 432 | 3,446 / 32 | 49.69 | 371.9 |
| 21:31Z | HOLD-3 | 40 @ 150 | 23.8 | 34.3 | 46.0 | 51.3 | 53.7 | 37 | 429 | 3,801 / 32 | 48.45 | 369.8 |
| 21:32Z | HOLD-3 | 40 @ 150 | 21.2 | 32.0 | 41.7 | 48.3 | 51.7 | 37 | 420 | 4,179 / 32 | 48.48 | 376.1 |
| 21:33Z | HOLD-3 | 40 @ 150 | 20.0 | 33.7 | 41.0 | 48.7 | 49.3 | 34 | 390 | 4,530 / 32 | 46.84 | 366.6 |
| 21:34Z | HOLD-3 | 40 @ 150 | 19.8 | 33.3 | 40.0 | 47.7 | 49.3 | 35 | 420 | 4,902 / 32 | 47.50 | 366.8 |
| 21:35Z | HOLD-3 | 60 @ 150 | 18.5 | 32.7 | 43.7 | 50.3 | 53.7 | 48 | 523 | 5,247 / 32 | 55.39 | 405.6 |
| 21:36Z | HOLD-3 | 60 @ 150 | 17.8 | 32.7 | 40.0 | 48.0 | 51.3 | 58 | 471 | 5,537 / 32 | 60.01 | 390.5 |
| 21:37Z | HOLD-3 | 60 @ 150 | 15.8 | 30.3 | 38.3 | 46.0 | 48.7 | 57 | 461 | 5,926 / 32 | 58.19 | 405.9 |
| 21:38Z | HOLD-3 | 60 @ 150 | 20.5 | 30.0 | 38.3 | 46.0 | 47.0 | 52 | 473 | 6,323 / 32 | 56.12 | 393.5 |
| 21:39Z | HOLD-3 | 60 @ 150 | 14.5 | 30.0 | 39.7 | 45.7 | 48.7 | 50 | 469 | 6,655 / 32 | 55.92 | 403.9 |
| 21:40Z | HOLD-3 | 60 @ 150 | 16.0 | 29.0 | 38.0 | 48.7 | 52.0 | 52 | 445 | 6,892 / 32 | 58.85 | 419.8 |
| 21:41Z | HOLD-3 | 60 @ 150 | 15.0 | 29.7 | 36.3 | 43.7 | 48.0 | 59 | 444 | 7,102 / 32 | 62.63 | 403.2 |
| 21:42Z | HOLD-3 | 60 @ 150 | 18.0 | 32.7 | 41.0 | 48.0 | 52.0 | 56 | 470 | 7,300 / 32 | 60.34 | 411.7 |
| 21:43Z | HOLD-3 | 60 @ 150 | 14.8 | 29.0 | 38.3 | 45.0 | 48.7 | 56 | 471 | 7,611 / 32 | 60.04 | 377.4 |
| 21:44Z | HOLD-3 | 60 @ 150 | 18.5 | 30.3 | 38.3 | 48.7 | 52.0 | 53 | 494 | 8,008 / 32 | 58.80 | 394.8 |
| 21:45Z | HOLD-3 | 60 @ 150 | 17.5 | 31.3 | 39.0 | 47.7 | 49.0 | 54 | 468 | 8,413 / 32 | 61.18 | 405.0 |
| 21:46Z | HOLD-3 | 60 @ 150 | 16.5 | 30.7 | 37.7 | 43.7 | 47.0 | 57 | 495 | 8,789 / 32 | 62.00 | 413.9 |
| 21:51Z | HOLD-4 | 0 @ 100 | 33.0 | 43.0 | 43.7 | 46.3 | 48.7 | 0 | 0 | 8,439 / 32 | 25.67 | 274.7 |
| 21:53Z | RETURN | 0 @ 100 | 35.2 | 43.0 | 47.0 | 48.0 | 49.3 | 0 | 0 | 8,164 / 32 | 23.92 | 260.5 |
| 21:54Z | RETURN | 0 @ 100 | 34.2 | 42.0 | 45.0 | 46.0 | 48.7 | 0 | 0 | 8,039 / 32 | 24.74 | 289.4 |
| 21:55Z | RETURN | 0 @ 100 | 35.5 | 42.7 | 43.0 | 46.7 | 46.0 | 0 | 0 | 7,898 / 32 | 24.07 | 235.5 |
| 21:56Z | RETURN | 0 @ 100 | 33.0 | 42.3 | 45.7 | 49.3 | 48.3 | 0 | 0 | 7,886 / 32 | 24.06 | 258.0 |
| 21:57Z | RETURN | 0 @ 100 | 33.8 | 41.0 | 44.3 | 48.7 | 47.3 | 0 | 0 | 7,863 / 32 | 25.52 | 294.3 |
| 21:58Z | RETURN | 0 @ 100 | 31.5 | 39.3 | 43.0 | 42.7 | 43.0 | 0 | 0 | 7,867 / 32 | 25.71 | 281.5 |
| 21:59Z | RETURN | 0 @ 100 | 35.0 | 40.7 | 44.0 | 47.0 | 49.0 | 0 | 0 | 7,782 / 32 | 24.33 | 335.4 |
| 22:00Z | RETURN | 0 @ 100 | 35.8 | 44.0 | 46.0 | 50.0 | 50.3 | 0 | 0 | 7,599 / 32 | 23.47 | 273.3 |
| 22:01Z | RETURN | 0 @ 100 | 36.0 | 41.3 | 44.3 | 47.3 | 49.3 | 0 | 0 | 7,415 / 32 | 24.42 | 269.0 |
| 22:02Z | RETURN | 0 @ 100 | 32.5 | 38.7 | 43.7 | 47.0 | 50.7 | 0 | 0 | 7,230 / 32 | 24.00 | 296.0 |
| 22:03Z | RETURN | 0 @ 100 | 33.0 | 40.7 | 43.0 | 46.0 | 47.3 | 0 | 0 | 7,220 / 32 | 25.49 | 297.5 |
| 22:04Z | RETURN | 0 @ 100 | 36.0 | 44.3 | 47.7 | 49.0 | 48.3 | 0 | 0 | 7,239 / 32 | 24.94 | 171.1 |

## What a next attempt could try (not opened)

- A real fee duel: two independent lanes escalating against each other, instead of fixed tiers against a fixed lane.
- Read hop landing time per tier, not only hops per minute.
- Consolidate key 0 first (320 coins over 3 tKAS left).
- Run the bot's free check once, read-only, before arming.
