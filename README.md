# imigraph reports

Generated HTML reports from [imigraph](https://github.com/molntamas/imigraph). Each page is
self-contained (simulation data, plots and animations inline) and opens directly in a browser.
Every run produces a new timestamped file; older pages are kept.

| page | content |
| --- | --- |
| [brownian_vs_graph_2026-10-30_200000_responsive.html](brownian_vs_graph_2026-10-30_200000_responsive.html) | Brownian motion in a box vs. the random-hop graph rule on a square lattice: checks, animations, rule explanation, energy/momentum/entropy metrics |
| [gas_2026-10-30_195958_hard-disk-gas.html](gas_2026-10-30_195958_hard-disk-gas.html) | Energy-conserving hard-disk gas (free expansion): conservation checks, Maxwell speed distribution, entropy |

Regenerate with `python -m imigraph report --label <change>` and `python -m imigraph gas-report --label <change>`
(see the imigraph README for the Docker workflow).
