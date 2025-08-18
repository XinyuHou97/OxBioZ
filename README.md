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

## Footnote

This research has been approved by the Research
Ethics Committee of the Department of Computer Science
of the University of Oxford.
