OBSERVATION

Not scored. No payment of ours in pre-run 15: families only, on the desk's private node, plus our own heavy lane at the N shown per minute.

# HOLD-2, desk, pre-run 15

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-2 in pre-run 15 is lane N=0 (the middle control): N0-mid 12 whole minutes. Families only for payments (no payment of ours); our own heavy lane ran at the N and rate shown per minute (N = how many lane chains may each hold one ready transaction in the mempool). The HOLD file names are kept so the bot's and Mini's gates read as in earlier pre-runs. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r150 (families 5–7) 150 sompi/gram on the desk's private node, r200 (families 8–10) 200 sompi/gram on the desk's private node, r300 (families 11–13) 300 sompi/gram on the desk's private node, r450 (families 14–16) 450 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | Lane N / rate | floor (100) | r150 (150) | r200 (200) | r300 (300) | r450 (450) | Our heavy in mempool / ready | Our heavy landed | Lane submits OK | Outside heavy at 100 (>200k mass) / ready | Outside at 100, n | Ready mass, blocks | Mempool | Fee estimate priority |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T21:11 | 0 / 100 | 134 | 128 | 143 | 154 | 157 | 0 / 0 | 56 | 0 | 3,183 / 32 | 3,183 | 24.82 | 3,234 | 293.6 |
| 2026-11-12T21:12 | 0 / 100 | 150 | 131 | 147 | 151 | 150 | 0 / 0 | 0 | 0 | 3,157 / 32 | 3,157 | 23.03 | 3,186 | 265.8 |
| 2026-11-12T21:13 | 0 / 100 | 152 | 138 | 146 | 150 | 152 | 0 / 0 | 0 | 0 | 3,127 / 32 | 3,127 | 23.29 | 3,165 | 280.7 |
| 2026-11-12T21:14 | 0 / 100 | 153 | 140 | 141 | 150 | 152 | 0 / 0 | 0 | 0 | 3,087 / 32 | 3,087 | 23.09 | 3,161 | 298.6 |
| 2026-11-12T21:15 | 0 / 100 | 147 | 134 | 139 | 146 | 145 | 0 / 0 | 0 | 0 | 2,885 / 32 | 2,885 | 22.09 | 2,924 | 281.7 |
| 2026-11-12T21:16 | 0 / 100 | 140 | 130 | 141 | 145 | 147 | 0 / 0 | 0 | 0 | 2,631 / 32 | 2,631 | 22.84 | 2,677 | 300.1 |
| 2026-11-12T21:17 | 0 / 100 | 160 | 163 | 186 | 199 | 206 | 0 / 0 | 0 | 0 | 2,334 / 32 | 2,334 | 23.28 | 2,396 | 287.1 |
| 2026-11-12T21:18 | 0 / 100 | 141 | 122 | 132 | 146 | 144 | 0 / 0 | 0 | 0 | 2,032 / 32 | 2,032 | 22.91 | 2,082 | 281.5 |
| 2026-11-12T21:19 | 0 / 100 | 143 | 131 | 141 | 148 | 154 | 0 / 0 | 0 | 0 | 1,798 / 32 | 1,798 | 22.50 | 1,830 | 298.0 |
| 2026-11-12T21:20 | 0 / 100 | 145 | 136 | 146 | 155 | 157 | 0 / 0 | 0 | 0 | 1,731 / 32 | 1,731 | 23.74 | 1,773 | 267.0 |
| 2026-11-12T21:21 | 0 / 100 | 143 | 131 | 135 | 143 | 152 | 0 / 0 | 0 | 0 | 1,636 / 32 | 1,636 | 23.35 | 1,672 | 265.6 |
| 2026-11-12T21:22 | 0 / 100 | 156 | 144 | 152 | 164 | 167 | 0 / 0 | 0 | 20 | 1,591 / 32 | 1,591 | 22.66 | 1,625 | 257.6 |

Lane N / rate is the cap the runner set for that minute (N lane chains, each with at most one ready transaction in the mempool) and the lane's fee rate. Our heavy in mempool / ready is the probe's median count of our own lane entries; our heavy landed is what the desk counter read as accepted on chain from our lane in the minute; lane submits OK is the lane's own log. Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs (our lane is in our logs) paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R150 hops (150) | R200 hops (200) | R300 hops (300) | R450 hops (450) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T21:11 | 4,368 | 0 | 134 | 128 | 143 | 154 | 157 | 3,596 | 370 | 1 | 575 | 20 | kept pace |
| 2026-11-12T21:12 | 4,252 | 0 | 150 | 131 | 147 | 151 | 150 | 3,523 | 367 | 2 | 790 | 20 | kept pace |
| 2026-11-12T21:13 | 4,398 | 0 | 152 | 138 | 146 | 150 | 152 | 3,660 | 348 | 1 | 515 | 20 | kept pace |
| 2026-11-12T21:14 | 4,367 | 0 | 153 | 140 | 141 | 150 | 152 | 3,631 | 386 | 0 | 469 | 20 | kept pace |
| 2026-11-12T21:15 | 4,274 | 0 | 147 | 134 | 139 | 146 | 145 | 3,563 | 363 | 0 | 308 | 19 | kept pace |
| 2026-11-12T21:16 | 4,220 | 0 | 140 | 130 | 141 | 145 | 147 | 3,517 | 381 | 1 | 518 | 20 | kept pace |
| 2026-11-12T21:17 | 4,394 | 0 | 160 | 163 | 186 | 199 | 206 | 3,480 | 368 | 0 | 424 | 20 | kept pace |
| 2026-11-12T21:18 | 4,210 | 0 | 141 | 122 | 132 | 146 | 144 | 3,525 | 354 | 1 | 532 | 20 | kept pace |
| 2026-11-12T21:19 | 4,264 | 0 | 143 | 131 | 141 | 148 | 154 | 3,547 | 355 | 1 | 584 | 20 | kept pace |
| 2026-11-12T21:20 | 4,248 | 0 | 145 | 136 | 146 | 155 | 157 | 3,510 | 369 | 1 | 330 | 21 | kept pace |
| 2026-11-12T21:21 | 4,215 | 0 | 143 | 131 | 135 | 143 | 152 | 3,511 | 351 | 1 | 532 | 20 | kept pace |
| 2026-11-12T21:22 | 4,315 | 0 | 156 | 144 | 152 | 164 | 167 | 3,533 | 370 | 1 | 397 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R150 (families 5–7, desk private node): 150 sompi/gram per hop. R200 (families 8–10, desk private node): 200 sompi/gram per hop. R300 (families 11–13, desk private node): 300 sompi/gram per hop. R450 (families 14–16, desk private node): 450 sompi/gram per hop. In pre-run 15 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (100) | 100.16 (100–100.32) | 312 | 40,586 (40,377–43,758) | 100–100.32 |
| r150 (150) | 150.16 (150–150.32) | 467 | 40,595 (40,383–43,761) | 150–150.32 |
| r200 (200) | 200.16 (200–200.32) | 623 | 40,615 (40,390–43,758) | 200.01–200.31 |
| r300 (300) | 300.18 (300–300.32) | 935 | 40,660 (40,403–43,758) | 300–300.32 |
| r450 (450) | 450.15 (450–450.32) | 1402 | 40,636 (40,423–43,764) | 450–450.32 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 4 (401), 5 (368), 6 (331), 3 (247), 7 (228), 8 (156), 9 (118), 10 (93), 11 (72), 12 (35), 18 (30), 22 (26), and 70 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | R300 OK / att / rate rej / full rej / waiting | R450 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T21:11 | 0 | 0 | 0 | 0 | 0 | 134 / 341 / 0 / 0 / 4 | 129 / 278 / 0 / 0 / 3 | 143 / 278 / 0 / 0 / 3 | 150 / 280 / 0 / 0 / 1 | 151 / 277 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T21:12 | 0 | 0 | 0 | 0 | 0 | 150 / 345 / 0 / 0 / 4 | 131 / 268 / 0 / 0 / 3 | 147 / 281 / 0 / 0 / 3 | 153 / 279 / 0 / 0 / 3 | 153 / 280 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:13 | 0 | 0 | 0 | 0 | 0 | 152 / 352 / 0 / 0 / 4 | 138 / 276 / 0 / 0 / 3 | 146 / 271 / 0 / 0 / 3 | 150 / 272 / 0 / 0 / 3 | 152 / 271 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:14 | 0 | 0 | 0 | 0 | 0 | 153 / 350 / 0 / 0 / 4 | 140 / 277 / 0 / 0 / 3 | 141 / 269 / 0 / 0 / 3 | 150 / 281 / 0 / 0 / 3 | 152 / 284 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:15 | 0 | 0 | 0 | 0 | 0 | 147 / 349 / 0 / 0 / 4 | 134 / 272 / 0 / 0 / 3 | 139 / 270 / 0 / 0 / 3 | 146 / 283 / 0 / 0 / 3 | 145 / 278 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:16 | 0 | 0 | 0 | 0 | 0 | 140 / 345 / 0 / 0 / 4 | 130 / 265 / 0 / 0 / 3 | 141 / 272 / 0 / 0 / 3 | 145 / 276 / 0 / 0 / 3 | 147 / 280 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:17 | 0 | 0 | 0 | 0 | 0 | 161 / 352 / 0 / 0 / 4 | 163 / 273 / 0 / 0 / 3 | 186 / 272 / 0 / 0 / 3 | 199 / 276 / 0 / 0 / 3 | 206 / 279 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:18 | 0 | 0 | 0 | 0 | 0 | 140 / 347 / 0 / 0 / 4 | 122 / 260 / 0 / 0 / 3 | 132 / 270 / 0 / 0 / 3 | 146 / 280 / 0 / 0 / 3 | 144 / 276 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:19 | 0 | 0 | 0 | 0 | 0 | 141 / 344 / 0 / 0 / 3 | 131 / 269 / 0 / 0 / 3 | 141 / 279 / 0 / 0 / 3 | 148 / 284 / 0 / 0 / 3 | 154 / 295 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:20 | 0 | 0 | 0 | 0 | 0 | 147 / 353 / 0 / 0 / 5 | 136 / 273 / 0 / 0 / 3 | 146 / 277 / 0 / 0 / 3 | 155 / 289 / 0 / 0 / 3 | 157 / 286 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:21 | 0 | 0 | 0 | 0 | 0 | 143 / 345 / 0 / 0 / 5 | 131 / 273 / 0 / 0 / 3 | 135 / 271 / 0 / 0 / 3 | 143 / 275 / 0 / 0 / 3 | 152 / 280 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:22 | 0 | 0 | 0 | 0 | 0 | 155 / 347 / 0 / 0 / 4 | 143 / 271 / 0 / 0 / 2 | 150 / 278 / 0 / 0 / 1 | 164 / 283 / 0 / 0 / 3 | 167 / 289 / 0 / 0 / 3 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 15 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621823887 | 0 | 0 | 0 | 38 |
| 5 | yes | 621823887 | 0 | 0 | 0 | 37 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 1762 of 1763 | 1379 | 2466 |
| r150 | 1628 of 1628 | 1141 | 1822 |
| r200 | 1747 of 1747 | 1072 | 1614 |
| r300 | 1849 of 1849 | 1007 | 1500 |
| r450 | 1880 of 1880 | 981 | 1467 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | R300 in mempool / ready | R450 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: r150 | Template: r200 | Template: r300 | Template: r450 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T21:11 | 2 | 3,234 | 85 | 24.82 | 3,220 | 69 | 3,183 | 266,641 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 470,106 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 3 | 2 | 293.6 / 171.1 / 113.3 | 3,247 | 3,250 |
| 2026-11-12T21:12 | 3 | 3,186 | 73 | 23.03 | 3,187 | 61 | 3,157 | 266,641 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 471,288 | 1 | 0 | 0 | 0 | 0 | 1 | 0 | 2 | 1 | 265.8 / 166.6 / 112.8 | 3,185 | 3,179 |
| 2026-11-12T21:13 | 3 | 3,165 | 71 | 23.29 | 3,149 | 59 | 3,127 | 266,641 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 469,293 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 1 | 280.7 / 169.1 / 113.1 | 3,159 | 3,159 |
| 2026-11-12T21:14 | 3 | 3,161 | 78 | 23.09 | 3,150 | 62 | 3,087 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 9 | 473,306 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 4 | 298.6 / 171.9 / 113.4 | 3,131 | 3,131 |
| 2026-11-12T21:15 | 3 | 2,924 | 70 | 22.09 | 2,908 | 55 | 2,885 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 473,047 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 3 | 1 | 281.7 / 169.3 / 113.1 | 2,909 | 2,900 |
| 2026-11-12T21:16 | 3 | 2,677 | 82 | 22.84 | 2,665 | 66 | 2,631 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 9 | 473,304 | 0 | 0 | 0 | 0 | 0 | 2 | 1 | 3 | 0 | 300.1 / 172.1 / 113.4 | 2,654 | 2,662 |
| 2026-11-12T21:17 | 3 | 2,396 | 75 | 23.28 | 2,387 | 59 | 2,334 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 473,145 | 1 | 0 | 0 | 0 | 0 | 0 | 2 | 0 | 1 | 287.1 / 170.2 / 113.2 | 2,389 | 2,389 |
| 2026-11-12T21:18 | 3 | 2,082 | 78 | 22.91 | 2,070 | 62 | 2,032 | 266,640 | 0 | 0 / 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 471,004 | 1 | 0 | 0 | 0 | 0 | 0 | 2 | 3 | 2 | 281.5 / 169.3 / 113.1 | 2,055 | 2,063 |
| 2026-11-12T21:19 | 3 | 1,830 | 83 | 22.50 | 1,815 | 67 | 1,798 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 470,056 | 1 | 0 | 0 | 0 | 0 | 1 | 2 | 3 | 2 | 298.0 / 171.8 / 113.4 | 1,832 | 1,832 |
| 2026-11-12T21:20 | 3 | 1,773 | 93 | 23.74 | 1,757 | 77 | 1,731 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 390,964 | 1 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 2 | 267.0 / 166.8 / 112.9 | 1,756 | 1,763 |
| 2026-11-12T21:21 | 3 | 1,672 | 68 | 23.35 | 1,656 | 52 | 1,636 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 11 | 455,461 | 0 | 0 | 0 | 0 | 2 | 2 | 3 | 3 | 0 | 265.6 / 166.5 / 112.8 | 1,687 | 1,685 |
| 2026-11-12T21:22 | 3 | 1,625 | 66 | 22.66 | 1,609 | 50 | 1,591 | 266,640 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 1 / 1 | 8 | 472,674 | 1 | 0 | 0 | 0 | 0 | 0 | 2 | 0 | 2 | 257.6 / 165.0 / 112.7 | 1,615 | 1,640 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
