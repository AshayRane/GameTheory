# GameTheory — Prisoner's Dilemma Tournament

An interactive recreation of the **Axelrod tournament** from Veritasium's
*"What Game Theory Reveals About Life, The Universe, and Everything"*.

Open `index.html` in any browser — no build step, no dependencies.

## The game

Two players secretly choose **Cooperate (C)** or **Defect (D)** each round:

| Outcome          | Payoff            |
|------------------|-------------------|
| C · C            | 3 pts each        |
| D · C            | 5 / 0             |
| C · D            | 0 / 5             |
| D · D            | 1 pt each         |

## Tournament rules

- Every strategy plays every other strategy **and a copy of itself** (15 matchups).
- Round count per match is randomized (default 180–220) so nobody knows when the game ends.
- Highest **total** points wins — it's not head-to-head.

## The strategies

| Strategy         | Type  | Behavior |
|------------------|-------|----------|
| Tit for Tat      | Nice  | Cooperate first, then copy the opponent's last move |
| Tit for Two Tats | Nice  | Defects only after two defections in a row |
| Friedman         | Nice  | Never defects first, but one defection → defects forever |
| Joss             | Nasty | Mostly copies, sneaks in a defection ~10% of the time |
| Always Defect    | Nasty | Defects every round |

## Controls

- **Speed** slider — pace of the animated round-by-round play
- **Run Tournament** — animated playthrough of all 15 matchups
- **Skip to result** — compute all matchups instantly

Expected result: nice strategies dominate, Always Defect finishes last.
