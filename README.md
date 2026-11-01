# imigraph reports

Generated HTML reports from [imigraph](https://github.com/molntamas/imigraph). Each page is
self-contained (simulation data, plots and animations inline) and opens directly in a browser.
Every run produces a new timestamped file; older pages are kept. Newest first.

| page | content |
| --- | --- |
| [rule_editor_2026-11-01_173916_overlaps.html](rule_editor_2026-11-01_173916_overlaps.html) | **Rule editor with overlap strategies** (imigraph #2): the browser GUI as one self-contained file. The new option *overlapping matches* (parallel, ordered, random, oldest) decides which matches of a rule that share a site edge are applied in a step, in the Wolfram sense of a match consuming its left-hand side; waiting hops are counted and the strategies are explained on the page. Includes the collision demo, walker models and collisions. Download and open locally; Pyodide is fetched from the CDN on load |
| [rule_editor_2026-11-01_172408_collision-demo.html](rule_editor_2026-11-01_172408_collision-demo.html) | **Rule editor with the collision demo** (imigraph #2): section 1c runs a fixed 4x4 world where two hyperedge walkers meet head-on; every step has a caption (what Collide, Reflect and Stream did, the total momentum) next to the explanation of the HPP collision, and a button loads the world into the playground. Every hyperedge run shows such captions and its momentum bookkeeping. Download and open locally; Pyodide is fetched from the CDN on load |
| [playground_2026-11-01_172407_lattice-gas-captions.html](playground_2026-11-01_172407_lattice-gas-captions.html) | Playground result page of the HPP lattice gas with the step captions and the momentum bookkeeping |
| [rule_editor_2026-11-01_165959_collisions.html](rule_editor_2026-11-01_165959_collisions.html) | **Rule editor with walker models and collisions** (imigraph #2): the browser GUI as one self-contained file. Rules carry a description; the walker model is *edge* (`{w,s}`, no interaction) or *hyperedge* (`{w,s,s'}`, heading, exclusion principle); collisions *none* or *hpp* (the HPP collision of the lattice gas); built-in Stream and Reflect rules; the page explains the models and collisions. Download and open locally; Pyodide is fetched from the CDN on load |
| [playground_2026-11-01_165803_lattice-gas.html](playground_2026-11-01_165803_lattice-gas.html) | Playground result page of the HPP lattice gas built in the rule editor: hyperedge walkers, hpp collisions, Reflect + Stream on a 9x9 world with 24 walkers from the left half; Collide pattern, arrows and collision rings in the run, blocked hops and collision counts, the walker-model and collision documentation |
| [rule_editor_2026-11-01_162129_rule-editor.html](rule_editor_2026-11-01_162129_rule-editor.html) | **Rule editor** (imigraph #2): the interactive browser GUI as one self-contained file. Download it and open it locally: edit rules in the drawing or as text, build rule sets, set the starting universe (size, walls, where the walkers start), run with the chosen speed, see measured vs predicted drift/diffusion, save a result page. Python runs in the browser through Pyodide, which is downloaded from the jsDelivr CDN on load (about 15 MB, once) |
| [playground_2026-11-01_100328_drift-nostay.html](playground_2026-11-01_100328_drift-nostay.html) | Playground result page (imigraph #2, rule editor): the rule set Drift + NoStay applied in order in every step on a 9x9 world with walkers starting in the left half; rules with pattern drawings, the starting universe, the run step by step, measured drift/diffusion against the prediction, and the session JSON that reproduces it |
| [brownian_vs_graph_2026-11-01_100327_rule-editor.html](brownian_vs_graph_2026-11-01_100327_rule-editor.html) | Brownian motion vs the random-hop rule, with the pattern drawing of the rule in the rules table (rule editor round) |
| [gas_2026-10-31_201241_lattice-gas.html](gas_2026-10-31_201241_lattice-gas.html) | Hard-disk gas next to a lattice gas on the walker graph (HPP rules Collide / Reflect / Stream as edge rewrites): conservation checks of both, collisions, cross-comparison, graph-model questions and answers |
| [brownian_vs_graph_2026-10-31_201245_graph-model-qa.html](brownian_vs_graph_2026-10-31_201245_graph-model-qa.html) | Brownian motion vs the random-hop rule, now with the graph-model Q&A card and the rule's predicted physics |
| [brownian_vs_graph_2026-10-30_200000_responsive.html](brownian_vs_graph_2026-10-30_200000_responsive.html) | Brownian motion in a box vs. the random-hop graph rule on a square lattice: checks, animations, rule explanation, energy/momentum/entropy metrics |
| [gas_2026-10-30_195958_hard-disk-gas.html](gas_2026-10-30_195958_hard-disk-gas.html) | Energy-conserving hard-disk gas (free expansion): conservation checks, Maxwell speed distribution, entropy |

Regenerate with `python -m imigraph report --label <change>`, `python -m imigraph gas-report --label <change>`,
`python -m imigraph playground-report --request-file session.json --label <change>` and `python -m imigraph gui-page
--label <change>` for the rule editor (see the imigraph README for the Docker workflow). Playground pages can also be
saved from the browser GUI (*Save result page*).

GitHub shows HTML files as source. To use a page, download it (the *Download raw file* button of the file view) and
open the downloaded file in a browser.
