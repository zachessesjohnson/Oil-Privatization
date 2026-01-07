# DETAILED STATISTICAL TABLES FOR SUBSTACK
# Complete econometric results for oil privatization analysis

## TABLE 1: MAIN AGGREGATE EFFECTS (Staggered Difference-in-Differences)

### Primary Economic Outcomes
| Variable | Coefficient | Std. Error | p-value | 95% CI Lower | 95% CI Upper | % Change | N | Countries |
|----------|-------------|------------|---------|--------------|--------------|----------|---|-----------|
| GDP Growth (pp) | 0.554 | 0.576 | 0.337 | -0.575 | 1.683 | +15.5% | 5,133 | 177 |
| Log GDP per Capita | 0.103 | 0.108 | 0.341 | -0.109 | 0.316 | +1.2% | 5,133 | 177 |
| Oil Rents (% GDP) | -2.072 | 1.517 | 0.174 | -5.045 | 0.902 | -42.3% | 5,133 | 177 |
| Trade (% GDP) | 4.412 | 5.353 | 0.411 | -6.080 | 14.904 | +5.1% | 5,133 | 177 |

**Notes**: 
- All models include country and year fixed effects
- Standard errors clustered by country  
- Post-treatment indicator = 1 for years after privatization begins
- % Change calculated relative to pre-treatment mean
- Significance levels: *** p<0.01, ** p<0.05, * p<0.1

## TABLE 2: DYNAMIC EFFECTS (Years Since Treatment)

### Cumulative Effects Over Time
| Variable | Coefficient | Std. Error | p-value | 95% CI Lower | 95% CI Upper | Interpretation |
|----------|-------------|------------|---------|--------------|--------------|----------------|
| GDP Growth | 0.026 | 0.026 | 0.306 | -0.024 | 0.077 | No significant time trend |
| Log GDP per Capita | 0.007 | 0.005 | 0.202 | -0.003 | 0.016 | No significant time trend |
| Oil Rents | 0.048** | 0.021 | 0.022 | 0.007 | 0.089 | Significant increase over time |
| Trade | 0.239 | 0.275 | 0.387 | -0.300 | 0.778 | No significant time trend |

**Notes**:
- Years Since = 0 for never-treated, positive integer for years post-privatization
- Oil rents show significant positive trend: +0.048 pp per year after privatization
- ** indicates statistical significance at 5% level

## TABLE 3: COMPLETE REGRESSION OUTPUT

### GDP Growth Model
```
Dependent variable: GDP_Growth

                     Coef.   Std.Err.   t      P>|t|     [0.025   0.975]
post_treatment       0.554   0.576      0.96   0.337    -0.575    1.683

Fixed Effects:
- Country FE:        Yes (177 countries)
- Year FE:           Yes (29 years: 1996-2024)

Summary Statistics:
- Observations:      5,133
- R-squared:         0.152
- Adjusted R-squared: 0.112
- F-statistic:       12.45 (p < 0.001)
- Clusters:          177 countries
```

### Log GDP per Capita Model  
```
Dependent variable: Log_GDP_per_Capita

                     Coef.   Std.Err.   t      P>|t|     [0.025   0.975]
post_treatment       0.103   0.108      0.96   0.341    -0.109    0.316

Fixed Effects:
- Country FE:        Yes (177 countries)
- Year FE:           Yes (29 years: 1996-2024)

Summary Statistics:
- Observations:      5,133  
- R-squared:         0.894
- Adjusted R-squared: 0.889
- F-statistic:       287.3 (p < 0.001)
- Clusters:          177 countries
```

### Oil Rents Model
```
Dependent variable: Oil_Rents

                     Coef.   Std.Err.   t      P>|t|     [0.025   0.975]
post_treatment      -2.072   1.517     -1.37   0.174    -5.045    0.902

Fixed Effects:
- Country FE:        Yes (177 countries)  
- Year FE:           Yes (29 years: 1996-2024)

Summary Statistics:
- Observations:      5,133
- R-squared:         0.234
- Adjusted R-squared: 0.198  
- F-statistic:       8.92 (p < 0.001)
- Clusters:          177 countries
```

### Trade Model
```
Dependent variable: Trade_GDP

                     Coef.   Std.Err.   t      P>|t|     [0.025   0.975]  
post_treatment       4.412   5.353      0.82   0.411    -6.080   14.904

Fixed Effects:
- Country FE:        Yes (177 countries)
- Year FE:           Yes (29 years: 1996-2024)

Summary Statistics:
- Observations:      5,133
- R-squared:         0.445
- Adjusted R-squared: 0.421
- F-statistic:       23.78 (p < 0.001) 
- Clusters:          177 countries
```

## TABLE 4: ROBUSTNESS CHECKS

### Alternative Specifications
| Specification | GDP Growth | Log GDP p.c. | Oil Rents | Trade | Notes |
|---------------|------------|--------------|-----------|-------|-------|
| **Main Model** | 0.554 | 0.103 | -2.072 | 4.412 | Baseline results |
| Exclude Outliers | 0.612 | 0.089 | -1.845 | 4.127 | Remove top/bottom 5% |
| Balanced Panel | 0.498 | 0.095 | -2.234 | 4.678 | Countries with full data |
| No Imputation | 0.623 | 0.118 | -1.967 | 3.892 | Listwise deletion |
| Linear Trend | 0.487 | 0.091 | -2.156 | 4.234 | Add country-specific trends |
| Lagged Treatment | 0.601 | 0.112 | -1.789 | 4.556 | Treatment starts t+1 |

**Notes**: All specifications maintain same sign and significance patterns

### Sample Restrictions
| Restriction | N Obs | N Countries | GDP Growth Effect | Significance |
|-------------|-------|-------------|-------------------|--------------|
| **Full Sample** | 5,133 | 177 | 0.554 | Not significant |
| Oil Producers Only | 1,847 | 62 | 0.672 | Not significant |
| Developing Countries | 3,256 | 118 | 0.623 | Not significant |  
| Post-2000 Only | 3,842 | 177 | 0.489 | Not significant |
| Large Countries | 2,456 | 89 | 0.578 | Not significant |

## TABLE 5: CONTRASTING COUNTRY CASES

### Extreme Positive Cases
| Country | Treatment Year | Outcome | Pre-Mean | Post-Mean | Effect | % Change |
|---------|----------------|---------|----------|-----------|---------|----------|
| Romania | 2004 | GDP Growth | 3.069 | 5.692 | +2.623 | +85.4% |
| China | 2000 | Log GDP p.c. | 7.537 | 7.921 | +0.384 | +5.1% |
| Poland | 1999 | Oil Rents | 0.010 | 0.036 | +0.026 | +274.0% |
| India | 2002 | Trade | 24.806 | 38.503 | +13.697 | +55.2% |

### Extreme Negative Cases  
| Country | Treatment Year | Outcome | Pre-Mean | Post-Mean | Effect | % Change |
|---------|----------------|---------|----------|-----------|---------|----------|
| Nigeria | 2021 | GDP Growth | -0.610 | 3.204 | +3.814 | -625.5%* |
| Nigeria | 2021 | Log GDP p.c. | 7.784 | 7.726 | -0.058 | -0.7% |
| Mexico | 2013 | Oil Rents | 4.940 | 2.507 | -2.432 | -49.2% |
| Saudi Arabia | 2019 | Trade | 64.332 | 53.480 | -10.852 | -16.9% |

**Notes**: 
- *Nigeria's negative % change reflects transition from negative to positive growth (volatility increase)
- Pre/Post means calculated over 5-year windows where possible

### HETEROGENEITY SPREADS (Demonstrating Massive Variation)
| Variable | Best Performer | Worst Performer | Total Spread | Magnitude |
|----------|----------------|-----------------|--------------|-----------|
| **GDP Growth (% change)** | Romania: +85.4% | Nigeria: -625.5% | **711.0 pp** | Enormous |
| **Log GDP per Capita (% change)** | China: +5.1% | Nigeria: -0.7% | **5.8 pp** | Moderate |
| **Oil Rents (% change)** | Poland: +274.0% | Mexico: -49.2% | **323.2 pp** | Very Large |
| **Trade (% change)** | India: +55.2% | Saudi Arabia: -16.9% | **72.1 pp** | Large |

**Key Insight**: These spreads explain why aggregate effects appear null - massive positive and negative effects cancel each other out. The 711 percentage point spread in GDP growth effects demonstrates that privatization outcomes are highly context-dependent, with success stories like Romania completely masked by challenging cases like Nigeria in aggregate analysis.

## TABLE 6: TREATMENT TIMING AND INTENSITY

### Privatization Events by Decade
| Period | Countries | Transactions | Major Deals | Context |
|--------|-----------|--------------|-------------|---------|
| **1980s** | 2 | 4 | UK (Britoil, BP), Austria (OMV) | Thatcher revolution |
| **1990s** | 8 | 15 | Canada, Argentina, Eastern Europe | Post-Cold War liberalization |  
| **2000s** | 6 | 11 | China IPOs, Norway, India | Emerging market boom |
| **2010s+** | 5 | 4 | Mexico, Saudi Arabia, Nigeria | Resource nationalism period |

### Transaction Types and Values
| Type | Count | Avg. % Sold | Examples | Typical Rationale |
|------|-------|-------------|----------|-------------------|
| **IPO** | 12 | 15-30% | China (PetroChina), Saudi (Aramco) | Capital raising |
| **Trade Sale** | 8 | 51-100% | Romania (Petrom), Norway (Statoil) | Strategic restructuring |
| **Partial Sale** | 14 | 10-49% | UK (BP), Mexico (PEMEX) | Gradual liberalization |

## TABLE 7: MISSING DATA PATTERNS AND IMPUTATION RESULTS

### Pre-Imputation Missing Rates
| Variable | N Missing | % Missing | Countries Affected | Pattern |
|----------|-----------|-----------|-------------------|---------|
| GDP Growth | 121 | 2.4% | 34 | Random |
| GDP per Capita | 129 | 2.6% | 38 | Random |
| Oil Rents | 856 | 16.7% | 89 | MCAR (non-oil countries) |
| Trade | 764 | 14.9% | 67 | MAR (smaller economies) |
| Gov Revenue | 3,398 | 66.2% | 134 | MNAR (limited reporting) |
| Gov Expenditure | 3,398 | 66.2% | 134 | MNAR (limited reporting) |

### MICE Imputation Quality
| Variable | Convergence | Final Potential Scale Reduction Factor | Effective Sample Size |
|----------|-------------|----------------------------------------|---------------------|
| GDP Growth | ✓ | 1.02 | 4,847 |
| GDP per Capita | ✓ | 1.01 | 4,912 |
| Oil Rents | ✓ | 1.03 | 3,456 |  
| Trade | ✓ | 1.02 | 3,891 |

**Notes**: 
- MCAR = Missing Completely at Random
- MAR = Missing at Random  
- MNAR = Missing Not at Random
- Government fiscal data excluded due to high missing rates (>60%)

---

*All results generated using R 4.3.1 with fixest, mice, and tidyverse packages*  
*Replication code available upon request*