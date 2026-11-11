# SkyVLN — OMEGA Lab project page

Project page for **SkyVLN: Vision-and-Language Navigation and NMPC Control for UAVs in
Urban Environments** (IROS 2025), in the OMEGA Lab style.

- Paper: <https://arxiv.org/abs/2507.06564> (arXiv), <https://doi.org/10.1109/IROS60139.2025.11247609> (IEEE Xplore)
- Page: <https://omega-hkustgz.github.io/projects/skyvln/> (live once the lab site lists it)

## Working on the page

The page is `index.html` plus `assets/`; there is no build step. Rules for agents are in
[`AGENTS.md`](AGENTS.md).

```sh
node tools/check.mjs     # what CI runs
node tools/serve.mjs     # look at it locally
```

Every pull request gets a preview link, posted on the pull request. A push to `main` asks the
lab site to republish.

## Sources

Everything on the page comes from public material. Keep this list current.

| On the page | Source |
| --- | --- |
| Title, authors, affiliations, text | arXiv 2507.06564v1 (9 Jul 2025). The text paraphrases the abstract and Sections III–V; it adds no claims. |
| Venue, pages, DOI | The arXiv comment ("accepted by IROS 2025"), the lab site's `publications.json` entry for this paper, and the Crossref record for DOI 10.1109/IROS60139.2025.11247609 (IROS 2025, pp. 17199–17206). |
| `task.webp`, `architecture.webp`, `memory-graph.webp`, `spatial-descriptor.webp`, `simulator.webp`, `example-task.webp` | Figs. 1, 2, 3, 4, 5 and 9 of the paper, rendered from the arXiv source PDFs at 2400 px wide (`pdftoppm`, then `cwebp -q 90`; Fig. 5 is portrait and is 2000 px wide). `social.jpg` is Fig. 1 on a 1200 × 630 canvas for link previews. |
| AVDN table, headline numbers, controller and language-model numbers | Tables I and II of the paper, copied from the LaTeX source. Row labels are the paper's. |
| Evidence labels | Figs. 5 and 9 are labelled "Simulation": the paper's simulator is built on AirSim and Unreal Engine 4, and all of its experiments run there. |
| Demo clips | None. |

Not on the page because no public material exists: code, model prompts or weights, demo
video, and any hardware-in-the-loop or real-flight result (the paper reports none). Left to
the paper: the AVDN dataset statistics (Fig. 6), the controller tracking curves (Figs. 7–8)
and the language-model ablation table (Table II, summarised in one sentence).
