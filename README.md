# tiny-chess-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/koejanvok-oss/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/koejanvok-oss/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A tiny chess engine that fits in under 4 KB. It searches with alpha-beta, a transposition table and quiescence search, evaluates positions with PeSTO piece-square tables, and plays a full game against the make.fun environment server over HTTP.

## How it plays

The engine thinks on a fixed budget of 150,000 nodes per move, deepening iteratively until the budget runs out. Moves are ordered by the transposition-table move first, then by MVV-LVA captures, so the search spends its time on the lines that matter most.

## Run it

```sh
python3 main.py
```

Built for the tiny-chess-01 bounty on [make.fun](https://make.fun/bounty/tiny-chess-01).
