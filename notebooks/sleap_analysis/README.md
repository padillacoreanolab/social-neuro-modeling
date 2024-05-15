# SLEAP Notebooks Documentation

This repository contains two Jupyter notebooks that utilize SLEAP, a machine learning tool for pose estimation in video data, to analyze animal behavior in experimental settings.

## Notebooks

### 1. SLEAP Processing

This notebook is designed for processing and analyzing pose estimation data using the SLEAP framework. It focuses on refining raw pose data, computing specific metrics, and preparing the data for detailed behavioral analysis.

#### Features:
- Data loading and preprocessing.
- Integration of video and pose estimation data.
- Calculation of velocity and other motion-related metrics.
- Visualization of pose tracking data.

#### Usage:
This notebook is intended for users with intermediate knowledge of Python and data analysis, specifically in the context of behavioral studies using video tracking. Users should customize the input paths and parameters according to their experimental setup.

### 2. SLEAP Distance Calculation

Focused on calculating distances and velocities from pose estimation data, this notebook provides tools for quantitative analysis of movement dynamics in experimental animal studies.

#### Features:
- Calculation of velocities using smoothed pose data.
- Measurement of distances between tracked nodes and specific points (e.g., reward locations).
- Conversion of pixel measurements to real-world units (e.g., centimeters).
- Generation of detailed plots to visualize movements and interactions.

#### Usage:
This notebook is suitable for users who need to perform detailed motion analysis from video tracking data. It requires a setup of SLEAP outputs and configuration for the specific experimental recordings being analyzed.

## Installation

Before running these notebooks, ensure you have the following installed:
- Python 3.6+
- Jupyter Notebook or JupyterLab
- Required Python packages: `numpy`, `pandas`, `matplotlib`, `scipy`, `h5py`
- SLEAP installed and properly configured to process your video data.

## Running the Notebooks

1. Clone this repository to your local machine or download the notebooks directly.
2. Install the necessary Python packages following the commands in: `social-neuro-modeling/bin/spike_interface_0_99_0.sh`
3. Open the notebooks in Jupyter Notebook or JupyterLab.
4. Update the paths and parameters in the cells to match your data and configuration.
5. Run the cells sequentially from top to bottom to process your data and view the results.