# BaseballSwingTrainingConditions
A repository of the data from the pitch modality study used for my thesis work. 

To read my thesis, visit my LinkedIn profile: https://www.linkedin.com/in/devin-thompson-180198b7/

It contains more information on methodology and details the calculations and results.

Trials were collected under four unique training conditions, where the pitch was delivered in a different way. The four conditions include:
1. A tee (Tee)
2. A batting practice pitcher (BP)
3. A robot pitching machine (RPM)
4. A live pitcher (Live)

The following image details the setup:

![SetupFigure](https://github.com/DevinThompson2/BaseballSwingTrainingConditions/assets/53098472/8686258c-6baa-411b-b3f9-ffaade7b2c3b)

The distances and pitch speeds were chosen so that the amount of time from release to home plate was approximately controlled. All pitches were four-seam fastballs.

## Markerset
![Markerset](https://github.com/DevinThompson2/BaseballSwingTrainingConditions/assets/53098472/0decf81d-ef2c-4821-bef5-62ac6b6b8bcb)

LMEP and RMEP are calibration only markers. They exist in the calibration file but not the motion files.

## Folders
SwingData: Contains data folders of various data
* C3D: Contains folders for each hitter. Each hitter's folder contains trial data as c3d files and a labeling vsk file.
* Metrics: Contains the calculated metrics for each trial, in a csv format or .mat data type
* Visual3D: Contains the .cmz and .mdh files of the Visual3D data and models for each player
  
## C3D Info
A common naming convention was followed. The four pitching conditions used were `Tee`, `BP`, `Cannon` (which is the RPM), and `Live`. They follow the following structure:

`ParticipantID PitchingCondition TrialNumber`

`ParticipantID` = the unique participant ID
`PitchingCondition` = the pitching condition that the trial was collecte under
`TrialNumber` = the trial number for that participant's pitching condition

Examples:
* Subject4 Tee 01
* Subject6 Cannon 12
* Subject10 BP 05

When the `PitchingCondition` is `Cal`, this indicates that it is the static calibration file.

## Metrics Info


## Visual3D Info
