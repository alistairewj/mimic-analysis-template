# Reproduction template

The goal of this template is to guide documentation of a reproduction of a study in an electronic health record database. Reproductions are assumed to be retrospective observational studies.

This template is based on material from the OSF, as well as from Brandt et al., 2013.

## Study information

### Objective(s) of the study

Describe the primary and secondary objectives of the research study.

### Dataset(s) used

Describe the dataset used in the original study. Include:

* Dataset name and version
* DOI (or link if no DOI available)
* Citation
* Other relevant information (link to dataset documentation, etc)

## Original paper analysis

### Data extraction

#### Variables

List out the covariates and exposures extracted for the study, e.g. admission source.
If describing a time-varying covariate, be specific regarding the aggregation and the time window (e.g. "lowest mean arterial pressure during the first 24 hours of the ICU stay.").

#### Outcome(s)

List the outcome(s) used in the study, e.g. 28-day mortality.

#### Inclusion/Exclusion criteria

Describe the inclusion criteria for the study. Since inclusion/exclusion criteria are interchangeable, decide on the most clear presentation of the study methodology, e.g. "the study included all adults, and excluded patients admitted to CSRU."

### Population summary

Provide information about the original study's population: sample size, average mortality, etc. Typically the data is presented in the first table (i.e. Table 1). Select a parsimonious set of descriptors which you will compare your reproduction against. At the very least include the sample size and a summary measure of the outcome(s).

### Analysis method

Explain the analysis method of the study.

### Power calculations (if present)

If a power calculation is present, describe the approach and the assumptions made.

#### Outlier handling

If outliers were specially processed, describe the approach here.

#### Missing data handling

For any missing data present in the study, explain the approach to handle it.

### Evaluation measures

e.g. p-value, effect sizes, statistical tests, performance measures like area under the receiver operator characteristic curve, etc.

### Sensitivity Analyses

Describe any additional sensitivity analyses performed in the study.

## Reproduction

### Dataset(s) used

Describe the dataset used in the reproduction. Include the same information as above, that is at least:

* Dataset name and version
* DOI (or link if no DOI available)
* Citation
* Other relevant information (link to dataset documentation, etc)

If the same dataset in the original study is used for the reproduction, reference the prior section.

### Known differences

Specify changes to the data processing and/or methodology which are known to you. For each difference, describe: (1) the original study approach, (2) the reproduction approach, (3) the justification for the change. If possible, classify the differences as major (could impact the result of the study) or minor (unlikely to change the result of the study).

### Unknown differences

Specify changes to the data processing and/or methodology which *may* have occurred, but you are unable to confirm due to ambiguity in the original material studied. For each difference, describe (1) the most specific reference to the approach in the original study, if possible, and (2) the approach taken in the reproduction.

### Comparison of population

A table comparing the population measures between the original and the reproduction.

Population measure | Original Study | Reproduction
--- | --- | ---
TBD | | 

### Comparison of results

A table of the evaluation measures comparing the results in the original study and the reproduction. Also include the final size of the cohort, proportion of individuals excluded, and other important summary measures for the study.

Evaluation measure | Original Study | Reproduction
--- | --- | ---
TBD | | 