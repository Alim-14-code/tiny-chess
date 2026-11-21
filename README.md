# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Alim-14-code/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Alim-14-code/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact chess engine in a single Python file (`main.py`, 4,085 bytes,
stdlib only). 0x88 board, negamax + PVS, transposition table, MVV-LVA and
killer move ordering, quiescence search (captures, promotions, check
evasions), check extensions, null-move pruning, and iterative deepening to
a fixed node budget (100,000 nodes/move) — no clock, no randomness, so
every game replays deterministically.

`main.py` is the kit-compressed form of the readable source, produced by
`node cli/makefun.mjs compress`. The engine speaks the make.fun env
protocol: it reads `$MAKEFUN_ENV_URL` and plays UCI moves over
`POST /game`, `POST /move`, `POST /resign`.

Practice trials (6 games each vs the house rungs) measured on the kit's
local env: see the trial states in the build notes. The readable source
is 22 KB; the compressed entrypoint fits the 4,096-byte cap.

## Run it

```sh
python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=e6d1qmmj&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

License: MIT (`LICENSE`).
