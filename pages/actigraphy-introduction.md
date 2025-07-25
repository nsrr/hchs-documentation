# Actigraphy introduction

The Sueño Ancillary study recruited 2,252 HCHS/SOL participants to wear wrist-worn actigraphy devices ([Actiwatch Spectrum, Philips Respironics](http://www.usa.philips.com/healthcare/product/HC1046964/actiwatch-spectrum-activity-monitor)) between 2010 and 2013. Participants were instructed to wear the watch for a week. Records were scored by a trained technician at the Boston Sleep Reading Center.

The [documentation folder](:files_path:/documentation) contains manuals and in-depth descriptions of the actigraphy devices and scoring process used in the Sueño Ancillary study. Further, the [`hchs-sol-sueno-ancillary` dataset](:files_path:/datasets) contains summary phenotype data from the actigraphy data collection.

## Epoch-by-epoch files

[Epoch-by-epoch (EBE) data files (CSV)](:files_path:/actigraphy) have been created for 1,886 participants with actigraphy data whose HCHS/SOL data are available for public use. Each row in these files represents 30 seconds worth of summary data from the actigraphy device. Based upon the Sueño actigraphy scoring, invalid (low quality) days were removed from these files. A day was marked invalid if 1) there were 4 or more hours of offwrist/invalid time or 2) the main sleep period contained offwrist/invalid time.

Notes:

- The Sueño Ancillary study used actigraphy primarily as a means to estimate sleep and wake times, **not** as a means to assess physical activity.
- The `day` indicator in the file runs from noon-to-noon (i.e. not midnight-to-midnight) because the goal was to have each individual day in the file wholly contain a single main sleep period.
- Original dates have been removed. The `date_shifted` variable represents a reconstructed date aligned to the same day of the week in the first week of the year 2000.
- Each epoch contains a clock time.

## Variable description

Each epoch-by-epoch file contains 19 variables. The meanings of these variables are as follows:

| Name          | Label                       | Units / Categories                          |
| ------------- | --------------------------- | ------------------------------------------- |
| `pid`         | Random BioLINCC ID for LAD  |                                             |
| `sawa2`       | Contact Occasion (1 or 2)   |                                             |
| `line`        | Epoch line number           |                                             |
| `offwrist`    | Off wrist indicator         | 0 = On wrist / 1 = Off wrist                |
| `activity`    | Activity count              |                                             |
| `marker`      | Event marker indicator      | 0 = Marker not pressed / 1 = Marker pressed |
| `whitelight`  | White light                 | Lux                                         |
| `redlight`    | Red light                   | Microwatts per square centimeter            |
| `greenlight`  | Green light                 | Microwatts per square centimeter            |
| `bluelight`   | Blue light                  | Microwatts per square centimeter            |
| `wake`        | Awake indicator<sup>*</sup> | 0 = Asleep / 1 = Awake                      |
| `interval`    | Interval type<sup>*</sup>   |                                             |
| `starth`      | Start hour of recording     | *Administrative variable*                   |
| `day`         | Incrementing day indicator  |                                             |
| `dayofweek`   | Day of the week             | 1 = Sunday / 2 = Monday / etc.              |
| `validday`    | Valid day indicator         | *Administrative variable*                   |
| `time`        | Clock time                  | HH:MM:SS                                    |
| `date_shifted`      | Shifted calendar date 			        | Aligned to same day of week as original date|
| `actigraphy_month_start`| Start month of actigraphy recording| 1 = January / 2 = February / etc.        |


<sup>* The wake/sleep detection algorithm runs across the entire recording, though sleep in ACTIVE intervals is never counted toward overall sleep totals. Actual sleep is tallied within REST intervals only. REST-S intervals indicate the period between sleep onset and offset.

## References

- [Patel, S. R., Weng, J., Rueschman, M., Dudley, K. A., Loredo, J. S., Mossavar-Rahmani, Y., Ramirez, M., Ramos, A. R., Reid, K., Seiger, A. N., Sotres-Alvarez, D., Zee, P. C., & Wang, R. (2015). Reproducibility of a Standardized Actigraphy Scoring Algorithm for Sleep in a US Hispanic/Latino Population. Sleep, 9, 1497–1503.](https://www.ncbi.nlm.nih.gov/pubmed/25845697)

## History / changelog

*July 2025*
- Add new `date_shifted` and `actigraphy_month_start` variables

*September 2016*
- Upload actigraphy epoch-by-epoch data to sleepdata.org

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
