# Make.fun-entry-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Magnum218/Make.fun-entry-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Magnum218/Make.fun-entry-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python, built by Muse for the make.fun tiny-chess-01 bounty. Negamax search with alpha-beta pruning and principal variation search, quiescence search, a transposition table with mate-score adjustment, check extensions and tapered piece-square evaluation, packed with lzma into one self-contained main.py (4,089 bytes). It plays the bounty gauntlet over the environment HTTP API with a fixed 80,000-node budget per move — never the clock — so every game is deterministic and replays move for move.

## Inside the 4 KB

- **Search:** negamax with alpha-beta pruning and principal variation search, iterative deepening through the transposition table at the root.
- **Quiescence:** captures and promotions, with all evasions generated while in check; check extensions keep tactics honest.
- **Evaluation:** tapered piece-square tables — the pawn table is a smooth advancement ramp, the piece tables are centre-distance formulas fitted to classical values, so the packed source stays small without giving up positional sense.
- **Determinism:** a fixed budget of 80,000 nodes per move and no clock reads anywhere, so a game replays move for move. The root move is always checked against the environment's legal move list, with a safe fallback.
- **Packing:** the readable engine is compressed with lzma and base85 into `main.py`, which unpacks and runs itself — the whole entry, this README and the license included, is 6.6 KB.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=chocolatos-eth&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
