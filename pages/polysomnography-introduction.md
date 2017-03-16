# Polysomnography introduction

In-home polysomnography (PSG) was conducted using the Apnea Risk Evaluation System (ARES Unicorder, Advanced Brain Imaging, Carlsbad CA).  Nocturnal recordings were transmitted to the centralized reading center at Brigham and Women's Hospital and data were scored by trained technicians using current guidelines.

Notes:

- [ARES Montage and Sampling Rate Information](:pages_path:/montage-and-sampling-rate-information.md)
- [Baseline Sleep Monitoring Manual](:files_path:/documentation?f=HCHS_SOL_Baseline_Sleep_Monitoring_Manual.pdf)
- [ARES Unicorder validation manuscript](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2276822/)

## Signal and annotation files

[Raw polysomnography data](:files_path:/polysomnography) are available for 12,088 HCHS/SOL participants. Each recording has a signal file (.EDF) and event scoring annotations (.XML).

1. **[EDF](:files_path:/polysomnography/edfs)** - Signal files in the [European Data Format](http://www.edfplus.info/) exported from Compumedics Profusion.
2. **[XML (NSRR)](:files_path:/polysomnography/annotations-events-nsrr)** - Annotation files processed in the [EDF Editor and Translator](https://www.sleepdata.org/community/tools/12) tool.

## Known issues

- *Not all subjects with sleep monitor data have EDF/XML files* - There were issues converting ARES Unicorder raw data to EDF/XML. A brief summary is below:
  - Studies were processed using ARES Insight Software to produce EDF signal and XML annotation files. Pilot studies were not processed. Studies with an overall quality of -1 (no valid data) were not processed. There were 395 studies with an overall quality grade of 0 or greater that were missing. Some studies were missing components to properly complete the exportation process. Some studies produced errors during the exportation process. Duplicate studies were removed. Studies that did not pass integrity checks were removed. Studies without an official HCHS ID were removed. Studies from subjects that were not part of the HCHS Limited Access Dataset were removed.

## History / changelog

*March 2017*
- Polysomnography data uploaded to sleepdata.org after exports from ARES software

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
