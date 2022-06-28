# Reproduction template

The goal of this template is to guide documentation of a reproduction of a study in an electronic health record database. Reproductions are assumed to be retrospective observational studies.

This template is based on material from the OSF, as well as from Brandt et al., 2013.

## Title of the study

The title of the reproduced study with its digital object identifier (DOI).

## Dataset(s) used

Describe the dataset used in the reproduction. Include the same information as above, that is at least:

* Dataset name and version
* DOI (or link if no DOI available)
* Citation
* Other relevant information (link to dataset documentation, etc)

If the same dataset in the original study is used for the reproduction, reference the prior section.

## Data extraction

### Inclusion/Exclusion criteria

Provide the column names for your proposed "cohort" table, which will apply all inclusion/exclusion criteria. Include the description of the criteria, the table in the dataset you will use, and how missing data will be interpreted (e.g. missing values will be assumed to include the patient).

### Variables

List out the planned source for all covariates and exposures extracted for the study, e.g. admission source.
If describing a time-varying covariate, be specific regarding the aggregation and the time window (e.g. "lowest mean arterial pressure during the first 24 hours of the ICU stay."). The following template is a useful guide.

Variable name | Description | Timing | Aggregation | Source | Notes
--- | --- | --- | --- | --- | ---
Heart Rate Day 1 | Patient heart rate | First 24 hours of ICU stay | Highest | chartevents | 
Sedative use | Midazolam or propofol | Any time during the ICU Stay | Any value | inputevents | 

If unsure about the source, write all possibilities, and justify them in the notes.
Also include in the notes whether outliers were processed (and how), as well as the approach for missing data.

### Outcome(s)

List the outcome(s) used in the study, e.g. 28-day mortality, with similar detail as the above variables.
