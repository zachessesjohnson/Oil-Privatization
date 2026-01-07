# Oil Privatization Effects: A Global Analysis (1996-2024)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![R Version](https://img.shields.io/badge/R-4.3.1-blue.svg)](https://www.r-project.org/)
[![Data](https://img.shields.io/badge/Data-World%20Bank%20%7C%20WGI-green.svg)](https://datacatalog.worldbank.org/)

## Overview

This repository contains a comprehensive econometric analysis of oil privatization effects across 21 countries from 1996-2024. Using staggered difference-in-differences methodology with multiple imputation, we analyze the heterogeneous impacts of oil sector privatization on economic outcomes.

## Key Findings

**Main Result:** Oil privatization shows **no significant aggregate effects** but reveals **massive heterogeneity** across countries:

- **Romania:** +85.4% GDP growth effect
- **Nigeria:** -625.5% GDP growth effect (massive volatility)
- **Poland:** +274% oil sector development increase
- **Effect Spread:** 711 percentage points between best and worst outcomes

**Policy Implication:** Privatization outcomes are highly context-dependent. Success depends on institutional quality, timing, and governance frameworks rather than privatization per se.

## Methodology

- **Research Design:** Staggered Difference-in-Differences with two-way fixed effects
- **Missing Data:** MICE (Multiple Imputation by Chained Equations) with 5 imputations
- **Standard Errors:** Clustered by country
- **Sample:** 5,133 country-year observations across 177 countries
- **Treatment:** 21 countries with 34 privatization events

## Repository Structure

```
Data Files
├── privatization_transactions.csv     # Core privatization events dataset
├── production_datapoints.csv          # Oil production data
├── financial_datapoints.csv           # Company financial data
├── data_sources_metadata.csv          # Data source documentation
├── legitimate_countries.txt           # Validated country list
├── wdi/                              # World Development Indicators
└── wgi/                              # World Governance Indicators

Analysis Scripts
├── mice_staggered_did.R              # Main MICE-based staggered DiD analysis
├── staggered_did_analysis.R          # Enhanced staggered DiD with visualizations
├── contrasting_cases.R               # Individual country heterogeneity analysis
├── enhanced_event_study.R            # Professional time series validation
└── final_graphics.R                  # Publication-ready visualizations

Documentation
├── README_DATASET.md                 # Detailed data documentation
├── COMPREHENSIVE_ANALYSIS_SUMMARY.md # Complete methodology and results
├── STAGGERED_DID_EXPLANATION.md      # Technical methodology explanation
├── DETAILED_STATS_TABLES.md          # Full econometric results
└── ACCURATE_COUNTRY_TABLE.md         # Country-specific effects table

Visualizations
├── final_heterogeneity.png           # Flagship heterogeneity visualization
├── final_spreads.png                 # Effect variation quantification
├── final_why_averages_lie.png        # Policy lesson demonstration
└── enhanced_staggered_did_event_study.png # Time series validation
```

## How to Reproduce the Analysis

### Requirements

```r
# Required R packages
install.packages(c(
  "dplyr", "ggplot2", "tidyr", "fixest", 
  "mice", "viridis", "gridExtra", "broom"
))
```

- **R Version:** 4.3.1 or higher
- **RAM:** 8GB+ recommended for MICE imputation
- **Runtime:** ~10-15 minutes for full analysis

### Step-by-Step Execution

1. **Clone the repository:**
   ```bash
   git clone [repository-url]
   cd oil-privatization-analysis
   ```

2. **Run main analysis:**
   ```r
   # Complete staggered DiD with MICE imputation
   source("mice_staggered_did.R")
   
   # Enhanced event study visualization
   source("staggered_did_analysis.R")
   
   # Individual country analysis
   source("contrasting_cases.R")
   
   # Create publication graphics
   source("final_graphics.R")
   ```

3. **Output files generated:**
   - Enhanced visualizations (PNG files)
   - Statistical summary tables
   - Individual country effect estimates

## Data Sources

| Dataset | Source | Coverage | Purpose |
|---------|--------|----------|---------|
| **Privatization Events** | Manual compilation from government sources, news reports, academic papers | 1980-2024 | Treatment timing identification |
| **Economic Indicators** | World Bank World Development Indicators | 1996-2024 | Outcome variables (GDP, trade, etc.) |
| **Governance Data** | World Bank Worldwide Governance Indicators | 1996-2024 | Control variables |
| **Oil Production** | BP Statistical Review, national statistics | 1969-2025 | Sector-specific outcomes |
| **Financial Data** | Company annual reports, SEC filings | 1990-2025 | Firm-level performance |

## Key Results Summary

| Variable | Aggregate Effect | Standard Error | P-Value | Heterogeneity Range |
|----------|------------------|----------------|---------|-------------------|
| GDP Growth | +0.554 | (0.576) | 0.337 | -625% to +85% |
| Income Level | +10.3% | (10.8) | 0.344 | -0.7% to +5.1% |
| Oil Dependency | -2.07 | (1.52) | 0.177 | -49% to +274% |
| Trade Openness | +4.41 | (5.35) | 0.413 | -17% to +55% |

*Note: No aggregate effects are statistically significant, but individual country effects show enormous variation.*

## Econometric Specifications

**Basic Staggered DiD:**
```
Y_it = α_i + λ_t + β×Post_it + ε_it
```

**Event Study:**
```
Y_it = α_i + λ_t + Σ_k β_k×D_it^k + ε_it
```

Where:
- `Y_it`: Outcome for country i in year t
- `α_i`: Country fixed effects
- `λ_t`: Year fixed effects  
- `Post_it`: Post-privatization indicator
- `D_it^k`: Event time indicators (k years relative to treatment)

## Policy Implications

1. **Context Matters:** Privatization effects depend critically on institutional quality and timing
2. **No Universal Solution:** One-size-fits-all privatization policies are likely to fail
3. **Heterogeneity is Key:** Average effects mask enormous cross-country variation
4. **Institutional Prerequisites:** Strong governance frameworks appear necessary for success

## Academic Citations

If you use this analysis, please cite:

```bibtex
@article{oil_privatization_2024,
  title={Oil Privatization Effects: A Global Analysis of Heterogeneous Impacts},
  author={[Your Name]},
  year={2024},
  journal={Working Paper},
  note={Available at: https://github.com/[username]/oil-privatization-analysis}
}
```

## Data Citations

- World Bank. (2024). World Development Indicators. Washington, DC: World Bank.
- Kaufmann, D., Kraay, A., & Mastruzzi, M. (2023). The Worldwide Governance Indicators: Methodology and Analytical Issues. World Bank Policy Research Working Paper.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

- **Author:** [Your Name]
- **Email:** [Your Email]
- **LinkedIn:** [Your LinkedIn]
- **Twitter:** [Your Twitter]

## Acknowledgments

- World Bank for providing comprehensive economic and governance data
- The R community for developing excellent econometric packages (`fixest`, `mice`)
- Academic community for methodological contributions to staggered DiD literature

---

**If you find this analysis useful, please consider starring the repository!**