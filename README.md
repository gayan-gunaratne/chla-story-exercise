# Take-Home Exercise: Chlorophyll-*a* Story

---

## Dataset

You will find the dataset in the data folder.
It contains a depth-resolved biogeochemical dataset collected from a site in Cockburn Sound, Western Australia, spanning 2009–2024.
Cockburn Sound is a seasonally productive coastal embayment, where chlorophyll-a serves as a key indicator of phytoplankton biomass and overall ecosystem productivity. 
However, its behaviour varies significantly with season, water depth, and ecological conditions, meaning the underlying patterns must be carefully interpreted.

Each sampling trip profiles multiple depths (0, 10, 20, 30, 40 m and bottom) as well as a **water column (WC)** integrated sample. Key variables relevant to this exercise:

| Column | Description | Units |
|---|---|---|
| `SampleDate_Local` | Sampling date | DD/MM/YYYY |
| `SampleDepth_m` | Depth of sample (0–bottom or `WC`) | m |
| `CphlA_mgm3` | Chlorophyll-*a* concentration | mg m⁻³ |

> **Note on units:** Chl-a in this dataset is in mg m⁻³. We typically report Chl-a in mg/L.
---

## Your Task

You are acting as a consultant supporting a client working in Cockburn Sound.

Assume the client is undertaking a hypothetical activity (e.g. port development, aquaculture, discharge, or similar). Based on your understanding of that activity, provide advice on potential environmental impacts informed by the available baseline data.

**Your task is to explore and communicate the Chl-*a* story to the client.**

### Suggested Approach

1. **Clean & prepare** the dataset
   - Separate depth-profile samples from WC (water column) integrated samples, these are different measurement types and should be treated differently

2. **Visualise** - produce at least one clear figure (subplots welcome). Suggested directions:
   - Surface (0 m) Chl-*a* time series with seasonal context
   - Depth-profile and/or concentration-percentile plots

3. **Summarise** - a few bullet points describing:
   - The dominant seasonal patterns you observe
   - Any long-term trends or inter-annual variability
   - Gaps, anomalies, or caveats in the data

---

## What to Deliver

Please email your work **one day before the 2nd round interview** as:

- **Script** - a Jupyter notebook (`.ipynb`), R Markdown (`.Rmd`), or MATLAB script (`.m`)
- **Tech Note** - 1-page document (Word, PDF, HTML, or Markdown) including your key findings and plot(s)

---

## Estimated Time

⏱ **45–60 minutes**

---

## Assessment Criteria

We are looking for:

- **Data handling** - mixed sample types
- **Visualisation** - clear, well-labelled figures that tell a story without clutter
- **Scientific interpretation** - does the narrative reflect an understanding of coastal marine ecology?
- **Communication** - concise written summary accessible to a non-specialist audience

You do not need to produce a polished report. Clarity of thinking and code quality matter more than completeness.

---

## About

This exercise is part of the environmental modelling candidate assessment at BMT. It tests your ability to work with observational water quality datasets, exercise scientific judgement in data cleaning, and communicate environmental insights clearly.
