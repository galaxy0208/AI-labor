# Immigration, AI Exposure & Labor Vulnerability

> How immigration policy shapes who bears the cost of AI-driven occupational displacement — a cross-national analysis of the United States and South Korea.

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![GitHub Pages](https://img.shields.io/badge/demo-live-brightgreen)](https://galaxy0208.github.io/AI-labor/)

---

## Overview

This project presents an interactive, data-driven research website that explores the intersection of **agentic AI labor displacement** and **immigration policy**. It extends a broader analysis of AI's impact on U.S. labor markets by asking a structural question:

> *Does a country's immigration openness determine how AI exposure translates into real labor market harm?*

The site compares two economies with opposing immigration profiles — the **United States** (19.1% foreign-born workforce) and **South Korea** (~3.9%) — to show that the same AI exposure score produces fundamentally different outcomes depending on a nation's demographic flexibility.

## Key Findings

| # | Finding |
|---|---------|
| 1 | High-immigration economies (U.S., Canada) distribute AI exposure risk across a more mobile, international workforce — partially buffering domestic employment shocks. |
| 2 | The H-1B visa system creates a paradox: immigrant labor fills AI-exposed roles at potentially lower cost, compressing wages — yet immigrant founders and engineers also *build* the AI systems driving displacement. |
| 3 | South Korea faces compounding structural risk: high AI exposure in clerical roles, no immigration buffer, and accelerating demographic decline — a uniquely vulnerable profile among advanced economies. |

## Visualizations

The site includes **7 interactive Chart.js visualizations** rendered client-side:

| ID | Chart | Type | What it shows |
|----|-------|------|---------------|
| **Chart A** | Immigrant Concentration vs. AI Exposure by Industry | Grouped Bar | Dual vulnerability — sectors with high AI exposure also carry above-average immigrant workforce shares |
| **Fig. 1** | 5-Year Employment Trend Forecast | Line | Employment index (2025–2030) by AI exposure group; high-exposure jobs grow fastest (augmentation > displacement) |
| **Fig. 2** | Occupational Risk Matrix | Bubble | AI exposure × job growth × workforce size; reveals augmentation vs. displacement quadrants |
| **Chart B** | Entry-Level Job Postings Decline | Line | Post-ChatGPT collapse in new-hire rates for young workers (22–25) in high-exposure occupations |
| **Chart C** | H-1B Approvals vs. Tech Layoffs | Bar | Major firms simultaneously hiring H-1B workers and announcing domestic layoffs |
| **Chart D** | U.S. vs. South Korea Comparison | Table | Side-by-side structural comparison across 7 policy dimensions |
| **Chart E** | Immigration Openness vs. AI Vulnerability | Bubble | Cross-national view — countries with higher immigrant shares have greater labor market flexibility |

## Methodology

**AI Exposure Index** — There is no single official statistic published as an "AI exposure index." The values used throughout the site are a **synthesized composite** constructed by rescaling and combining:

- **Task-level exposure estimates** from [Eloundou et al. (2023)](https://arxiv.org/abs/2303.10130) — GPT task mapping
- **O\*NET 28.0** task descriptors
- **BLS** occupational employment weights

The resulting 0–100 index is a *relative, illustrative* measure for cross-occupation and cross-industry comparison — not a directly reported number, and not a probability of job loss.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Structure | Semantic HTML5, single-page |
| Styling | Vanilla CSS with CSS custom properties (design tokens) |
| Charts | [Chart.js 4.4.1](https://www.chartjs.org/) via CDN |
| Typography | `ui-monospace` system font stack |
| Hosting | GitHub Pages (static) |

No build step. No frameworks. No dependencies beyond Chart.js.

## Project Structure

```
AI-labor/
├── index.html          # Full application — markup, styles (embedded), and chart logic
├── README.md
└── .gitignore
```

## Getting Started

```bash
# Clone the repository
git clone https://github.com/galaxy0208/AI-labor.git
cd AI-labor

# Open directly in browser — no build required
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or visit the **[live demo](https://galaxy0208.github.io/AI-labor/)** on GitHub Pages.

## Data Sources

All data points are keyed to numbered references within the site. Primary sources include:

1. **BLS** — [Foreign-Born Workers, 2025](https://www.bls.gov/news.release/forbrn.nr0.htm) · [Employment Projections 2024–2034](https://www.bls.gov/emp/)
2. **USCIS** — [H-1B Characteristics Report, FY2024](https://www.uscis.gov/) · H-1B Employer Data Hub
3. **NFAP** — [Immigrant Founders of America's AI Companies (2023)](https://nfap.com/)
4. **Eloundou et al.** — [GPTs are GPTs (2023)](https://arxiv.org/abs/2303.10130)
5. **O\*NET 28.0** — [Task-level occupation data](https://www.onetcenter.org/database.html)
6. **Anthropic Economic Index** — [Massenkoff & McCrory (2026)](https://www.anthropic.com/economic-index)
7. **OECD** — [International Migration Outlook 2024](https://www.oecd.org/en/publications/international-migration-outlook-2024_50b0353e-en.html)
8. **IMF** — [WP/23/216: Labor Market Exposure to AI](https://www.imf.org/en/Publications/WP/Issues/2023/10/04/Labor-Market-Exposure-to-AI-Cross-country-Differences-and-Distributional-Implications-539656) · Korea Selected Issues (2025)
9. **Statistics Korea (KOSTAT)** — Population estimates, immigrant survey, firm AI adoption
10. **WEF** — [Future of Jobs Report 2025](https://www.weforum.org/publications/the-future-of-jobs-report-2025/)

## Author

**Seung Jun Heo**

## License

This project is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).
