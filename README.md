# tiny-chess-rumi

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/septiadini1996-sudo/tiny-chess-rumi/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/septiadini1996-sudo/tiny-chess-rumi/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,091 bytes of Python (packed with the official kit compressor). It plays a fixed ~95k-node iterative-deepening negamax search with alpha-beta pruning, a persistent transposition table with honest bound flags, zobrist hashing with snapshot undo, null-move pruning, late-move reductions, PVS, check extensions, and a quiescence search with stand-pat plus a full in-check evasion search. Evaluation combines procedurally expanded piece-square tables, a phase-blended king table, cached passed-pawn structure scoring, and knight mobility, with history-heuristic move ordering.

Local practice trial 0 (the kit's replica of the server grade): 1,364 Elo — 3 wins, 1 draw, 2 losses against the house gauntlet.

## Round 2: the compact-first rebuild

The round-2 engine was rewritten from scratch around a compact-first design, so every byte of the 4 KB budget goes to search strength rather than scaffolding. Its transposition table is honest — entries are stored only with bound flags that match what the search actually proved — and the pruning stack combines null-move pruning, late-move reductions, and principal-variation search, with check extensions on forcing moves. Quiescence is no longer a separate routine: it is merged into the main search and answers checks with full in-check evasions instead of a stand-pat shortcut. A phase-blended king table rounds out the evaluation, valuing king shelter in the middlegame and king activity in the endgame, and the rebuild scored 1,364 on the local trial.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8931 MAKEFUN_PROMPT_FILE=prompt.txt python3 main.py
```

The engine connects to a make.fun tiny-chess environment server, fetches the current game, and posts its moves until the trial is done.

---

<sub>Entered on [make.fun](https://make.fun/?ref=5c10w57m&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
