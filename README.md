# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Ngntier/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Ngntier/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,096 bytes of Python. It plays the make.fun gauntlet
through the trial environment: alpha-beta search with iterative deepening
under a fixed 100,000-node budget per move (deterministic — no clock),
quiescence over captures and promotions plus full evasions in check,
null-move pruning, a transposition table, killer-move ordering, repetition
detection from the game history, and a material + piece-square-table
evaluation with a tapered king table.
`main.py` is a tiny unpacker around an lzma-compressed payload (allowed
by the rules; payload and unpacker together stay under the cap).

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 -P -s main.py
```

Point `MAKEFUN_ENV_URL` at a running trial env (the kit's
`program/env/server.mjs` serves one locally). The engine plays every game
in the trial, one after another, and exits when they are all over.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
