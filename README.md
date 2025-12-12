# Stable Survival Extrapolation using Mortality Projections

This repository contains the code accompanying the paper:

**Anastasios Apsemidis and Nikolaos Demiris**
*Stable Survival Extrapolation using Mortality Projections*
*Biometrics*, Volume 81, Issue 4, December 2025
DOI: ujaf159

---

## Abstract
The mean survival is the key ingredient of the decision process in several applications, notably in health economic evaluations. It is defined as the area under the complete survival curve, thus necessitating extrapolation of the observed data. This may be achieved in a more stable manner by borrowing long term evidence from registry and demographic data. In this article we employ a Bayesian mortality model and transfer its projections in order to construct the baseline population that acts as an anchor of the survival model. We then propose extrapolation methods based on flexible parametric poly-hazard models which can naturally accommodate diverse shapes, including non-proportional hazards and crossing survival curves, while typically maintaining a natural interpretation as a data generating mechanism. We estimate the mean survival and related estimands in three cases, namely breast cancer, advanced melanoma and cardiac arrhythmia. Specifically, we evaluate the survival disadvantage of triple-negative breast cancer cases, the efficacy of combining immunotherapy with mRNA cancer therapeutics for melanoma treatment and the suitability of implantable cardioverter defibrilators for cardiac arrhythmia. The last is conducted in a competing risks context illustrating how working on the cause-specific hazard alone minimizes potential instability. The results suggest that the proposed approach offers a flexible, interpretable and robust approach when survival extrapolation is required.

---

## Repository structure

### Data
Contains the external population data and the extracted data from published Kaplan–Meier curves used throughout the paper:
- `prop_f.csv`, `prop_m.csv` – proportions for the arrhythmia example
- `surv_f.R`, `surv_m.R` – female and male survival data of the external population
- `surv_icd.csv` – ICD data
- `surv_pemb.csv` – melanoma data

### Code
Contains the R code for reproducing the four examples considered in the paper, as well as the Lee–Carter mortality model.

- **Advanced melanoma example**
  - `[R] melanoma_example`
  - `[R] melanoma_example_extrapolation`

- **Breast cancer example**
  - `[R] BC_example`
  - `[R] BC_example_extrapolation`

- **Cardiac arrhythmia example**
  - `[R] arrhythmia_example`
  - `[R] arrhythmia_example_extrapolation`

- **Mortality projections**
  - `[R] Mortality_projections`

- **Precision medicine example (Triple-negative breast cancer)**
  - `[R] BC_3N_example`
  - `[R] BC_3N_example_extrapolation`

---

## Requirements
- **R** ≥ 4.0
- R packages:
  - `survival`, `muhaz`, `pracma`, `ggplot2`, `rstan`, `BayesMortalityPlus`

---

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/apsemidis/SurvExtr.git
   cd SurvExtr
   ```

2. Ensure the `Data/` folder contains the required datasets (`prop_f.csv`, `surv_icd.csv`, etc.).

3. Run the desired example by sourcing the corresponding R script, e.g.:
   ```R
   # Breast cancer example
   source("Code/Breast cancer example/[R] BC_example")

   # Advanced melanoma example
   source("Code/Advanced melanoma example/[R] melanoma_example")

   # Cardiac arrhythmia example
   source("Code/Cardiac arrythmia example/[R] arrhythmia_example")

   # Mortality projections (Lee–Carter model)
   source("Code/Mortality projections/[R] Mortality_projections")
   ```

---

## Citation
If you use this code, please cite:

> Apsemidis, A. and Demiris, N. *Stable Survival Extrapolation using Mortality Projections.* *Biometrics*, Volume 81, Issue 4, December 2025, ujaf159, https://doi.org/10.1093/biomtc/ujaf159.

---

## Contact
- Anastasios Apsemidis – [apsemidis@aueb.gr](mailto:apsemidis@aueb.gr)
- Nikolaos Demiris – [nikos@aueb.gr](mailto:nikos@aueb.gr)
