# Baseball Swing - Training Conditions
A repository of the data from the pitch modality study used for my thesis work. 

To read my thesis, visit my [LinkedIn profile](https://www.linkedin.com/in/devin-thompson-180198b7/) or ProQuest: 

Thompson, D. J. (2022). Kinematic Differences Between Baseball Batting Training Conditions in Collegiate Players Using Statistical Parametric Mapping: A Preliminary Study [M.S., Washington State University]. In ProQuest Dissertations and Theses. https://www.proquest.com/docview/2836737489/abstract/EEBFE22334524870PQ/1


It contains more information on methodology and details the calculations and results.

Trials were collected under four unique training conditions, where the pitch was delivered in a different way. The four conditions include:
1. A tee (Tee)
2. A batting practice pitcher (BP)
3. A robot pitching machine (RPM)
4. A live pitcher (Live)

The following image details the setup:

![SetupFigure](https://github.com/DevinThompson2/BaseballSwingTrainingConditions/assets/53098472/8ef8e4d5-ac12-4657-8139-5696ae9fdd44)

The distances and pitch speeds were chosen so that the amount of time from release to home plate was approximately controlled. All pitches were four-seam fastballs. Data were captured at 500Hz with a 10-camera, Vicon passive IR motion capture system.

## Markerset
![Markerset](https://github.com/DevinThompson2/BaseballSwingTrainingConditions/assets/53098472/d74f8091-b257-4354-af5a-523e9cab6c6f)

LMEP and RMEP are calibration only markers. They exist in the calibration file but not the motion files.

## Global Coordinate System
![ImpactEvent](https://github.com/DevinThompson2/BaseballSwingTrainingConditions/assets/53098472/97334144-4c8e-4173-8894-b4f00e4f0ffc)

The global +y-direction is towards the pitcher, the global +z-direction is vertical, and the +x-direction is the cross product of the y and z directions, using the right-hand rule. This ends up being to the right, when facing the pitcher. 

## Folders
**SwingData:** Contains data folders of various data.
* Data: Contains folders for each hitter. Each hitter's folder contains the calculated metrics for each trial, in a csv format or .mat data type. These are outputs from Visual3D. It also contains anthropometric data and other information on the participants in the `ParticipantList_DeIdentify` file.
* Figures: Contains various figures that care calculated from the `MainProcessing` MATLAB script. Various folders of output data include `Contact Rates`, `Events`,`Max Metrics`, `Pitch Location`,`Signals`, and `Stats`. Each of these folders contains .png and .fig (MATLAB) duplicate types.
* PitchModality: Contains folders for each hitter. Each hitter's folder contains trial and calibration data as c3d files and a labeling vsk file.
* Visual3D: Contains the .cmz and .mdh files of the Visual3D data and models for each player.

**Scripts:** Contains the MATLAB and Visual3D scripts that were used to process the data.
* MATLAB: Various MATLAB scripts and functions to process the Visual3D outputs and perform other pre-processing steps.
  * AddBall: Adds a marker to the calibration file that can be labeled as the ball.
  * MainProcessing: Processes the output .mat files from Visual3D. Generates numerous figures from the data, both continuous and discrete.
  * ReplaceTrajectories: Uses various techniques to estimate the starting position of various markers and insert them, so that they can be gap-filled.
* Visual3D: Scripts to build models and calculate model variables
  * LH: For processing left-handed hitters.
  * RH: For processing right-handed hitters.

  
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
