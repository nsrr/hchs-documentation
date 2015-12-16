# Dataset Introduction

The [HCHS/SOL dataset](:files_path:/datasets) posted on the NSRR has gone through various post-processing steps in order to prepare the data for more widespread sharing. The dataset was based upon the [data prepared and deposited on BioLINCC in October 2015](https://biolincc.nhlbi.nih.gov/studies/hchssol/?q=hchs) by the Collaborative Studies Coordinating Center at UNC Chapel Hill. Changes and updates to the source data and variable definitions have been coordinated in the [hchs-data-dictionary repository](https://github.com/sleepepi/hchs-data-dictionary).

## Structure of the Dataset

For the NSRR, we have chosen key datasets and variables from the BioLINCC posting and collapsed them into a new, NSRR-specific dataset. The following HCHS/SOL individual datasets have been converted and processed into the NSRR-specific format:

### `part_derv_lad1.sas7bdat`

The participant derived variable dataset is not associated solely with any particular form because it contains variables from many forms and files. There is one record per enrolled participant (16,415 observations) at baseline PART_DERV_LAD1. This file is a cross-section of "derived variables" whose values are defined based on combinations of data items (e.g. age from date of birth, or body mass index from height and weight, waist-hip ratio from girth measurements), primarily from the anthropometry, demographics, respiratory history, clinical laboratory analysis and pulmonary function records. Important study design variables like sample weight and strata identifiers are also found here.
