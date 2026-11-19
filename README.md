# tiny-chess-rumi

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/septiadini1996-sudo/tiny-chess-rumi/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/septiadini1996-sudo/tiny-chess-rumi/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A tiny chess engine in a single Python file: negamax alpha-beta search with quiescence, a transposition table, null-move pruning, PVS with late-move reductions, check extensions, repetition-aware scoring, and a compact evaluation (material, piece-square tables, bishop pair, pawn structure). Deterministic by design: fixed node budget, no clock, no randomness. As the competition rules allow, `main.py` unpacks and execs an lzma-compressed payload; engine and unpacker together are 4,070 bytes.

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=5c10w57m&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
