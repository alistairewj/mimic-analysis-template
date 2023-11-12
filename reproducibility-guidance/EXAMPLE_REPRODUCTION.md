# Reproduction of the MIMIC-IV arterial line study

This is an example of the [REPRODUCTION_TEMPLATE.md](REPRODUCTION_TEMPLATE.md) file filled in using info from the MIMIC-IV arterial line reproduction, available at the following GitHub repo: [mimic-iv-aline-study](https://github.com/alistairewj/mimic-iv-aline-study.git).

## Study information

### Reference to the study

Reference:

> Hsu DJ, Feng M, Kothari R, Zhou H, Chen KP, Celi LA. The association between indwelling arterial catheters and mortality in hemodynamically stable patients with respiratory failure: a propensity score analysis. CHEST Journal. 2015 Dec 1;148(6):1470-6.

DOI: https://doi.org/10.1378/chest.15-0516

### Objective(s) of the study

Assess whether indwelling arterial catheter use was associated with mortality in patients who are mechanically ventilated and do not require vasopressor support.

### Dataset(s) used

* MIMIC-II, unknown version
* DOI (or link if no DOI available): https://doi.org/10.13026/C2NC7F.
* Citation: Raffa, J. (2016). Clinical data from the MIMIC-II database for a case study on indwelling arterial catheters (version 1.0). PhysioNet.
* Other relevant information (link to dataset documentation, etc): Raffa J.D., Ghassemi M., Naumann T., Feng M., Hsu D. (2016) Data Analysis. In: Secondary Analysis of Electronic Health Records. Springer, Cham

## Original paper analysis

### Data extraction

#### Variables

Sourced from e-Appendix 1, section A.1.

Variable | Description | Notes
--- | --- | ---
Arterial line | Use of an arterial line | 
Age | Age on hospital admission |
Gender | | 
Race | |
Weight | Weight in kg |
SAPS-I | Simplified Acute Physiology Score on the first day of the ICU admission | 
SOFA | Sequential Organ Failure Assessment on the first day of the ICU admission | 
Service | ICU service patient admitted under | 
Day of the week | e.g. Monday, Tuesday, etc. | 
Time of day | e.g. 10am, 11am | 
Congestive Heart Failure | | 
Atrial Fibrillation | | 
Chronic Renal Failure  | | 
End stage liver disease  | | 
COPD  | | 
History of stroke | | 
Hematologic malignancy | | 
Respiratory failure | | 
iv_day_1 | input fluids by IV on day 1 (mL, numeric) | 
Sedative usage | Includes fentanyl, midazolam, or propofol |

Below variables are extracted as the first value after mechanical ventilation.

Variable | Description | Notes
--- | --- | ---
map_1st | Mean arterial pressure (mmHg, numeric) | 
hr_1st | Heart Rate (numeric) | 
temp_1st | Temperature (F, numeric) | 
spo2_1st | SpO2 (%, numeric) | 
abg_count | arterial blood gas count (number of tests, numeric) | 
wbc_first | White blood cell count (K/uL, numeric) | 
hgb_first | Hemoglobin (g/dL, numeric) | 
platelet_first | Platelets (K/u, numericL) | 
sodium_first | Sodium (mEq/L, numeric) | 
potassium_first | Potassium (mEq/L, numeric) | 
tco2_first | Bicarbonate (mEq/L, numeric) | 
chloride_first | Chloride (mEq/L, numeric) | 
bun_first | Blood urea nitrogen (mg/dL, numeric) | 
creatinine_first | Creatinine (mg/dL, numeric) | 
po2_first | Partial pressure of oxygen in the arterial blood (mmHg, numeric) | 
pco2_first | Partial pressure of carbon dioxide in the arterial blood (mmHg, numeric) | 

#### Outcome Measures

* 28-day mortality
* ICU length of stay
* Duration of mechanical ventilation
* Number of arterial blood gas measurements performed per day
* Number of venous blood gas measurements performed per day

#### Inclusion criteria

* Adult patients
* Presence of an IAC
* First ICU admission

#### Exclusion criteria

* Sepsis according to criteria of Angus et al.
* Vasopressors while in the ICU
* IAC placement done before mechanical ventilation (incl pre-ICU)
* Cardiac surgery recovery unit

### Population summary

Population measure | Original Study
--- | --- 
TBD | 


### Analysis method

* Propensity score matching
    * caliper 0.01
    * one-to-one
    * without replacement
    * tested differences in matched groups
* McNemar test on binary outcomes
* Paired t-test on continuous outcomes

### Power calculations (if present)

None present.

#### Outlier handling

Not described.

#### Missing data handling

Not described.

### Evaluation measures

p-value for McNemar test and paired t-tset.

e.g. p-value, effect sizes, statistical tests, performance measures like area under the receiver operator characteristic curve, etc.

### Sensitivity Analyses

* varying timing of mechanical ventilation exclusion
* varying caliper levels
* propensity score weighting rather than matching

## Reproduction Analysis

### Dataset(s) used

* MIMIC-IV v0.4
* DOI (or link if no DOI available): https://doi.org/10.13026/a3wn-hq05
* Citation: Johnson, A., Bulgarelli, L., Pollard, T., Horng, S., Celi, L. A., & Mark, R. (2020). MIMIC-IV (version 0.4). PhysioNet.
* Other relevant information (link to dataset documentation, etc): https://mimic.mit.edu

### Known differences

* (minor) the original study subselected variables using a genetic algorithm, whereas we simply use the final set of variables they report
* (minor) we did not include PO2 and PCO2 in the propensity score
* (minor) we removed patients based on hospital service, not ICU service

### Unknown differences

* (major) The number of admissions removed for IAC before admission is *way* higher in the original study than ours.

### Comparison of population

A table comparing the population measures between the original and the reproduction.

Population measure | Original Study | Reproduction
--- | --- | ---
TBD | | 

### Comparison of results

Evaluation measure | Original Study | Reproduction
--- | --- | ---
 | | 