# Actigraphy Introduction

The Sueno Ancillary study recruited 2,252 HCHS/SOL participants to wear wrist-worn actigraphy devices ([Actiwatch Spectrum, Philips Respironics](http://www.usa.philips.com/healthcare/product/HC1046964/actiwatch-spectrum-activity-monitor)) between 2010 and 2013. Participants were instructed to wear the watch for a week. Records were scored by a trained technician at the Boston Sleep Reading Center.

The [documentation folder](:files_path:/documentation) contains manuals and in-depth descriptions of the actigraphy devices and scoring process used in the Sueno Ancillary study. Further, the [`hchs-sol-sueno-ancillary` dataset](:files_path:/datasets) contains summary phenotype data from the actigraphy data collection.

## Epoch-by-epoch Files

[Epoch-by-epoch (EBE) data files (CSV))](:files_path:/actigraphy) have been created for 1,887 participants with actigraphy data whose HCHS/SOL data are available for public use. Each row in these files represents 30 seconds worth of summary data from the actigraphy device. Based upon the Sueno actigraphy scoring, invalid (low quality) days were removed from these files. A day was marked invalid if 1) there were 4 or more hours of offwrist/invalid time or 2) the main sleep period contained offwrist/invalid time.

Notes:

- The Sueno Ancillary study used actigraphy primarily as a means to estimate sleep and wake times, **not** as a means to assess physical activity.
- The `day` indicator in the file runs from noon-to-noon (i.e. not midnight-to-midnight) because the goal was to have each individual day in the file wholly contain a singular main sleep period.
- Dates have been removed from the file. Each epoch contains a clock time.

## Variable Description

Each epoch-by-epoch file contains 17 variables. The meanings of these variables are as follows:

| Name          | Label                       | Units / Categories                          |
| ------------- | --------------------------- | ------------------------------------------- |
| `pid`         | Random BioLINCC ID for LAD  |                                             |
| `sawa2`       | Contact Occasion (1 or 2)   |                                             |
| `line`        | Contact Occasion (1 or 2)   |                                             |
| `offwrist`    | Off wrist indicator         | 0 = On wrist | 1 = Off wrist                |
| `activity`    | Activity count              |                                             |
| `marker`      | Event marker indicator      | 0 = Marker not pressed | 1 = Marker pressed |
| `whitelight`  | White light                 | Lux                                         |
| `redlight`    | Red light                   | Microwatts per square centimeter            |
| `greenlight`  | Green light                 | Microwatts per square centimeter            |
| `bluelight`   | Blue light                  | Microwatts per square centimeter            |
| `wake`        | Awake indicator             | 0 = Asleep | 1 = Awake                      |
| `interval`    | Interval type               |                                             |
| `starth`      | Start hour of recording     |                                             |
| `day`         | Incrementing day indicator  |                                             |
| `dayofweek`   | Day of the week             | 1 = Sunday | 2 = Monday | etc.              |
| `validday`    | Valid day indicator         | 0 = Valid day | 1 = Invalid Day             |
| `time`        | Clock time                  | HH:MM:SS                                    |


1. `pid` Random BioLINCC ID for LAD
2. `sawa2` Contact Occasion (1 or 2)
3. `line`
4. `offwrist`
5. `activity`
6. `marker`
7. `whitelight`
8. `redlight`
9. `greenlight`
10. `bluelight`
11. `wake`
12. `interval`
13. `starth`
14. `day`
15. `dayofweek`
16. `validday`
17. `time`
