OBSERVATION

Not scored. No payment of ours in pre-run 15: families only, on the desk's private node, plus our own heavy lane at the N shown per minute.

# BASE, desk, pre-run 15

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

BASE in pre-run 15 is lane N=0 (control): N0-control 12 whole minutes. Families only for payments (no payment of ours); our own heavy lane ran at the N and rate shown per minute (N = how many lane chains may each hold one ready transaction in the mempool). The HOLD file names are kept so the bot's and Mini's gates read as in earlier pre-runs. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r150 (families 5–7) 150 sompi/gram on the desk's private node, r200 (families 8–10) 200 sompi/gram on the desk's private node, r300 (families 11–13) 300 sompi/gram on the desk's private node, r450 (families 14–16) 450 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | Lane N / rate | floor (100) | r150 (150) | r200 (200) | r300 (300) | r450 (450) | Our heavy in mempool / ready | Our heavy landed | Lane submits OK | Outside heavy at 100 (>200k mass) / ready | Outside at 100, n | Ready mass, blocks | Mempool | Fee estimate priority |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T20:47 | 0 / 100 | 187 | 151 | 156 | 157 | 156 | 0 / 0 | 0 | 0 | 4 / 4 | 4 | 1.98 | 18 | 199.5 |
| 2026-11-12T20:48 | 0 / 100 | 193 | 144 | 147 | 148 | 143 | 0 / 0 | 0 | 0 | 2 / 2 | 2 | 1.31 | 13 | 231.2 |
| 2026-11-12T20:49 | 0 / 100 | 176 | 139 | 140 | 142 | 149 | 0 / 0 | 0 | 0 | 9 / 9 | 9 | 6.10 | 23 | 257.3 |
| 2026-11-12T20:50 | 0 / 100 | 187 | 135 | 142 | 152 | 150 | 0 / 0 | 0 | 0 | 7 / 7 | 7 | 5.11 | 24 | 242.6 |
| 2026-11-12T20:51 | 0 / 100 | 186 | 146 | 150 | 152 | 147 | 0 / 0 | 0 | 0 | 8 / 8 | 8 | 3.02 | 14 | 232.7 |
| 2026-11-12T20:52 | 0 / 100 | 174 | 141 | 145 | 148 | 147 | 0 / 0 | 0 | 0 | 18 / 16 | 18 | 10.51 | 39 | 195.2 |
| 2026-11-12T20:53 | 0 / 100 | 168 | 137 | 141 | 148 | 151 | 0 / 0 | 0 | 0 | 17 / 16 | 17 | 11.28 | 38 | 255.9 |
| 2026-11-12T20:54 | 0 / 100 | 164 | 132 | 134 | 142 | 142 | 0 / 0 | 0 | 0 | 15 / 13 | 15 | 9.75 | 34 | 233.4 |
| 2026-11-12T20:55 | 0 / 100 | 163 | 141 | 140 | 146 | 150 | 0 / 0 | 0 | 0 | 35 / 19 | 35 | 13.41 | 48 | 329.5 |
| 2026-11-12T20:56 | 0 / 100 | 162 | 136 | 141 | 145 | 151 | 0 / 0 | 0 | 0 | 21 / 18 | 21 | 13.82 | 46 | 265.8 |
| 2026-11-12T20:57 | 0 / 100 | 184 | 140 | 147 | 153 | 156 | 0 / 0 | 0 | 0 | 15 / 13 | 15 | 10.09 | 27 | 270.7 |
| 2026-11-12T20:58 | 0 / 100 | 178 | 146 | 151 | 156 | 158 | 0 / 0 | 0 | 20 | 17 / 13 | 17 | 10.57 | 39 | 247.2 |

Lane N / rate is the cap the runner set for that minute (N lane chains, each with at most one ready transaction in the mempool) and the lane's fee rate. Our heavy in mempool / ready is the probe's median count of our own lane entries; our heavy landed is what the desk counter read as accepted on chain from our lane in the minute; lane submits OK is the lane's own log. Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs (our lane is in our logs) paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R150 hops (150) | R200 hops (200) | R300 hops (300) | R450 hops (450) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T20:47 | 4,140 | 0 | 187 | 151 | 156 | 157 | 156 | 3,352 | 402 | 0 | 589 | 20 | kept pace |
| 2026-11-12T20:48 | 4,176 | 0 | 193 | 144 | 147 | 148 | 143 | 3,410 | 372 | 1 | 638 | 19 | kept pace |
| 2026-11-12T20:49 | 4,197 | 0 | 176 | 139 | 140 | 142 | 149 | 3,463 | 371 | 1 | 421 | 20 | kept pace |
| 2026-11-12T20:50 | 4,348 | 0 | 187 | 135 | 142 | 152 | 150 | 3,589 | 360 | 1 | 532 | 20 | kept pace |
| 2026-11-12T20:51 | 4,205 | 0 | 186 | 146 | 150 | 152 | 147 | 3,434 | 366 | 2 | 546 | 20 | kept pace |
| 2026-11-12T20:52 | 4,303 | 0 | 174 | 141 | 145 | 148 | 147 | 3,552 | 359 | 1 | 591 | 20 | kept pace |
| 2026-11-12T20:53 | 4,245 | 0 | 168 | 137 | 141 | 148 | 151 | 3,500 | 373 | 1 | 615 | 21 | kept pace |
| 2026-11-12T20:54 | 4,171 | 0 | 164 | 132 | 134 | 142 | 142 | 3,460 | 354 | 2 | 498 | 20 | kept pace |
| 2026-11-12T20:55 | 4,286 | 0 | 163 | 141 | 140 | 146 | 150 | 3,548 | 364 | 0 | 646 | 20 | kept pace |
| 2026-11-12T20:56 | 4,253 | 0 | 162 | 136 | 141 | 145 | 151 | 3,520 | 373 | 1 | 389 | 20 | kept pace |
| 2026-11-12T20:57 | 4,336 | 0 | 184 | 140 | 147 | 153 | 156 | 3,559 | 385 | 0 | 533 | 19 | kept pace |
| 2026-11-12T20:58 | 4,260 | 0 | 178 | 146 | 151 | 156 | 158 | 3,476 | 368 | 1 | 409 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R150 (families 5–7, desk private node): 150 sompi/gram per hop. R200 (families 8–10, desk private node): 200 sompi/gram per hop. R300 (families 11–13, desk private node): 300 sompi/gram per hop. R450 (families 14–16, desk private node): 450 sompi/gram per hop. In pre-run 15 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (100) | 100.16 (100–100.32) | 312 | 40,670 (40,377–43,761) | 100–100.32 |
| r150 (150) | 150.16 (150–150.32) | 468 | 40,622 (40,383–43,763) | 150–150.31 |
| r200 (200) | 200.15 (200–200.32) | 624 | 40,672 (40,390–43,763) | 200–200.32 |
| r300 (300) | 300.17 (300–300.32) | 935 | 40,627 (40,403–43,763) | 300–300.32 |
| r450 (450) | 450.16 (450–450.32) | 1404 | 40,680 (40,423–43,761) | 450.01–450.32 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 6 (457), 10 (428), 8 (423), 9 (423), 5 (418), 7 (412), 4 (383), 11 (344), 12 (241), 3 (192), 13 (183), 14 (75), and 74 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | R300 OK / att / rate rej / full rej / waiting | R450 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T20:47 | 0 | 0 | 0 | 0 | 0 | 189 / 365 / 0 / 0 / 3 | 152 / 281 / 0 / 0 / 1 | 157 / 286 / 0 / 0 / 1 | 157 / 287 / 0 / 0 / 0 | 154 / 285 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T20:48 | 0 | 0 | 0 | 0 | 0 | 194 / 372 / 0 / 0 / 4 | 146 / 274 / 0 / 0 / 3 | 148 / 277 / 0 / 0 / 2 | 151 / 278 / 0 / 0 / 3 | 146 / 278 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:49 | 0 | 0 | 0 | 0 | 0 | 176 / 365 / 0 / 0 / 4 | 138 / 278 / 0 / 0 / 2 | 141 / 279 / 0 / 0 / 3 | 142 / 279 / 0 / 0 / 3 | 149 / 282 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:50 | 0 | 0 | 0 | 0 | 0 | 187 / 370 / 0 / 0 / 4 | 136 / 274 / 0 / 0 / 3 | 142 / 278 / 0 / 0 / 3 | 152 / 287 / 0 / 0 / 3 | 150 / 283 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:51 | 0 | 0 | 0 | 0 | 0 | 187 / 369 / 0 / 0 / 5 | 146 / 281 / 0 / 0 / 3 | 150 / 285 / 0 / 0 / 3 | 152 / 289 / 0 / 0 / 3 | 147 / 275 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:52 | 0 | 0 | 0 | 0 | 0 | 173 / 362 / 0 / 0 / 4 | 141 / 280 / 0 / 0 / 3 | 145 / 280 / 0 / 0 / 3 | 148 / 281 / 0 / 0 / 3 | 147 / 279 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:53 | 0 | 0 | 0 | 0 | 0 | 168 / 354 / 0 / 0 / 4 | 137 / 266 / 0 / 0 / 3 | 141 / 268 / 0 / 0 / 3 | 147 / 278 / 0 / 0 / 2 | 151 / 286 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:54 | 0 | 0 | 0 | 0 | 0 | 164 / 360 / 0 / 0 / 4 | 132 / 272 / 0 / 0 / 3 | 134 / 273 / 0 / 0 / 3 | 143 / 279 / 0 / 0 / 3 | 142 / 275 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:55 | 0 | 0 | 0 | 0 | 0 | 164 / 362 / 0 / 0 / 5 | 141 / 277 / 0 / 0 / 3 | 140 / 277 / 0 / 0 / 3 | 146 / 286 / 0 / 0 / 3 | 150 / 289 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:56 | 0 | 0 | 0 | 0 | 0 | 162 / 354 / 0 / 0 / 5 | 136 / 272 / 0 / 0 / 3 | 140 / 273 / 0 / 0 / 2 | 145 / 275 / 0 / 0 / 3 | 150 / 280 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T20:57 | 0 | 0 | 0 | 0 | 0 | 183 / 364 / 0 / 0 / 4 | 140 / 261 / 0 / 0 / 3 | 148 / 274 / 0 / 0 / 3 | 153 / 275 / 0 / 0 / 3 | 157 / 276 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T20:58 | 0 | 0 | 0 | 0 | 0 | 179 / 368 / 0 / 0 / 4 | 147 / 282 / 0 / 0 / 4 | 151 / 286 / 0 / 0 / 3 | 156 / 283 / 0 / 0 / 3 | 158 / 284 / 0 / 0 / 3 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 15 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621809878 | 0 | 0 | 0 | 39 |
| 5 | yes | 621809878 | 0 | 0 | 0 | 38 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 2126 of 2126 | 1133 | 1798 |
| r150 | 1692 of 1692 | 1097 | 1608 |
| r200 | 1737 of 1737 | 1054 | 1520 |
| r300 | 1792 of 1792 | 1031 | 1487 |
| r450 | 1801 of 1801 | 1020 | 1468 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | R300 in mempool / ready | R450 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: r150 | Template: r200 | Template: r300 | Template: r450 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T20:47 | 3 | 18 | 17 | 1.98 | 4 | 4 | 4 | 266,645 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 1 / 1 | 13 | 492,271 | 0 | 0 | 0 | 3 | 2 | 2 | 3 | 1 | 2 | 199.5 / 150.4 / 110.9 | 4 | 10 |
| 2026-11-12T20:48 | 3 | 13 | 16 | 1.31 | 2 | 2 | 2 | 266,645 | 0 | 0 / 0 | 3 / 3 | 2 / 2 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 491,492 | 0 | 0 | 0 | 1 | 2 | 3 | 3 | 3 | 1 | 231.2 / 159.2 / 112.0 | 2 | 7 |
| 2026-11-12T20:49 | 3 | 23 | 25 | 6.10 | 9 | 9 | 9 | 266,645 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 470,258 | 1 | 0 | 0 | 1 | 0 | 1 | 1 | 3 | 1 | 257.3 / 164.9 / 112.7 | 10 | 24 |
| 2026-11-12T20:50 | 3 | 24 | 24 | 5.11 | 9 | 9 | 7 | 266,645 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 474,252 | 0 | 0 | 0 | 0 | 2 | 3 | 3 | 3 | 1 | 242.6 / 161.9 / 112.3 | 18 | 16 |
| 2026-11-12T20:51 | 3 | 14 | 19 | 3.02 | 4 | 4 | 8 | 266,645 | 0 | 0 / 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 488,020 | 0 | 0 | 0 | 1 | 2 | 3 | 3 | 3 | 0 | 232.7 / 159.6 / 112.1 | 6 | 10 |
| 2026-11-12T20:52 | 3 | 39 | 36 | 10.51 | 24 | 24 | 18 | 266,645 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 1 / 1 | 1 / 1 | 2 / 2 | 7 | 470,502 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 2 | 2 | 195.2 / 149.0 / 110.7 | 27 | 28 |
| 2026-11-12T20:53 | 3 | 38 | 38 | 11.28 | 22 | 22 | 17 | 266,645 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 14 | 489,116 | 0 | 0 | 0 | 1 | 2 | 3 | 3 | 3 | 2 | 255.9 / 164.7 / 112.6 | 24 | 35 |
| 2026-11-12T20:54 | 3 | 34 | 32 | 9.75 | 21 | 19 | 15 | 266,642 | 0 | 0 / 0 | 3 / 3 | 3 / 3 | 2 / 2 | 3 / 3 | 3 / 3 | 6 | 469,682 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 1 | 233.4 / 159.8 / 112.1 | 22 | 34 |
| 2026-11-12T20:55 | 3 | 48 | 83 | 13.41 | 85 | 67 | 35 | 266,642 | 0 | 0 / 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 24 | 457,842 | 0 | 0 | 0 | 1 | 2 | 2 | 3 | 3 | 13 | 329.5 / 175.8 / 113.7 | 42 | 60 |
| 2026-11-12T20:56 | 3 | 46 | 48 | 13.82 | 36 | 33 | 21 | 266,642 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 11 | 492,258 | 0 | 0 | 0 | 0 | 2 | 1 | 3 | 3 | 1 | 265.8 / 166.6 / 112.8 | 39 | 55 |
| 2026-11-12T20:57 | 3 | 27 | 33 | 10.09 | 21 | 19 | 15 | 266,642 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 470,111 | 0 | 0 | 0 | 1 | 1 | 1 | 3 | 3 | 1 | 270.7 / 167.4 / 112.9 | 21 | 29 |
| 2026-11-12T20:58 | 3 | 39 | 42 | 10.57 | 36 | 32 | 17 | 266,642 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 11 | 472,067 | 1 | 0 | 0 | 1 | 0 | 2 | 2 | 3 | 3 | 247.2 / 162.9 / 112.4 | 34 | 33 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
