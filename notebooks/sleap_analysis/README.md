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

# Notebook 01: SLEAP Distance Calculation

## Overview
This notebook calculates distances in animal behavior studies using SLEAP pose estimation data. It computes velocities and analyzes distances between tracked nodes and specific points of interest.

## Dependencies
- Python libraries: `os`, `glob`, `git`, `sys`, `numpy`, `pandas`, `matplotlib`, `scipy`, `h5py`
- SLEAP software for pose data processing

## Structure
- **Imports**: Setup of libraries and path configurations.
- **Function Definitions**: Includes `compute_velocity`, averaging functions, and window index calculations.
- **Data Loading**: Configuration and loading of video and pose data.
- **Data Processing**: Calculations of velocity and distance measurements.
- **Outputs**: Generation of plots and data files for further analysis.

## Usage
1. Configure the environment and ensure all dependencies are installed.
2. Modify paths and parameters as per your data setup.
3. Run the notebook cells sequentially to perform data processing and generate outputs.

## Inputs
- SLEAP pose data files detailing positions and identities in experimental setups.

## Outputs
- Visualizations of movement velocities and distances.
- Data files with computed metrics, ready for further analysis or reporting.

# Notebook 02: SLEAP Processing

## Overview
This Jupyter notebook is dedicated to processing animal behavior video data through SLEAP for pose estimation and subsequent data aggregation and analysis. It includes detailed steps from setting up the environment to processing and visualizing data.

## Usage
1. **Setup**: Configure paths and import necessary libraries.
2. **Data Loading**: Load video data and associated metadata for analysis.
3. **Data Processing**: Apply pose estimation and clean the data for further analysis.
4. **Data Analysis**: Conduct exploratory data analysis and compute statistical metrics.
5. **Output**: Save the processed data and generate visualizations.

## Functions Defined
- `mask_slices`: Masks portions of arrays.
- `overlay_arrays`: Overlays two arrays based on NaN values.
- Additional utility functions for data manipulation and analysis.

## Inputs
- Video files and metadata in specified formats.

## Outputs
- Processed data frames and visual plots of analyzed data.

## Data Structure
Data should include video files and metadata necessary for pose estimation and behavior analysis.