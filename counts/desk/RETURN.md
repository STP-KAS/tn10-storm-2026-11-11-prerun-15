OBSERVATION

Not scored. No payment of ours in pre-run 15: families only, on the desk's private node, plus our own heavy lane at the N shown per minute.

# RETURN, desk, pre-run 15

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

RETURN is families only with our heavy lane at N=0 (the drain), 12 whole minutes, the last stretch before the families stop. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r150 (families 5–7) 150 sompi/gram on the desk's private node, r200 (families 8–10) 200 sompi/gram on the desk's private node, r300 (families 11–13) 300 sompi/gram on the desk's private node, r450 (families 14–16) 450 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | Lane N / rate | floor (100) | r150 (150) | r200 (200) | r300 (300) | r450 (450) | Our heavy in mempool / ready | Our heavy landed | Lane submits OK | Outside heavy at 100 (>200k mass) / ready | Outside at 100, n | Ready mass, blocks | Mempool | Fee estimate priority |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T21:53 | 0 / 100 | 141 | 129 | 141 | 144 | 148 | 0 / 0 | 0 | 0 | 8,164 / 32 | 8,164 | 23.92 | 8,189 | 260.5 |
| 2026-11-12T21:54 | 0 / 100 | 137 | 126 | 135 | 138 | 146 | 0 / 0 | 0 | 0 | 8,039 / 32 | 8,039 | 24.74 | 8,082 | 289.4 |
| 2026-11-12T21:55 | 0 / 100 | 142 | 128 | 129 | 140 | 138 | 0 / 0 | 0 | 0 | 7,898 / 32 | 7,898 | 24.07 | 7,959 | 235.5 |
| 2026-11-12T21:56 | 0 / 100 | 132 | 127 | 137 | 148 | 145 | 0 / 0 | 0 | 0 | 7,886 / 32 | 7,886 | 24.06 | 7,913 | 258.0 |
| 2026-11-12T21:57 | 0 / 100 | 135 | 123 | 133 | 146 | 142 | 0 / 0 | 0 | 0 | 7,863 / 32 | 7,863 | 25.52 | 7,922 | 294.3 |
| 2026-11-12T21:58 | 0 / 100 | 126 | 118 | 129 | 128 | 129 | 0 / 0 | 0 | 0 | 7,867 / 32 | 7,867 | 25.71 | 7,912 | 281.5 |
| 2026-11-12T21:59 | 0 / 100 | 140 | 122 | 132 | 141 | 147 | 0 / 0 | 0 | 0 | 7,782 / 32 | 7,782 | 24.33 | 7,807 | 335.4 |
| 2026-11-12T22:00 | 0 / 100 | 143 | 132 | 138 | 150 | 151 | 0 / 0 | 0 | 0 | 7,599 / 32 | 7,599 | 23.47 | 7,641 | 273.3 |
| 2026-11-12T22:01 | 0 / 100 | 144 | 124 | 133 | 142 | 148 | 0 / 0 | 0 | 0 | 7,415 / 32 | 7,415 | 24.42 | 7,443 | 269.0 |
| 2026-11-12T22:02 | 0 / 100 | 130 | 116 | 131 | 141 | 152 | 0 / 0 | 0 | 0 | 7,230 / 32 | 7,230 | 24.00 | 7,259 | 296.0 |
| 2026-11-12T22:03 | 0 / 100 | 132 | 122 | 129 | 138 | 142 | 0 / 0 | 0 | 0 | 7,220 / 32 | 7,220 | 25.49 | 7,273 | 297.5 |
| 2026-11-12T22:04 | 0 / 100 | 144 | 133 | 143 | 147 | 145 | 0 / 0 | 0 | 0 | 7,239 / 32 | 7,239 | 24.94 | 7,268 | 171.1 |

Lane N / rate is the cap the runner set for that minute (N lane chains, each with at most one ready transaction in the mempool) and the lane's fee rate. Our heavy in mempool / ready is the probe's median count of our own lane entries; our heavy landed is what the desk counter read as accepted on chain from our lane in the minute; lane submits OK is the lane's own log. Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs (our lane is in our logs) paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R150 hops (150) | R200 hops (200) | R300 hops (300) | R450 hops (450) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T21:53 | 4,308 | 0 | 141 | 129 | 141 | 144 | 148 | 3,605 | 352 | 2 | 441 | 20 | kept pace |
| 2026-11-12T21:54 | 4,240 | 0 | 137 | 126 | 135 | 138 | 146 | 3,558 | 364 | 1 | 415 | 20 | kept pace |
| 2026-11-12T21:55 | 4,219 | 0 | 142 | 128 | 129 | 140 | 138 | 3,542 | 358 | 0 | 398 | 21 | kept pace |
| 2026-11-12T21:56 | 4,274 | 0 | 132 | 127 | 137 | 148 | 145 | 3,585 | 353 | 1 | 458 | 19 | kept pace |
| 2026-11-12T21:57 | 4,145 | 0 | 135 | 123 | 133 | 146 | 142 | 3,466 | 313 | 1 | 388 | 20 | kept pace |
| 2026-11-12T21:58 | 4,125 | 0 | 126 | 118 | 129 | 128 | 129 | 3,495 | 294 | 0 | 469 | 20 | kept pace |
| 2026-11-12T21:59 | 4,182 | 0 | 140 | 122 | 132 | 141 | 147 | 3,500 | 294 | 1 | 282 | 20 | kept pace |
| 2026-11-12T22:00 | 4,422 | 0 | 143 | 132 | 138 | 150 | 151 | 3,708 | 316 | 0 | 652 | 20 | kept pace |
| 2026-11-12T22:01 | 4,231 | 0 | 144 | 124 | 133 | 142 | 148 | 3,540 | 323 | 1 | 646 | 20 | kept pace |
| 2026-11-12T22:02 | 4,124 | 0 | 130 | 116 | 131 | 141 | 152 | 3,454 | 306 | 1 | 848 | 20 | kept pace |
| 2026-11-12T22:03 | 4,163 | 0 | 132 | 122 | 129 | 138 | 142 | 3,500 | 306 | 0 | 576 | 20 | kept pace |
| 2026-11-12T22:04 | 4,228 | 0 | 144 | 133 | 143 | 147 | 145 | 3,517 | 358 | 1 | 578 | 19 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R150 (families 5–7, desk private node): 150 sompi/gram per hop. R200 (families 8–10, desk private node): 200 sompi/gram per hop. R300 (families 11–13, desk private node): 300 sompi/gram per hop. R450 (families 14–16, desk private node): 450 sompi/gram per hop. In pre-run 15 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (100) | 100.09 (100–100.3) | 335 | 43,702 (40,423–43,740) | 100–100.3 |
| r150 (150) | 150.15 (150–150.3) | 503 | 43,702 (40,673–43,740) | 150–150.28 |
| r200 (200) | 200.17 (200–200.3) | 670 | 43,703 (40,852–43,739) | 200.01–200.29 |
| r300 (300) | 300.16 (300–300.3) | 1005 | 43,703 (40,406–43,740) | 300.01–300.29 |
| r450 (450) | 450.14 (450.01–450.3) | 1508 | 43,700 (40,729–43,737) | 450.01–450.29 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 239 (14), 248 (12), 251 (12), 249 (11), 234 (11), 237 (11), 243 (11), 233 (10), 255 (10), 245 (10), 253 (9), 242 (9), and 59 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | R300 OK / att / rate rej / full rej / waiting | R450 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T21:53 | 0 | 0 | 0 | 0 | 0 | 141 / 352 / 0 / 0 / 5 | 129 / 272 / 0 / 0 / 3 | 141 / 283 / 0 / 0 / 3 | 144 / 286 / 0 / 0 / 3 | 148 / 287 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:54 | 0 | 0 | 0 | 0 | 0 | 137 / 341 / 0 / 0 / 5 | 126 / 264 / 0 / 0 / 3 | 135 / 275 / 0 / 0 / 3 | 136 / 276 / 0 / 0 / 1 | 143 / 283 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T21:55 | 0 | 0 | 0 | 0 | 0 | 142 / 351 / 0 / 0 / 5 | 128 / 264 / 0 / 0 / 3 | 129 / 270 / 0 / 0 / 3 | 142 / 280 / 0 / 0 / 3 | 141 / 277 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:56 | 0 | 0 | 0 | 0 | 0 | 131 / 346 / 0 / 0 / 4 | 127 / 269 / 0 / 0 / 3 | 137 / 274 / 0 / 0 / 3 | 148 / 277 / 0 / 0 / 3 | 145 / 272 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:57 | 0 | 0 | 0 | 0 | 0 | 135 / 334 / 0 / 0 / 4 | 123 / 261 / 0 / 0 / 3 | 133 / 271 / 0 / 0 / 3 | 146 / 280 / 0 / 0 / 3 | 142 / 273 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:58 | 0 | 0 | 0 | 0 | 0 | 127 / 334 / 0 / 0 / 5 | 118 / 259 / 0 / 0 / 3 | 129 / 260 / 0 / 0 / 3 | 128 / 266 / 0 / 0 / 3 | 129 / 264 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T21:59 | 0 | 0 | 0 | 0 | 0 | 140 / 340 / 0 / 0 / 5 | 122 / 260 / 0 / 0 / 3 | 132 / 263 / 0 / 0 / 3 | 141 / 268 / 0 / 0 / 3 | 147 / 279 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T22:00 | 0 | 0 | 0 | 0 | 0 | 143 / 343 / 0 / 0 / 5 | 132 / 274 / 0 / 0 / 3 | 138 / 275 / 0 / 0 / 3 | 150 / 276 / 0 / 0 / 3 | 151 / 278 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T22:01 | 0 | 0 | 0 | 0 | 0 | 143 / 345 / 0 / 0 / 4 | 123 / 264 / 0 / 0 / 2 | 133 / 271 / 0 / 0 / 3 | 142 / 275 / 0 / 0 / 3 | 147 / 279 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T22:02 | 0 | 0 | 0 | 0 | 0 | 131 / 344 / 0 / 0 / 5 | 117 / 265 / 0 / 0 / 3 | 131 / 268 / 0 / 0 / 3 | 141 / 280 / 0 / 0 / 3 | 151 / 290 / 0 / 0 / 1 | 0 | 0 | yes |
| 2026-11-12T22:03 | 0 | 0 | 0 | 0 | 0 | 132 / 338 / 0 / 0 / 5 | 121 / 266 / 0 / 0 / 2 | 127 / 268 / 0 / 0 / 1 | 137 / 275 / 0 / 0 / 2 | 144 / 276 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T22:04 | 0 | 0 | 0 | 0 | 0 | 144 / 346 / 0 / 0 / 5 | 134 / 271 / 0 / 0 / 3 | 144 / 275 / 0 / 0 / 3 | 146 / 287 / 0 / 0 / 3 | 145 / 286 / 0 / 0 / 3 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 15 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621848391 | 0 | 0 | 0 | 38 |
| 5 | yes | 621848391 | 0 | 0 | 0 | 35 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 1646 of 1646 | 1448 | 2677 |
| r150 | 1500 of 1500 | 1218 | 1899 |
| r200 | 1609 of 1609 | 1122 | 1691 |
| r300 | 1701 of 1701 | 1073 | 1595 |
| r450 | 1733 of 1733 | 1039 | 1516 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | R300 in mempool / ready | R450 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: r150 | Template: r200 | Template: r300 | Template: r450 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T21:53 | 3 | 8,189 | 65 | 23.92 | 8,186 | 54 | 8,164 | 266,632 | 0 | 0 / 0 | 4 / 4 | 2 / 2 | 2 / 2 | 3 / 3 | 3 / 3 | 7 | 485,161 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 260.5 / 165.6 / 112.7 | 8,181 | 8,188 |
| 2026-11-12T21:54 | 3 | 8,082 | 81 | 24.74 | 8,066 | 66 | 8,039 | 266,631 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 9 | 485,226 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 289.4 / 170.5 / 113.2 | 8,092 | 8,103 |
| 2026-11-12T21:55 | 3 | 7,959 | 79 | 24.07 | 7,951 | 65 | 7,898 | 266,631 | 0 | 0 / 0 | 3 / 3 | 3 / 3 | 3 / 3 | 2 / 2 | 0 / 0 | 11 | 437,467 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 235.5 / 160.3 / 112.2 | 7,954 | 7,954 |
| 2026-11-12T21:56 | 3 | 7,913 | 67 | 24.06 | 7,914 | 52 | 7,886 | 266,630 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 2 / 2 | 6 | 485,211 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 258.0 / 165.1 / 112.7 | 7,931 | 7,923 |
| 2026-11-12T21:57 | 3 | 7,922 | 83 | 25.52 | 7,910 | 71 | 7,863 | 266,630 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 13 | 480,820 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 294.3 / 171.2 / 113.3 | 7,907 | 7,915 |
| 2026-11-12T21:58 | 3 | 7,912 | 77 | 25.71 | 7,896 | 61 | 7,867 | 266,630 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 9 | 485,099 | 1 | 0 | 0 | 1 | 1 | 1 | 0 | 0 | 2 | 281.5 / 169.3 / 113.1 | 7,911 | 7,912 |
| 2026-11-12T21:59 | 2 | 7,807 | 124 | 24.33 | 7,858 | 108 | 7,782 | 266,629 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 12 | 485,167 | 1 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 1 | 335.4 / 176.4 / 113.8 | 7,833 | 7,833 |
| 2026-11-12T22:00 | 3 | 7,641 | 71 | 23.47 | 7,631 | 61 | 7,599 | 266,629 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 480,652 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 273.3 / 167.9 / 113.0 | 7,622 | 7,622 |
| 2026-11-12T22:01 | 3 | 7,443 | 63 | 24.42 | 7,433 | 49 | 7,415 | 266,628 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 8 | 485,103 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 269.0 / 167.1 / 112.9 | 7,455 | 7,456 |
| 2026-11-12T22:02 | 3 | 7,259 | 82 | 24.00 | 7,264 | 66 | 7,230 | 266,628 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 8 | 485,074 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 296.0 / 171.5 / 113.3 | 7,298 | 7,298 |
| 2026-11-12T22:03 | 3 | 7,273 | 85 | 25.49 | 7,257 | 69 | 7,220 | 266,628 | 0 | 0 / 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 485,064 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 297.5 / 171.7 / 113.3 | 7,278 | 7,266 |
| 2026-11-12T22:04 | 3 | 7,268 | 61 | 24.94 | 7,266 | 59 | 7,239 | 266,627 | 0 | 0 / 0 | 3 / 3 | 1 / 1 | 1 / 1 | 0 / 0 | 0 / 0 | 8 | 485,029 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 171.1 / 140.1 / 109.4 | 7,280 | 7,282 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
