NO SEND check-failed

# HOLD-4, bot sender log, pre-run 15

> Counts only. The bot's sender log. It is not a chain count. The desk counter and Mini count the chain.

Pinned minute (UTC): 2026-11-12T21:51. It is the first whole UTC minute whose start is at least 3 minutes after the desk's HOLD-3 file's On origin time, 2026-11-12T21:47:22Z (commit 8b57217). Fee 150 sompi/gram. Own coins only.

The bot sent nothing in this minute. Submit-OK 0, attempts 0, rejects rate 0, full 0.

## What happened, plainly

- The bot's machine (our box) rebooted at about 21:30Z and its files rolled back to about 21:28Z. The original waiter and finisher were gone. A resume actor relaunched the same waiter and finisher at 21:42:38Z, before HOLD-3 was on origin.
- The waiter first read HOLD-3 on origin at 21:47:25Z (3 s after its On origin time) and pinned 21:51.
- The free-node check started on time at pin−40 s, but it **crashed**: a Node module it loads (a websocket library) was missing after the rollback. It read no node. The waiter recorded an empty free list at **2026-11-12T21:50:21Z** and decided `NO SEND` then, 39 s before the minute. That decision stands as the bot's decision time. No send was attempted.
- The finisher then failed to render this file at 21:52:03Z, because the check's output was an error, not a result. So this file was not on origin at the minute's close.
- This file was written and pushed late, after 21:53Z, by the resume actor. It is not backdated.

Because the check never read a node, this is **not** a legal `no-free-node`. The paste's words for a no-send are `no-free-node`, `suspend`, `coins-short` or `halt`; none of them describes a check that did not run, so we write `check-failed`. Coins were not the reason.

## A read after the minute (not the decision)

After fixing the module path, the same check was run once more, read-only, at 2026-11-12T21:53:39Z, about 99 s after the pinned minute closed, with the desk's kept set (1, 5). It is shown only as context. It cannot stand in for a check before the minute.

| Node (bot label) | In the desk's kept set | Answered | Synced, DAA moving | Same kaspad as a kept node |
|---|---|---|---|---|
| desk 1 | yes | yes | yes | — |
| desk 2 | no | no | — | — |
| desk 3 | no | no | — | — |
| desk 4 | no | yes | yes | yes |
| desk 5 | yes | yes | yes | — |
| extra 1 | no | yes | yes | yes |
| extra 2 | no | yes | yes | yes |
| extra 3 | no | yes | yes | yes |

The kept nodes answered as 2 distinct kaspad processes. Every other node that answered was the same kaspad as a kept node, so this later read found no free node. We observed the same in earlier pre-runs; it suggests, but does not prove, that a check at 21:50:21Z would also have found none.

No txid, key, seed, address, host, port, or covenant id is in this file.
