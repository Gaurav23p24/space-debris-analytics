# Space Debris Visualization Suite

> Transform 65,000+ space objects into a compelling narrative about humanity's expanding footprint in Earth's orbit  
> **Visual Analytics 5122 | Design, Storytelling, and Communication**

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-success)](https://gaurav23p24.github.io/space-debris-analytics/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## The Problem

Space debris—from defunct satellites to collision fragments—grows each year. Traveling at thousands of miles per hour, small pieces can destroy active satellites, endanger missions and astronauts, and risk cascading collisions. With thousands of launches planned, our orbital environment is increasingly polluted.

## Our Goal

Make this silent threat understandable and actionable through clear visuals. This project turns catalog data into an accessible narrative that:
- Summarizes accumulation, distribution, and trends
- Places the stakes in spatial and temporal terms
- Frames evidence for mitigation and policy

---

## Live Demo

**[View Interactive Visualizations](https://gaurav23p24.github.io/space-debris-analytics/)**

Seven interactive charts covering accumulation, spatial distribution, and orbital characteristics.

---

## Visualizations: Why These Seven

Each chart answers a distinct question.

### 1. Growth Timeline
**Why:** Show progression and scale from Sputnik (1957) to today.  
**Insight:** From 2 objects to 30,000+ in under 70 years.  
**Chart:** Stacked area for accumulation and composition.

### 2. Orbit Regime Dominance
**Why:** Different altitudes have different risks, traffic patterns, and lifetimes.  
**Insight:** Ownership and risk concentration across low, medium, and geosynchronous orbits.  
**Chart:** Stacked bars per regime.

### 3. Launches vs Decays
**Why:** Compare inflow to natural decay to assess net growth.  
**Insight:** Launches outpace removals; net accumulation increases collision risk.  
**Chart:** Dual-axis area/line: launches/decays (bars) and cumulative active (line).

### 4. 3D Orbital Distribution
**Why:** Make the spatial dimension intuitive.  
**Insight:** Density and structure vary sharply across orbital shells.  
**Chart:** Interactive 3D scatter by altitude.

### 5. Public vs Private
**Why:** Understand who adds objects and how the landscape is changing.  
**Insight:** Commercial activity is rising rapidly.  
**Chart:** Stacked bars for public/private share by regime.

### 6. Altitude Pyramid
**Why:** Show population structure and altitude-specific decay patterns.  
**Insight:** Active vs. decayed objects across altitudes.  
**Chart:** Back-to-back bars (active vs. decayed) per altitude band.

### 7. Eccentricity Map
**Why:** Capture the diversity of orbital shapes.  
**Insight:** High variation in eccentricity affects collision and decay behavior.  
**Chart:** Scatter of perigee vs. apogee, colored/sized by eccentricity.

Together: problem scale, spatial structure, dynamics, stakeholders, mechanics.

---

## Design Philosophy

**Clutter Reduction** — Aggregated 65,000+ objects into readable groups  
**Color Harmony** — Consistent regime colors  
**Story Arc** — Progression: scale → distribution → urgency  
**Emotional Engagement** — Curiosity to concern  
**Technical Accuracy** — Orbital mechanics validated  
**Accessibility** — WCAG-compliant contrasts

**Key Design Choices**
- Regime colors: LEO (cyan), MEO (green), GEO (amber), HEO (magenta)
- Sector colors: Public (blue), Private (orange)
- Interactive: hover, zoom, filters, dual-axis controls
- Progressive disclosure: summary then detail on demand

---

## Quick Start

### View Visualizations
1. Visit [Live Demo Site](https://gaurav23p24.github.io/space-debris-analytics/)
2. Explore the interactive charts
3. Download the data and reproduce

### Run Locally

```bash
# Clone repository
git clone https://github.com/Gaurav23p24/space-debris-analytics.git
cd space-debris-analytics

# Install dependencies
pip install pandas plotly numpy jupyter

# Open notebook
jupyter notebook "GauravPatel_801426641_VA_Project1_Space_Debris (1).ipynb"
```

### Generate HTML Files
1. Upload notebook to [Google Colab](https://colab.research.google.com/)
2. Upload `satcat.csv`
3. Run all cells
4. Download HTML files from `/content/` folder

---

## Project Structure

```
space-debris-analytics/
├── index.html                                          # Landing page
├── GauravPatel_801426641_VA_Project1_Space_Debris (1).ipynb
├── Project3_DesignReport_GauravPatel.md               # Design rationale
├── content/                                            # Visualizations
│   ├── growth_timeline.html
│   ├── regime_dominance.html
│   ├── launches_decays_timeline.html
│   ├── orbit_3d_visualization_fixed.html
│   ├── public_private_stacked_bar.html
│   ├── orbit_altitude_pyramid.html
│   └── perigee_apogee_eccentricity.html
├── README.md (this file)
├── README_Project3.md                                  # Full documentation
└── LICENSE
```

---

## Documentation

- **[Full Project README](README_Project3.md)** - Complete project details
- **[Design Report](Project3_DesignReport_GauravPatel.md)** - Design rationale & reflection
- **[Quick Start Guide](QUICK_START.md)** - Get started in minutes
- **[GitHub Pages Setup](GITHUB_PAGES_SETUP.md)** - Publishing instructions

---

## Academic Information

**Course:** Visual Analytics 5122  
**Project:** Project 3 - Design, Storytelling, and Communication  
**Path:** Redesign Path (Improving Project 1)

**Student:** Gaurav Bharatkumar Patel  
**ID:** 801426641

---

## Rubric Coverage

- **Design & Execution (30 pts)** — Intentional palette, layout, clutter control
- **Storytelling (25 pts)** — Clear arc, clear audience
- **Rationale (25 pts)** — Evidence-backed decisions
- **Quality (20 pts)** — Functional, accessible, consistent, ready to publish

---

## Technologies

- **Python** — Data processing
- **Pandas** — Manipulation
- **Plotly** — Interactive charts
- **Jupyter** — Development
- **GitHub Pages** — Hosting

---

## Data Source

**Space-Track Catalog** (satcat.csv)
- 65,331 objects
- 1957 to present
- Public debris catalog

---

## License

MIT License — see [LICENSE](LICENSE).

---

## Acknowledgments

- Space-Track for the public catalog
- Plotly tools
- Visual Analytics 5122 course

---

**Making the invisible threat visible through data visualization**

---

### Quick Links
- [Live Site](https://gaurav23p24.github.io/space-debris-analytics/)
- [Full Documentation](README_Project3.md)
- [Design Report](Project3_DesignReport_GauravPatel.md)
- [Quick Start](QUICK_START.md)
