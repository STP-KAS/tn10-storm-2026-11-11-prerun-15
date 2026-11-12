OBSERVATION

Not scored. No payment of ours in pre-run 15: families only, on the desk's private node, plus our own heavy lane at the N shown per minute.

# HOLD-1, desk, pre-run 15

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-1 in pre-run 15 is lane N=60 at 126 (ready-mass hold 80 blocks): N60-r126 12 whole minutes. Families only for payments (no payment of ours); our own heavy lane ran at the N and rate shown per minute (N = how many lane chains may each hold one ready transaction in the mempool). The HOLD file names are kept so the bot's and Mini's gates read as in earlier pre-runs. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r150 (families 5–7) 150 sompi/gram on the desk's private node, r200 (families 8–10) 200 sompi/gram on the desk's private node, r300 (families 11–13) 300 sompi/gram on the desk's private node, r450 (families 14–16) 450 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | Lane N / rate | floor (100) | r150 (150) | r200 (200) | r300 (300) | r450 (450) | Our heavy in mempool / ready | Our heavy landed | Lane submits OK | Outside heavy at 100 (>200k mass) / ready | Outside at 100, n | Ready mass, blocks | Mempool | Fee estimate priority |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T20:59 | 60 / 126 | 89 | 103 | 134 | 157 | 162 | 58 / 58 | 397 | 433 | 212 / 32 | 212 | 50.94 | 372 | 385.5 |
| 2026-11-12T21:00 | 60 / 126 | 87 | 106 | 129 | 144 | 148 | 58 / 58 | 411 | 414 | 596 / 32 | 596 | 52.14 | 752 | 381.3 |
| 2026-11-12T21:01 | 60 / 126 | 87 | 119 | 145 | 174 | 186 | 54 / 54 | 423 | 420 | 947 / 32 | 947 | 51.38 | 1,084 | 389.5 |
| 2026-11-12T21:02 | 60 / 126 | 83 | 106 | 124 | 141 | 148 | 57 / 57 | 431 | 424 | 1,199 / 32 | 1,199 | 53.64 | 1,316 | 372.5 |
| 2026-11-12T21:03 | 60 / 126 | 86 | 105 | 124 | 135 | 146 | 56 / 56 | 410 | 421 | 1,411 / 32 | 1,411 | 52.90 | 1,520 | 342.3 |
| 2026-11-12T21:04 | 60 / 126 | 84 | 105 | 130 | 145 | 149 | 56 / 56 | 445 | 441 | 1,675 / 32 | 1,675 | 52.23 | 1,805 | 383.0 |
| 2026-11-12T21:05 | 60 / 126 | 88 | 103 | 125 | 144 | 152 | 57 / 57 | 418 | 417 | 1,917 / 32 | 1,917 | 52.83 | 2,074 | 387.4 |
| 2026-11-12T21:06 | 60 / 126 | 87 | 108 | 149 | 162 | 172 | 57 / 57 | 425 | 427 | 2,156 / 32 | 2,156 | 54.42 | 2,298 | 387.5 |
| 2026-11-12T21:07 | 60 / 126 | 82 | 107 | 134 | 157 | 163 | 55 / 55 | 402 | 401 | 2,407 / 32 | 2,407 | 54.15 | 2,548 | 379.5 |
| 2026-11-12T21:08 | 60 / 126 | 82 | 112 | 139 | 154 | 163 | 55 / 55 | 452 | 455 | 2,627 / 32 | 2,627 | 52.89 | 2,756 | 395.2 |
| 2026-11-12T21:09 | 60 / 126 | 92 | 117 | 134 | 148 | 156 | 60 / 60 | 443 | 441 | 2,870 / 32 | 2,870 | 56.18 | 2,965 | 353.5 |
| 2026-11-12T21:10 | 60 / 126 | 78 | 100 | 124 | 139 | 149 | 57 / 57 | 423 | 422 | 3,108 / 32 | 3,108 | 55.11 | 3,217 | 389.1 |

Lane N / rate is the cap the runner set for that minute (N lane chains, each with at most one ready transaction in the mempool) and the lane's fee rate. Our heavy in mempool / ready is the probe's median count of our own lane entries; our heavy landed is what the desk counter read as accepted on chain from our lane in the minute; lane submits OK is the lane's own log. Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs (our lane is in our logs) paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R150 hops (150) | R200 hops (200) | R300 hops (300) | R450 hops (450) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T20:59 | 4,133 | 0 | 89 | 103 | 134 | 157 | 162 | 3,094 | 345 | 0 | 467 | 19 | kept pace |
| 2026-11-12T21:00 | 4,218 | 0 | 87 | 106 | 129 | 144 | 148 | 3,193 | 363 | 1 | 613 | 20 | kept pace |
| 2026-11-12T21:01 | 4,295 | 0 | 87 | 119 | 145 | 174 | 186 | 3,162 | 369 | 1 | 381 | 20 | kept pace |
| 2026-11-12T21:02 | 4,387 | 0 | 83 | 106 | 124 | 141 | 148 | 3,354 | 374 | 0 | 453 | 20 | kept pace |
| 2026-11-12T21:03 | 4,141 | 0 | 86 | 105 | 124 | 135 | 146 | 3,138 | 354 | 1 | 679 | 20 | kept pace |
| 2026-11-12T21:04 | 4,150 | 0 | 84 | 105 | 130 | 145 | 149 | 3,092 | 369 | 1 | 706 | 19 | kept pace |
| 2026-11-12T21:05 | 4,169 | 0 | 88 | 103 | 125 | 144 | 152 | 3,139 | 359 | 0 | 606 | 20 | kept pace |
| 2026-11-12T21:06 | 4,246 | 0 | 87 | 108 | 149 | 162 | 172 | 3,143 | 366 | 2 | 547 | 20 | kept pace |
| 2026-11-12T21:07 | 4,152 | 0 | 82 | 107 | 134 | 157 | 163 | 3,107 | 377 | 1 | 498 | 19 | kept pace |
| 2026-11-12T21:08 | 4,305 | 0 | 82 | 112 | 139 | 154 | 163 | 3,204 | 419 | 2 | 389 | 20 | kept pace |
| 2026-11-12T21:09 | 4,195 | 0 | 92 | 117 | 134 | 148 | 156 | 3,105 | 381 | 1 | 700 | 20 | kept pace |
| 2026-11-12T21:10 | 4,106 | 0 | 78 | 100 | 124 | 139 | 149 | 3,093 | 360 | 1 | 490 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R150 (families 5–7, desk private node): 150 sompi/gram per hop. R200 (families 8–10, desk private node): 200 sompi/gram per hop. R300 (families 11–13, desk private node): 300 sompi/gram per hop. R450 (families 14–16, desk private node): 450 sompi/gram per hop. In pre-run 15 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (100) | 100.16 (100–100.32) | 312 | 40,579 (40,377–43,763) | 100–100.31 |
| r150 (150) | 150.17 (150–150.32) | 467 | 40,580 (40,383–43,763) | 150–150.31 |
| r200 (200) | 200.16 (200–200.32) | 623 | 40,585 (40,390–43,763) | 200.02–200.32 |
| r300 (300) | 300.18 (300–300.32) | 935 | 40,627 (40,403–43,763) | 300–300.31 |
| r450 (450) | 450.15 (450–450.32) | 1402 | 40,641 (40,422–43,761) | 450–450.32 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 5 (459), 4 (459), 6 (419), 7 (402), 8 (340), 9 (301), 3 (265), 10 (261), 11 (179), 12 (130), 13 (70), 14 (49), and 72 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | R300 OK / att / rate rej / full rej / waiting | R450 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T20:59 | 0 | 0 | 0 | 0 | 0 | 88 / 322 / 0 / 0 / 4 | 102 / 259 / 0 / 0 / 3 | 134 / 270 / 0 / 0 / 3 | 157 / 287 / 0 / 0 / 3 | 162 / 290 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:00 | 0 | 0 | 0 | 0 | 0 | 86 / 320 / 0 / 0 / 3 | 106 / 261 / 0 / 0 / 3 | 127 / 260 / 0 / 0 / 1 | 142 / 277 / 0 / 0 / 1 | 145 / 282 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T21:01 | 0 | 0 | 0 | 0 | 0 | 87 / 322 / 0 / 0 / 3 | 117 / 266 / 0 / 0 / 1 | 144 / 265 / 0 / 0 / 0 | 174 / 281 / 0 / 0 / 1 | 187 / 289 / 0 / 0 / 1 | 0 | 0 | yes |
| 2026-11-12T21:02 | 0 | 0 | 0 | 0 | 0 | 83 / 320 / 0 / 0 / 3 | 108 / 263 / 0 / 0 / 3 | 127 / 269 / 0 / 0 / 3 | 143 / 288 / 0 / 0 / 3 | 150 / 295 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:03 | 0 | 0 | 0 | 0 | 0 | 86 / 323 / 0 / 0 / 3 | 105 / 258 / 0 / 0 / 3 | 123 / 267 / 0 / 0 / 2 | 135 / 267 / 0 / 0 / 3 | 146 / 278 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:04 | 0 | 0 | 0 | 0 | 0 | 85 / 322 / 0 / 0 / 4 | 105 / 260 / 0 / 0 / 3 | 131 / 273 / 0 / 0 / 3 | 145 / 284 / 0 / 0 / 3 | 149 / 282 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:05 | 0 | 0 | 0 | 0 | 0 | 88 / 329 / 0 / 0 / 4 | 103 / 256 / 0 / 0 / 3 | 125 / 267 / 0 / 0 / 3 | 144 / 284 / 0 / 0 / 3 | 152 / 285 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:06 | 0 | 0 | 0 | 0 | 0 | 87 / 320 / 0 / 0 / 4 | 107 / 257 / 0 / 0 / 2 | 149 / 286 / 0 / 0 / 3 | 162 / 279 / 0 / 0 / 3 | 172 / 281 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:07 | 0 | 0 | 0 | 0 | 0 | 82 / 322 / 0 / 0 / 4 | 108 / 261 / 0 / 0 / 3 | 134 / 266 / 0 / 0 / 3 | 157 / 277 / 0 / 0 / 3 | 163 / 282 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:08 | 0 | 0 | 0 | 0 | 0 | 82 / 323 / 0 / 0 / 4 | 112 / 266 / 0 / 0 / 3 | 139 / 273 / 0 / 0 / 3 | 154 / 283 / 0 / 0 / 3 | 163 / 287 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:09 | 0 | 0 | 0 | 0 | 0 | 92 / 328 / 0 / 0 / 4 | 117 / 261 / 0 / 0 / 3 | 134 / 273 / 0 / 0 / 3 | 148 / 282 / 0 / 0 / 3 | 156 / 282 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:10 | 0 | 0 | 0 | 0 | 0 | 78 / 318 / 0 / 0 / 4 | 99 / 255 / 0 / 0 / 2 | 124 / 270 / 0 / 0 / 3 | 141 / 272 / 0 / 0 / 3 | 152 / 287 / 0 / 0 / 3 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 15 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621816821 | 0 | 0 | 0 | 39 |
| 5 | yes | 621816821 | 0 | 0 | 0 | 38 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 1024 of 1024 | 2179 | 5894 |
| r150 | 1289 of 1289 | 1397 | 2749 |
| r200 | 1591 of 1591 | 1157 | 1917 |
| r300 | 1802 of 1802 | 1018 | 1518 |
| r450 | 1897 of 1897 | 959 | 1444 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | R300 in mempool / ready | R450 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: r150 | Template: r200 | Template: r300 | Template: r450 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T20:59 | 3 | 372 | 149 | 50.94 | 301 | 88 | 212 | 266,642 | 0 | 58 / 58 | 4 / 4 | 2 / 2 | 2 / 2 | 3 / 3 | 3 / 3 | 8 | 470,429 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 3 | 2 | 385.5 / 181.0 / 114.2 | 366 | 372 |
| 2026-11-12T21:00 | 3 | 752 | 143 | 52.14 | 690 | 69 | 596 | 266,642 | 0 | 58 / 58 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 471,343 | 1 | 0 | 1 | 0 | 0 | 0 | 2 | 3 | 1 | 381.3 / 180.7 / 114.2 | 753 | 748 |
| 2026-11-12T21:01 | 3 | 1,084 | 183 | 51.38 | 1,017 | 114 | 947 | 266,642 | 0 | 54 / 54 | 4 / 4 | 3 / 3 | 3 / 3 | 2 / 2 | 3 / 3 | 8 | 470,951 | 1 | 0 | 0 | 0 | 0 | 0 | 2 | 3 | 2 | 389.5 / 181.3 / 114.2 | 1,077 | 1,087 |
| 2026-11-12T21:02 | 3 | 1,316 | 211 | 53.64 | 1,271 | 138 | 1,199 | 266,642 | 0 | 57 / 57 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 470,020 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 2 | 6 | 372.5 / 180.0 / 114.1 | 1,316 | 1,329 |
| 2026-11-12T21:03 | 3 | 1,520 | 174 | 52.90 | 1,452 | 107 | 1,411 | 266,642 | 0 | 56 / 56 | 4 / 4 | 3 / 3 | 2 / 2 | 2 / 2 | 1 / 1 | 9 | 469,957 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 3 | 342.3 / 177.2 / 113.9 | 1,542 | 1,556 |
| 2026-11-12T21:04 | 3 | 1,805 | 170 | 52.23 | 1,733 | 104 | 1,675 | 266,642 | 0 | 56 / 56 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 8 | 470,131 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 2 | 2 | 383.0 / 180.8 / 114.2 | 1,834 | 1,834 |
| 2026-11-12T21:05 | 3 | 2,074 | 172 | 52.83 | 2,003 | 100 | 1,917 | 266,642 | 0 | 57 / 57 | 4 / 4 | 3 / 3 | 3 / 3 | 2 / 2 | 3 / 3 | 9 | 470,859 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 0 | 3 | 387.4 / 181.2 / 114.2 | 2,087 | 2,094 |
| 2026-11-12T21:06 | 3 | 2,298 | 174 | 54.42 | 2,224 | 100 | 2,156 | 266,642 | 0 | 57 / 57 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 469,366 | 1 | 0 | 1 | 0 | 1 | 1 | 0 | 2 | 2 | 387.5 / 181.2 / 114.2 | 2,320 | 2,320 |
| 2026-11-12T21:07 | 3 | 2,548 | 173 | 54.15 | 2,477 | 102 | 2,407 | 266,642 | 0 | 55 / 55 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 8 | 470,610 | 1 | 0 | 1 | 0 | 0 | 0 | 2 | 3 | 0 | 379.5 / 180.6 / 114.2 | 2,586 | 2,586 |
| 2026-11-12T21:08 | 3 | 2,756 | 194 | 52.89 | 2,700 | 123 | 2,627 | 266,642 | 0 | 55 / 55 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 474,360 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 2 | 1 | 395.2 / 181.8 / 114.3 | 2,739 | 2,738 |
| 2026-11-12T21:09 | 3 | 2,965 | 151 | 56.18 | 2,907 | 76 | 2,870 | 266,642 | 0 | 60 / 60 | 4 / 4 | 3 / 3 | 3 / 3 | 2 / 2 | 3 / 3 | 6 | 471,948 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 3 | 4 | 353.5 / 178.3 / 114.0 | 2,953 | 2,953 |
| 2026-11-12T21:10 | 3 | 3,217 | 189 | 55.11 | 3,199 | 115 | 3,108 | 266,641 | 0 | 57 / 57 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 11 | 469,706 | 1 | 0 | 0 | 0 | 0 | 2 | 1 | 3 | 3 | 389.1 / 181.3 / 114.2 | 3,259 | 3,252 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
