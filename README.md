# imigraph reports

Generated HTML reports from [imigraph](https://github.com/molntamas/imigraph). Each page is
self-contained (simulation data, plots and animations inline) and opens directly in a browser.
Every run produces a new timestamped file; older pages are kept. Newest first.

| page | content |
| --- | --- |
| [playground_2026-11-01_100328_drift-nostay.html](playground_2026-11-01_100328_drift-nostay.html) | Playground result page (imigraph #2, rule editor): the rule set Drift + NoStay applied in order in every step on a 9x9 world with walkers starting in the left half; rules with pattern drawings, the starting universe, the run step by step, measured drift/diffusion against the prediction, and the session JSON that reproduces it |
| [brownian_vs_graph_2026-11-01_100327_rule-editor.html](brownian_vs_graph_2026-11-01_100327_rule-editor.html) | Brownian motion vs the random-hop rule, with the pattern drawing of the rule in the rules table (rule editor round) |
| [gas_2026-10-31_201241_lattice-gas.html](gas_2026-10-31_201241_lattice-gas.html) | Hard-disk gas next to a lattice gas on the walker graph (HPP rules Collide / Reflect / Stream as edge rewrites): conservation checks of both, collisions, cross-comparison, graph-model questions and answers |
| [brownian_vs_graph_2026-10-31_201245_graph-model-qa.html](brownian_vs_graph_2026-10-31_201245_graph-model-qa.html) | Brownian motion vs the random-hop rule, now with the graph-model Q&A card and the rule's predicted physics |
| [brownian_vs_graph_2026-10-30_200000_responsive.html](brownian_vs_graph_2026-10-30_200000_responsive.html) | Brownian motion in a box vs. the random-hop graph rule on a square lattice: checks, animations, rule explanation, energy/momentum/entropy metrics |
| [gas_2026-10-30_195958_hard-disk-gas.html](gas_2026-10-30_195958_hard-disk-gas.html) | Energy-conserving hard-disk gas (free expansion): conservation checks, Maxwell speed distribution, entropy |

Regenerate with `python -m imigraph report --label <change>`, `python -m imigraph gas-report --label <change>` and
`python -m imigraph playground-report --request-file session.json --label <change>` (see the imigraph README for the
Docker workflow). Playground pages can also be saved from the browser GUI (*Save result page*).
