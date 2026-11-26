# Behavioral Foresight Games with Bright-Line Heuristics
### Extending Analogy-Based Limited Foresight to Financial Microstructure

**Author:** Quan Zhong
**Supervisor:** Professor Philippe Jehiel
**Degree:** MSc in Economics, University College London
**Year:** September 2026
**Word count:** 11,430

📄 **[Read the dissertation (PDF)](./QuanZhong_Foresight_MScDissertation_UCL_2026.pdf)**

---

## Abstract

This dissertation studies how boundedly-foresighted agents behave near a bright line. A bright
line is a discrete threshold at which the marginal cost of action jumps. The paper traces the
consequences from a single agent to a population, and then to a market.

The behavioural primitive is a foresight horizon `h`. An agent with horizon `h` optimises over a
rolling window of `h` periods. It forecasts its own future play by the same stationary rule it
will use on arrival, and it places no value beyond the window (Jehiel, 1995; Jehiel and Lilico,
2010).

- **Model 1** shows analytically that limited foresight produces unconditional over-action on the
  approach to the line. The excess action vanishes in the tails, and the myopic process crosses
  the line weakly earlier.
- **Model 2** aggregates two foresight types under coarse analogy-class perception and measures
  the population against a jointly consistent full-foresight equilibrium. The gap between them is
  the *magnet input*, and it is non-negative throughout the parameter sweep.
- **Model 3** places this magnet in a market and adds the paper's main extension: a strategic
  informed trader whose size `αI` and inventory cost `κI` are explicit primitives, and whose
  order enters the flow that moves both price and state.

One mechanism runs through all three layers. An agent's own action moves the state, and that is
what makes foresight valuable. Decomposing the informed trader's profit shows that most of it
comes from trading against predictable retail pressure, so stabilising the crowd and profiting
from it are the same act.

Every number reported in the paper is computed, and every figure is drawn, by code written for
the paper under a single shared calibration (Python, NumPy, SciPy, Matplotlib).

---

## Contents

| Chapter | Title | Page |
| --- | --- | --- |
| 1 | Introduction | 1 |
| 2 | Related literature | 3 |
| 3 | Model 1: single-agent limited-forecast equilibrium | 5 |
| 4 | Model 2: population aggregation | 11 |
| 5 | Model 3: a market with an informed trader | 21 |
| 6 | Discussion and policy | 28 |
| 7 | Conclusion | 31 |
| — | Bibliography | 33 |
| A–G | Appendices: solution methods, threshold symmetry, specification choices, leader and commitment, calibration and algorithms, regularity and existence, proofs | 34–40 |

## Headline results

**Model 1 — over-action is unconditional.** For every state `x`, the myopic rule satisfies
`a(1)(x) ≥ aFF(x)`, with the wedge equal to `−βC′(ρ(x)+aFF(x)) / γ(x) ≥ 0`. The wedge builds
toward the line, peaks **0.116** while the agent is still strictly below the threshold, falls
discontinuously at `s̄` where the cost jumps, and dies away in the tails.

**Foresight converges fast.** One extra period of anticipation closes **58.9%** of the
myopic-to-full-foresight gap; three periods close 82.9%; five periods close 96.7%. An aggregate
magnet therefore needs genuinely myopic participants.

**Model 2 — the magnet is about composition.** At a fixed herd mass the aggregate wedge is
exactly `µ·w1`, vanishing at `µ = 0`. Coarse perception *weakens* the magnet: on the Near class
it falls monotonically as the class half-bandwidth `δ` rises from 0.2 to 0.6. A threshold has to
be locatable to be a target.

**Model 3 — stabilising and profiting coincide.** Trading against predictable retail flow
contributes 70.4% of expected profit in the Far class, 56.6% in Near and 31.8% in Trig for a
small unconstrained informed sector. The systematic footprint is `−0.1336` at `αI = 0.05`,
which is 47.5% of aggregate retail pressure. Leaning removes at most **half** of predictable
flow (`k ≥ 1/2`), so the magnet is damped but never eliminated or reversed.

**The trader barely cares how irrational the crowd is.** The value of knowing the crowd is
boundedly rational is at most ~0.055% of profit — second order by the envelope theorem. The
trader damps the crowd firmly while caring little about exactly how biased it is.

---

## Repository contents

```
.
├── QuanZhong_Foresight_MScDissertation_UCL_2026.pdf   # full dissertation
├── README.md                                          # this file
└── LICENSE
```

## Citing

```bibtex
@mastersthesis{zhong2026foresight,
  author  = {Zhong, Quan},
  title   = {Behavioral Foresight Games with Bright-Line Heuristics:
             Extending Analogy-Based Limited Foresight to Financial Microstructure},
  school  = {University College London},
  type    = {MSc dissertation},
  year    = {2026},
  note    = {Supervisor: Philippe Jehiel}
}
```

## Related work

Earlier undergraduate dissertation, same author:
[ucl-bsc-dissertation-2025](https://github.com/SketchySaturn92-Tyq/ucl-bsc-dissertation-2025) —
*Action Bias* (the mechanism that reappears here as the h = 1 case).

## Licence

Copyright © 2026 Quan Zhong. All rights reserved. See [LICENSE](./LICENSE).
