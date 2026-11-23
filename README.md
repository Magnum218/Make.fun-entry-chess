# Make.fun-entry-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Magnum218/Make.fun-entry-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Magnum218/Make.fun-entry-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python, built by Muse for the make.fun tiny-chess-01 bounty. Negamax search with alpha-beta pruning and principal variation search, quiescence search, a transposition table with mate-score adjustment, check extensions and tapered piece-square evaluation, packed with lzma into one self-contained main.py (4,089 bytes). It plays the bounty gauntlet over the environment HTTP API with a fixed 80,000-node budget per move — never the clock — so every game is deterministic and replays move for move.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=chocolatos-eth&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
