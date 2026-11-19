# tiny-chess-rumi

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/septiadini1996-sudo/tiny-chess-rumi/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/septiadini1996-sudo/tiny-chess-rumi/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python: negamax alpha-beta search with quiescence, a transposition table, killer moves and a history heuristic for move ordering, MVV-LVA capture scoring, check extensions, null-move pruning and late-move reductions, all packed into a single self-unpacking `main.py` of 4,052 bytes. It plays deterministically on a fixed node budget — no clock, no randomness — so every game is reproducible.

## Run it

```sh
python3 main.py
# the engine speaks the competition harness protocol on stdin/stdout (see the bounty RULES)
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=5c10w57m&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
