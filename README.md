# Scientific Paper Forensics

A public, static GitHub Pages library of critical scientific-paper evaluations.

**Website:** https://profdanger.github.io/paper_forensics/

## Published reviews

| Paper | Field | Review date | Page |
| --- | --- | --- | --- |
| Huang et al., *Nature Physics* (2011), DOI [10.1038/nphys1953](https://doi.org/10.1038/nphys1953) | Statistical mechanics / ultrafast optical tracking | 2026-11-04 | [Huang review](https://profdanger.github.io/paper_forensics/papers/huang-2011-brownian-motion/) |\n| Kodera et al., *Nature* (2010), DOI [10.1038/nature09450](https://doi.org/10.1038/nature09450) | Single-molecule biophysics / high-speed AFM | 2026-11-02 | [Kodera review](https://profdanger.github.io/paper_forensics/papers/kodera-2010-myosin-v-afm/) |
| Cherf et al., *Nature Biotechnology* (2012), DOI [10.1038/nbt.2147](https://doi.org/10.1038/nbt.2147) | Nanopore biophysics | 2026-11-02 | [Cherf review](https://profdanger.github.io/paper_forensics/papers/cherf-2012/) |
| Gilpin et al., *Nature Physics* (2017), DOI [10.1038/nphys3981](https://doi.org/10.1038/nphys3981) | Ciliary hydrodynamics | 2026-11-02 | [Gilpin review](https://profdanger.github.io/paper_forensics/papers/gilpin-2017-starfish-larvae/) |
| Gazzola et al., *Nature Physics* (2014), DOI [10.1038/nphys3078](https://doi.org/10.1038/nphys3078) | Aquatic locomotion / fluid mechanics | 2026-11-02 | [Gazzola review](https://profdanger.github.io/paper_forensics/papers/kodera-2010-myosin-v-afm/
  index.html                         # HS-AFM motor-motion forensic dossier
  assets/
    motor-walk.svg                   # original molecular stepping diagram
    evidence-ladder.svg              # original observation/inference diagram
papers/gazzola-2014-aquatic-locomotion/) |

## Structure

```text
index.html                           # central paper library
assets/shared/site.css               # library and modern review design
papers/cherf-2012/index.html         # original standalone Cherf page, preserved verbatim
papers/gilpin-2017-starfish-larvae/
  index.html                         # full retrospective dossier
  assets/
    vortex-schematic.svg             # original conceptual illustration
    boundary-comparison.svg          # original conceptual illustration
papers/gazzola-2014-aquatic-locomotion/
  index.html                         # full aquatic locomotion dossier
  assets/
    force-balance.svg               # original explanatory force-balance model
    scaling-regimes.svg             # original schematic scaling visualization
README.md
```

The original Cherf page was the previous site root. Its bytes are preserved **unchanged** at `papers/cherf-2012/index.html`. On the new library homepage, legacy fragment links (`/#mechanism`, `/#evidence`, `/#nabc`, `/#legacy`, `/#discussion`, `/#scores`) redirect to the Cherf review; the root now intentionally serves the requested central index.

## Adding a review

1. Use a unique lowercase slug under `papers/firstauthor-year-short-title/`.
2. Check existing published DOI entries first and **do not replace a review for the same DOI without permission**.
3. Create the full accessible HTML page, link to `../../assets/shared/site.css`, and put paper-specific media under `assets/`.
4. Add a card to `index.html` with first author/year, journal, field, executive verdict, date and the permanent paper link.
5. Update this README and verify old paper pages and fragment links, new links, mobile layout and GitHub Pages deployment.

## Editorial standards

Each assessment separates source observations, model-derived inferences, critique, independent follow-up, and unresolved tests. Disclose missing supplemental data and inability to reproduce computations. References use DOI links where available. Scores are six independent dimensions and are not averaged.

The six SVG illustrations in the Gilpin, Gazzola and Kodera reviews are **original explanatory illustrations, not reproduced or measured experimental figures**. They should not be cited as evidence. No original journal PDF or publisher figure files are distributed through this repository.

## Hosting

Static HTML/CSS/SVG served by GitHub Pages from the repository's `main` branch. No build system, dependencies, external fonts or JavaScript frameworks are required.