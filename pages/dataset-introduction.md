# Dataset Introduction

The [HCHS/SOL datasets](:files_path:/datasets) posted on the NSRR have gone through various post-processing steps in order to prepare the data for more widespread sharing. The datasets were based upon the [data prepared and deposited on BioLINCC](https://biolincc.nhlbi.nih.gov/studies/hchssol/?q=hchs) by the Collaborative Studies Coordinating Center at UNC Chapel Hill. Changes and updates to the source data and variable definitions have been coordinated in the [hchs-data-dictionary repository](https://github.com/sleepepi/hchs-data-dictionary).

The [documentation folder](:files_path:/documentation) contains more detailed descriptions of the data collection protocols and source datasets.

## Structure of the Dataset

For the NSRR, we have chosen key datasets and variables from the BioLINCC posting and collapsed them into new, NSRR-specific datasets. The following HCHS/SOL individual datasets have been converted and processed into the NSRR-specific format:

### `part_derv_lad1.sas7bdat` (Baseline Visit)

The participant derived variable dataset is not associated solely with any particular form because it contains variables from many forms and files. There is one record per enrolled participant (16,415 observations) at baseline `PART_DERV_LAD1`. This file is a cross-section of "derived variables" whose values are defined based on combinations of data items (e.g. age from date of birth, or body mass index from height and weight, waist-hip ratio from girth measurements), primarily from the anthropometry, demographics, respiratory history, clinical laboratory analysis and pulmonary function records. Important study design variables like sample weight and strata identifiers are also found here.

### `slea_lad1.sas7bdat` (Baseline Visit)

The sleep history questionnaire is a composite instrument derived from several sleep studies and retaining items thought to be most useful in the interpretation of sleep disorders when combined with information from the sleep monitor. Sleep duration variables have been updated in this version of the dataset.

### `slpa_lad1.sas7bdat` (Baseline Visit)

The Sleep Reading Center at Case Western Reserve University processes the overnight sleep studies recorded on the ARES model #5 sleep monitors which have been uploaded to them from the field centers. Use of the ARES device is described in HCHS/SOL Manual of Operations 6. The reading center produces one summary record per sleep study.

### `part_derv_sueno_lad1.sas7bdat` (Sueño Ancillary Visit)

The participant derived variable data sets are not associated solely with any particular form because they contain variables from many forms. There is one record per enrolled participant in the LAD1 (2,252 observations) but complete data is present for only the 1,912 who agreed to share their data with researchers external to the HCHS/SOL investigators. In addition, the same exclusions used for the investigator use files were applied to the dataset, `PART_DERV_SUENO_LAD1` which included 63 individuals who are not eligible due to being age 65 or older, interviewed more than 30 months from HCHS/SOL baseline, have AHI>50 at baseline, or not eligible Hispanic/Latino Background for the site). Indicator variable `SUENO_ELIGIBLE` flags those who meet Sueño eligibility criteria. This file is a cross-section of "derived variables" whose values are defined based on combinations of data items (e.g. age from date of birth, or body mass index from height and weight, etc.). See the separate document, "SUEÑO Derived Variable Dictionary" for the definitions of the variables included in this special purpose file.

The participant derived file includes several demographic variables from the HCHS/SOL main study, and all the remaining variables are derived from SUENO data. In some cases the variable name ends with `_SUENO` to explicitly state that this variable is derived from Sueno data. For example variable `BMI_SUENO` was derived from height and weight measured at Sueno visit (SUENO APEA form).

### `sawa_lad1.sas7bdat` (Sueño Ancillary Visit)

Participants were given a wrist actigraph device (Respironics Spectrum); this device records movement and is used to infer sleep and wake times. The participant was asked to wear the device for 7 consecutive days and nights. At the Field Center, actigraphy data was downloaded and transmitted to the Sleep Reading Center. Data released to investigators ONLY include sleep studies with valid status (SAWA4=1), and the variable with the invalid reason (SAWA5) was removed.
