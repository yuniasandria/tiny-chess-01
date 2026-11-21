[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/yuniasandria/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/yuniasandria/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# Tiny Chess — strongest chess engine in 4 KB of Python

A 0x88-board chess engine in Python 3.13 stdlib only, packed into
`main.py` (4,074 bytes). Built for the [make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01).

## Run it

```sh
python3 main.py
```

## Search
- Principal variation search (PVS) with quiescence search
- Null-move pruning and late move reductions (LMR)
- Transposition table with iterative deepening
- Move ordering: MVV-LVA captures plus history heuristic
- Fixed budget of 50,000 nodes per move

## Evaluation
- PeSTO tapered evaluation (middlegame / endgame tables)
- Tables stored delta-encoded in base-85 to fit the size cap

## Entry
- `main.py` — the entry, 4,074 bytes (cap 4,096)
- `engine_golf.py` — readable golfed source
- `engine_src.py` — full readable source

## Verification
- Trial 0 (kit scorer): 5 won, 1 drawn, 0 lost — Elo 1809
- Spare plies 518; no timeouts, no illegal moves
- Beats the Sunfish baseline (Elo 1364) by 445 Elo
- Perft on 6 standard positions: all OK
- Determinism: repeated runs byte-identical

---

<sub>Entered on [make.fun](https://make.fun/?ref=6cmdpsm5&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
