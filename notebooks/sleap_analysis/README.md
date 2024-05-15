# Reward Competition SLEAP Analysis

## Steps to start

0. Create/activate Conda environment that contains:
    - `git` 
        - https://anaconda.org/conda-forge/gitpython/
    - `numpy`
    - `pandas`
    - `matplotlib`
    - `scipy`
    - `h5py`
        - https://anaconda.org/anaconda/h5py

- Or create Conda environment with commands from: `social-neuro-modeling/bin/spike_interface_0_99_0.sh`
1. Download data from link into `data` directory: https://www.dropbox.com/scl/fo/bmfkb19mz6fciz35vskri/AN-uWgAHIYxknDEA8XZghkI?rlkey=0osqf1zvruv5lony5zsk447ua&st=cgh6tgdh&dl=0
2. Run `./01_rce2_add_sleap_pose_estimation.ipynb` notebook
3. Run `./02_rce2_processing_sleap.ipynb` notebook

## Dependencies
- Python libraries: `os`, `glob`, `git`, `sys`, `numpy`, `pandas`, `matplotlib`, `scipy`, `h5py`
- SLEAP software for pose data processing

# Notebook 01: SLEAP Distance Calculation

## Overview
This notebook calculates distances in animal behavior studies using SLEAP pose estimation data. It computes velocities and analyzes distances between tracked nodes and specific points of interest.

## Structure
- **Imports**: Setup of libraries and path configurations.
- **Data Loading**: Configuration and loading of video and pose data.
- **Data Processing**: Calculations of velocity and distance measurements.
- **Outputs**: Generation of plots and data files for further analysis.

## Usage
1. Configure the environment and ensure all dependencies are installed.
2. Modify paths and parameters as per your data setup.
3. Run the notebook cells sequentially to perform data processing and generate outputs.

## Inputs
- SLEAP pose data files detailing positions

## Outputs
- Visualizations of movement velocities and distances.
- Data files with computed metrics, ready for further analysis or reporting.


# Notebook 02: SLEAP Processing

## Overview
This notebook further processes the output from the previous notebook by removing unnecessary data and includes demonstrations of example analysis.

## Structure
1. **Setup**: Configure paths and import necessary libraries.
2. **Data Loading**: Load video data and associated metadata for analysis.
3. **Data Processing**: Apply pose estimation and clean the data for further analysis.
4. **Data Analysis**: Conduct exploratory data analysis and compute statistical metrics.
5. **Output**: Save the processed data and generate visualizations.

## Usage
1. Configure the environment and ensure all dependencies are installed.
2. Modify paths and parameters as per your data setup.
3. Run the notebook cells sequentially to perform data processing and generate outputs.

## Inputs
- Output from `./01_rce2_add_sleap_pose_estimation.ipynb` notebook

## Outputs
- Processed data frames and visual plots of analyzed data.

# Description of columns in output

- File metadata and information
```
# Name of SLEAP file
sleap_name
# File path of session directory
session_path
# Name of the recording
recording
# Cohort number
cohort
# Type of experiment
experiment
# File name of video
video_name
# Box number of the recording
box_number
# Name of session directory that the recording is a part of 
session_dir
```
- Subject info
```
current_subject
tracked_subject
all_subjects
subject
agent
```
- Timestamps
```
first_timestamp
last_timestamp
video_timestamps
tone_timestamps
lfp_timestamps
```
- Descriptions of each trial
```
# Origiinal trial labels
condition
# How competitive the trial was
competition_closeness
# Notes on the trial
notes
# The trial label(ie win vs lose)
trial_label
```
- The start and stop frame/timestamps of trials
    ```
    tone_start_frame
    reward_start_frame
    tone_stop_frame
    tone_start_timestamp
    tone_stop_timestamp
    ```
- The frame and timestamp at which port entries were made
```
box_1_port_entry_frames
box_2_port_entry_frames
box_1_port_entry_timestamps
box_2_port_entry_timestamps
```
- LFP Traces
```
mPFC_lfp_trace
MD_lfp_trace
LH_lfp_trace
BLA_lfp_trace
vHPC_lfp_trace
```
- The subjects that are in the video
```
in_video_subjects
```
- list of body parts tracked
```
body_parts
```
- Coordinatres of the corners of the operant chamber
```
box_top_left
box_top_right
reward_port
box_bottom_left
box_bottom_right
```
- SLEAP Output
```
# Coordinates of all the body parts
subject_locations
agent_locations
# Velocity of thorax
subject_thorax_velocity
agent_thorax_velocity
# Distance of thorax to reward port
subject_thorax_to_reward_port
agent_thorax_to_reward_port
```
- The first and last frame of when the subject is in the video
```
start_stop_frame
start_stop_timestamps
```
- Mask used to filter for tones that correspond to trials that are actually in the recording/
```
tone_mask
```