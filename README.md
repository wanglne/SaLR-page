# SaLR · NeurIPS 2026

Project page for **Safety-Aware Latent Space Reasoning in Large Language Models**.

[Paper](https://wanglne.github.io/papers/SaLR_NIPS2026.pdf) · [Code](https://github.com/wanglne/SaLR) · [OpenReview](https://openreview.net/forum?id=v5ExASonPK)

## Development

Use Node.js 22.12+ (or Node.js 24) and npm.

```sh
npm ci
npm run dev
```

```sh
npm run build
npm run preview
```

The GitHub Actions workflow deploys to GitHub Pages when pushed to `main`. Enable **GitHub Actions** as the Pages source in repository settings. The workflow sets the site's origin and base path automatically.

## Content

- `src/paper.mdx`: page text, authors, links, and citation.
- `src/data/results.json`: results transcribed from Tables 2, 3, and 6 of the paper's LaTeX source, including reported standard deviations.
- `src/components/Results.astro`: interactive model and evaluation selectors.
- `src/components/AttackResults.astro`: selected results from Tables 4, 5, and 7.
- `src/components/PaperFigure.astro`: guided figure explanations with animated zoom, manual steps, playback controls, and a static fallback.
- `public/figures/`: SVG exports of the supplied overview and method PDFs. Text is outlined; original embedded images are preserved.
- `src/styles/salr.css`: SaLR-specific presentation on top of the template.

The headline token comparison uses the 1B OOD averages (293.3 / 7.5 ≈ 39×); it is not a latency claim. The overview figure is reproduced from the paper, with its original plotting conventions. Detailed web tables use the paper's reported values without recomputing standard deviations.

The page follows Impact → Abstract → Overview → Methodology → Results → Citation. Figure explanations use the original SVG assets; playback starts only when requested, respects reduced-motion preferences, and pauses when the figure leaves view.

## Acknowledgment

The visual layout follows [PolyPose](https://polypose.csail.mit.edu/), with a common content width and matching header typography. Interactive tables remain specific to SaLR.

Built with [Roman Hauksson-Neill's Academic Project Page Template](https://research-template.roman.technology/), using Astro, MDX, and Tailwind CSS. Noto Sans is bundled locally under the [SIL Open Font License](public/fonts/OFL.txt).
