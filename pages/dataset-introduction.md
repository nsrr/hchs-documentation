# Dataset introduction

The [HCHS/SOL datasets](:files_path:/datasets) posted on the NSRR have gone through various post-processing steps in order to prepare the data for more widespread sharing. The datasets were based upon the [data prepared and deposited on BioLINCC](https://biolincc.nhlbi.nih.gov/studies/hchssol/?q=hchs) by the Collaborative Studies Coordinating Center at UNC Chapel Hill. Changes and updates to the source data and variable definitions have been coordinated in the [hchs-data-dictionary repository](https://github.com/nsrr/hchs-data-dictionary).

The [documentation folder](:files_path:/documentation) contains more detailed descriptions of the data collection protocols and source datasets. The [forms folder](:files_path:/forms) contains PDF copies of the original data collection instruments.

## Sharing restrictions

Participants were asked at the time of informed consent about future public data sharing. The HCHS/SOL Coordinating Center **removed data for subjects** who did not consent to any public sharing their data. The [**any_permit**](https://sleepdata.org/datasets/hchs/variables/any_permit) indicates which subjects consented to any public sharing and which did not. Among those who did not consent to sharing, data will be set to missing.

## Dataset structure

For the NSRR, we have chosen key datasets and variables from the BioLINCC posting and collapsed them into new, NSRR-specific datasets. The following HCHS/SOL individual datasets have been converted and processed into the NSRR-specific format. The primary subject identifier is [`PID`](https://sleepdata.org/datasets/hchs/variables/pid).

### `part_derv_lad1.sas7bdat` (Baseline Visit)

The participant derived variable dataset is not associated solely with any particular form because it contains variables from many forms and files. There is one record per enrolled participant (16,415 observations) at baseline `PART_DERV_LAD1`. This file is a cross-section of "derived variables" whose values are defined based on combinations of data items (e.g. age from date of birth, or body mass index from height and weight, waist-hip ratio from girth measurements), primarily from the anthropometry, demographics, respiratory history, clinical laboratory analysis and pulmonary function records. Important study design variables like sample weight and strata identifiers are also found here.

### `slea_lad1.sas7bdat` (Baseline Visit)

The sleep history questionnaire is a composite instrument derived from several sleep studies and retaining items thought to be most useful in the interpretation of sleep disorders when combined with information from the sleep monitor. Sleep duration variables have been updated in this version of the dataset.

### `slpa_lad1.sas7bdat` (Baseline Visit)

The Sleep Reading Center at Case Western Reserve University processes the overnight sleep studies recorded on the ARES model #5 sleep monitors which have been uploaded to them from the field centers. Use of the ARES device is described in HCHS/SOL Manual of Operations 6. The reading center produces one summary record per sleep study.

### `mhea_lad1.sas7bdat` (Baseline Visit)

The 39 item medical history form inquires about non-pulmonary related health conditions. This instrument contains general questions on self-reported cardiovascular disease, stroke, hypertension, hypercholesterolemia, metabolic problems, cancer, and parity.

### `part_derv_sueno_lad1.sas7bdat` (Sueño Ancillary Visit)

The participant derived variable data sets are not associated solely with any particular form because they contain variables from many forms. There is one record per enrolled participant in the LAD1 (2,252 observations) but complete data is present for only the 1,912 who agreed to share their data with researchers external to the HCHS/SOL investigators. In addition, the same exclusions used for the investigator use files were applied to the dataset, `PART_DERV_SUENO_LAD1` which included 63 individuals who are not eligible due to being age 65 or older, interviewed more than 30 months from HCHS/SOL baseline, have AHI>50 at baseline, or not eligible Hispanic/Latino Background for the site). Indicator variable `SUENO_ELIGIBLE` flags those who meet Sueño eligibility criteria. This file is a cross-section of "derived variables" whose values are defined based on combinations of data items (e.g. age from date of birth, or body mass index from height and weight, etc.). See the separate document, "SUEÑO Derived Variable Dictionary" for the definitions of the variables included in this special purpose file.

The participant derived file includes several demographic variables from the HCHS/SOL main study, and all the remaining variables are derived from Sueño data. In some cases the variable name ends with `_SUENO` to explicitly state that this variable is derived from Sueño data. For example variable `BMI_SUENO` was derived from height and weight measured at Sueño visit (SUENO APEA form).

### `sawa_lad1.sas7bdat` (Sueño Ancillary Visit)

Participants were given a wrist actigraph device (Respironics Spectrum); this device records movement and is used to infer sleep and wake times. The participant was asked to wear the device for 7 consecutive days and nights. At the Field Center, actigraphy data was downloaded and transmitted to the Sleep Reading Center. Data released to investigators ONLY include sleep studies with valid status (SAWA4=1), and the variable with the invalid reason (SAWA5) was removed.

### `spea_lad1.sas7bdat` (Sueño Ancillary Visit)

This 18 item instrument provides information about sleep patterns and symptoms of sleep disturbances.

Please note that the Spanish translation for question 18 was updated in SUENO on 09-17-2011 to match the English translation; it does not match the Spanish translation in the HCHS main study Sleep Questionnaire (SLSA).

SUENO SPSA18 original translation and HCHS/SOL main study SLSA18 translation: *¿Son estos síntomas peores en el transcurso del día o durante la noche?*

SUENO SPSA18 updated translation: *¿Son estos síntomas peores mas tarde en el día o durante la noche?*

### `sqea_lad1.sas7bdat` (Sueño Ancillary Visit)

This 25 item instrument provides information about the participant sleep patterns. It also evaluates circadian rhythms, insomnia, and sleep hygiene.

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
