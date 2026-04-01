# A Collective Mode of Inequality: Random Matrix Evidence from Latin America

**journal:** Economics Letters  (In review)
**Author:** Andy Domínguez-Monterroza  
**Affiliations:** Universidad Santo Tomás · Pontificia Universidad Javeriana · Bogotá, Colombia

---

## Overview

This repository contains the replication code and processed data for the paper.
We apply Random Matrix Theory (RMT) to the cross-country correlation structure
of Gini coefficient dynamics in fifteen Latin American economies (2001–2023).
A single eigenvalue significantly exceeds the Marchenko–Pastur noise threshold
(λ₁ = 3.480 > λ₊ = 3.333, p = 0.007), identifying a collective mode of
inequality co-movement that explains 23% of regional variance.

---

## Repository structure
```
├── data/
│   ├── gini_panel_2001_2023.csv      # Interpolated Gini panel (15 × 23)
│   ├── gini_all_years.csv            # Raw SEDLAC data, all years
│   ├── correlation_matrix.csv        # Empirical correlation matrix C (15 × 15)
│   └── eigenvalue_table.csv          # Eigenvalue decomposition summary
├── figs/
│   ├── fig1_spectrum.pdf             # Eigenvalue spectrum vs. Marchenko–Pastur
│   └── fig2_loadings.pdf             # Eigenvector loadings, collective mode
├── RMT_Inequality_LAC.ipynb          # Main analysis notebook
└── README.md
```

## Data source

Raw data: **SEDLAC** (CEDLAS and The World Bank), September 2025.  
Freely available at: https://www.cedlas.econo.unlp.edu.ar

> SEDLAC (CEDLAS and The World Bank). Socio-Economic Database for Latin
> America and the Caribbean. Accessed September 2025.

---

## Requirements
```bash
pip install numpy pandas matplotlib scipy openpyxl
```

---

## Replication

1. Place `2025_Act1_inequality_LAC.xlsx` in the root directory
2. Open `RMT_Inequality_LAC.ipynb`
3. Run all cells — figures and CSVs are generated automatically

---

## Key results

| Mode | λᵢ | Var. (%) | PR |
|------|----|----------|----|
| 1 *| 3.480 | 23.2 | 8.84 |
| 2 | 2.511 | 16.7 | 8.77 |
| 3 | 1.822 | 12.1 | 5.37 |

*Exceeds Marchenko–Pastur upper bound (λ₊ = 3.333, p = 0.007, Monte Carlo n = 5,000).

---

## License

Code: MIT  
Data: subject to SEDLAC terms of use (non-commercial, citation required)
