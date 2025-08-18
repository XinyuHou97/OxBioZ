# OxBioZ Dataset: Multi-Activity Dataset with Bioimpedance, Physiological, and Motion Signals

This dataset contains about 1000 min of trunk bio-impedance
together with various physiological and motion
signals of 21 subjects performing a range of different daily
activities.

## Data Structure

All data is stored in two hierarchical HDF5 files:
* `OxBioZ_gel_electrodes.hdf5` contains data from 20 subjects wearing gel electrodes.
* `OxBioZ_fabric_electrodes.hdf5` contains data from one subject wearing fabric electrodes.

## Subjects/Participants

The table below provides overall statistics of the 20 participant's physical characteristics and
perceived functional ability (PFA) and physical activity
rating (PAR). PFA and PAR are two popular scores based
on questionnaires that estimate physical activity capability.
The subject wearing fabric electrodes is excluded.

| **Characteristic**                   | **Value**         |
|--------------------------------------|-------------------|
| Age [yr]                             | 29.00 ± 5.74      |
| Height [cm]                          | 170.30 ± 9.38     |
| Weight [kg]                          | 66.09 ± 12.07     |
| Lower chest circumference [cm]       | 79.55 ± 9.17      |
| Waist circumference [cm]             | 74.65 ± 9.69      |
| PFA1                                 | 8.10 ± 2.75       |
| PFA2                                 | 6.65 ± 2.52       |
| PAR                                  | 5.35 ± 2.35       |
| Gender ratio (male:female)           | 12:8              |

## Devices

The table below lists the employed data collection devices.
For details about the OxBioZ device, please refer to our paper.

| **Sensor type** | **Sensor model**                | **Frequency**| **Data**                                 |
|-----------------|---------------------------------|--------------|------------------------------------------|
| BioZ AFE        | OxBioZ                          | 200 Hz       | Bioimpedance resistance                  |
|                 |                                 |              | Bioimpedance reactance                   |
| Spirometer      | Go Direct Spirometer, Vernier   | 50 Hz        | Flow Rate                                |
|                 |                                 |              | Volume                                   |
|                 |                                 |              | Adjusted volume                          |
|                 |                                 |              | Cycle volume                             |
|                 |                                 |              | Respiration rate                         |
|                 |                                 |              | Differential pressure                    |
| IMU             | Arduino Nano 33 BLE Sense, Arduino | 60 Hz     | 3-axis acceleration                      |
|                 |                                 |              | 3-axis angular velocity                  |
| Oximeter        | Apple Watch                     | 0.2 Hz       | Heart rate                               |
| BCA             | mBCA 525, Seca                  | -            | Total body water (TBW)                   |
|                 |                                 |              | Extra cellular water (ECW)               |
|                 |                                 |              | Fat / muscle mass, etc.                  |
| ECG             | Heal Force ECG Monitor          | -            | 3-lead ECG signal                        |

## Data Collection Protocoll

| **Period**     | **Time** | **Device**                                      | **Description**                                                                                                                                                                                           |
| -------------- | -------- | ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Measure 1    | –        | BCA <br> BioZ AFE                               | Measure body composition with BCA.<br>Measure MF-BIA with BioZ AFE at 12 frequencies <br>(F_I=819200, 409600, 204800, 102400, 51200, 25600, 12800, 6400, 3200, 1600, 800, 40 Hz).<br>Measure weight. |
| Short test 1 | 5 min    | BioZ AFE <br> IMU <br> Oximeter <br> Spirometer | Five 1-min activities:<br>lying, sitting, standing, walking, running.<br>BioZ AFE collects in single-frequency mode.<br>SF-BIA: I=32.00  μA (RMS), F_I=51200 Hz.                                 |
| Long test 1  | 20 min   | BioZ AFE <br> IMU <br> Oximeter                 | 0–3 min: warm-up (walk 6 km/h).<br>3–17 min: walk/jog/run at set speed.<br>17–20 min: cool-down (reduce speed).<br>Record Borg Rated Perceived Exertion (RPE) score.                                      |
| Measure 2    | –        | -                                               | Same as Measure 1                                                                                                                                                                                         |
| Long test 2  | 20 min   | -                                               | Same as Long test 1                                                                                                                                                                                       |
| Short test 2 | 5 min    | -                                               | Same as Short test 1                                                                                                                                                                                      |
| Measure 3    | –        | -                                               | Same as Measure 1                                                                                                                                                                                         |

## Footnote

This research has been approved by the Research
Ethics Committee of the Department of Computer Science
of the University of Oxford.
