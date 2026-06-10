# Take-Home Exercise: Chlorophyll-*a* Story

---

## Dataset

You will find the dataset inside the **`data`** folder.

It contains a **depth-resolved biogeochemical dataset** from the IMOS National Reference Station (NRS) at **Rottnest Island, Western Australia**, spanning **2009–2024**.

Each sampling trip profiles multiple depths (0, 10, 20, 30, 40 m and bottom) as well as a **water column (WC)** integrated sample. Key variables relevant to this exercise:

| Column | Description | Units |
|---|---|---|
| `SampleDate_Local` | Sampling date | DD/MM/YYYY |
| `SampleDepth_m` | Depth of sample (0–bottom or `WC`) | m |
| `CphlA_mgm3` | Chlorophyll-*a* concentration | mg m⁻³ |
| `DvCphlA_mgm3` | Divinyl Chlorophyll-*a* (prokaryote proxy) | mg m⁻³ |
| `DvCphlA_CphlA_mgm3` | Total Chl-*a* (monovinyl + divinyl) | mg m⁻³ |
| `Fuco_mgm3` | Fucoxanthin (diatom/dinoflagellate pigment) | mg m⁻³ |
| `Perid_mgm3` | Peridinin (dinoflagellate pigment) | mg m⁻³ |
| `Zea_mgm3` | Zeaxanthin (cyanobacteria pigment) | mg m⁻³ |
| `Salinity` | Salinity | PSU |
| `Oxygen_umolL` | Dissolved Oxygen | µmol L⁻¹ |
| `Ammonium_umolL` | Ammonium | µmol L⁻¹ |
| `Nitrate_umolL` | Nitrate | µmol L⁻¹ |
| `SecchiDepth_m` | Secchi depth (water clarity) | m |
| `*_flag` | Quality flags: `1` = good, `9` = missing/not measured | — |

> **Note on flags:** Before analysis, filter out rows where the relevant variable's flag is `9` (not measured). Flag `2` indicates data of questionable quality — consider how you handle these values and document your decision.

---

## Your Task

The Rottnest Island NRS sits at the boundary of oligotrophic offshore waters and the seasonally productive coastal zone of southwest Western Australia. Chlorophyll-*a* is a primary indicator of phytoplankton biomass and ecosystem productivity — but its story varies by season, depth, and community composition.

**Your task is to explore and communicate the Chl-*a* story in this dataset.**

### Minimum requirements

1. **Clean & prepare** the dataset
   - Parse dates correctly
   - Handle quality flags appropriately
   - Separate depth-profile samples from WC (water column) integrated samples — these are different measurement types and should be treated differently

2. **Visualise** — produce at least one clear figure (subplots welcome). Suggested directions:
   - Surface (0 m) Chl-*a* time series with seasonal context
   - Depth-time heatmap showing the DCM (deep chlorophyll maximum)
   - Seasonal cycle (e.g. monthly climatology)
   - Accessory pigment breakdown (Fuco, Perid, Zea) as a proxy for community composition
   - Relationship between Chl-*a* and a co-measured variable (e.g. nutrients, Secchi depth, oxygen)

3. **Summarise** — a few bullet points describing:
   - The dominant seasonal patterns you observe
   - Any long-term trends or inter-annual variability
   - Gaps, anomalies, or caveats in the data

### Stretch (optional)

- Compute a climatological mean depth profile and show the typical DCM depth
- Investigate whether the divinyl fraction (`DvCphlA_mgm3`) shows distinct seasonal behaviour from total Chl-*a*
- Compare surface Chl-*a* against Secchi depth and discuss the relationship

---

## What to Deliver

Please email your work **one day before the 2nd round interview** as:

- **Script** — a Jupyter notebook (`.ipynb`), R Markdown (`.Rmd`), or MATLAB script (`.m`)
- **Short Summary** — a 1-page summary (Word, PDF, HTML, or Markdown) including your key findings and plot(s)

---

## Estimated Time

⏱ **45–60 minutes**

---

## Assessment Criteria

We are looking for:

- **Data handling** — correct treatment of flags, mixed sample types, and missing values
- **Visualisation** — clear, well-labelled figures that tell a story without clutter
- **Scientific interpretation** — does the narrative reflect an understanding of coastal marine ecology?
- **Communication** — concise written summary accessible to a non-specialist audience

You do not need to produce a polished report. Clarity of thinking and code quality matter more than completeness.

---

## About

This exercise is part of the environmental modelling candidate assessment at BMT. It tests your ability to work with observational water quality datasets, exercise scientific judgement in data cleaning, and communicate environmental insights clearly.
