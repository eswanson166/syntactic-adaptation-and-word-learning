# Syntactic adaptation and word learning

This project presents materials and results for three experiments examining how syntactic adaptation supports children's word learning. The materials for this project are broken down into three sections: 1) experiments, 2) analysis, and 3) writing.

## Experiments

The experiments section contains all the materials needed for locally running the three main experiments, as well as the three norming experiments that were carried out when selecting stimuli.

For each experiment (including each norming experiment), there are four primary components:
- JS (code to run the experiment itself)
- CSS (code related to web styling)
- HTML (web version of the experiment)
- static/audio/images (audio and image files used in the experiment)

For Experiment 3, because the study was run on Lookit, an HTML version of the experiment is not available. However, the experiment is essentially identical to Experiment 2. You can contact Elizabeth Swanson (eswanson166@gmail.com) if you wish to view Experiment 3 on Lookit, which will require you to create your own Lookit account.

## Analysis

The analysis section contains the results of the three main experiments, as well as the three norming experiments. Each analysis section is broken down into three parts (data, graphs, and scripts):

### Data

For the norming experiments, this folder consists of each participant's individual CSV file.

For Experiments 1 and 2, there are two zip files: one containing a folder with each participant's raw data, and one containing a clean data CSV file (the output of running the data_cleaning.Rmd script). The clean data is ready to be run through the visualization and analysis scripts. NOTE: The zip files with the data must be unzipped before the R scripts can be run.

For Experiment 3, because the study involved hand-coding children's looks, there are five data files:
- The "What's a moop" JSON file contains the raw individual participant data collected from Lookit. This includes information about the timing of events in the study, what condition the child was in, etc.
- A folder containing the raw datavyu video codes for each child (the result of watching each child's video and hand-coding the direction of their eye movements)
- The preprocessed Lookit data, the result of running the "preprocess-lookit-json.Rmd" script on the "What's a moop" JSON file
- The full test data, the result of running the "datavyu-processing.Rmd" script, which combines the datavyu video codes with the Lookit data
- The full test data for analysis, which is compiled by the "data_visualization.Rmd" script and is ready to be used in the "data_analysis.Rmd" script

### Graphs

For each experiment, this folder contains all the graphs generated by the visualization scripts.

### Scripts

Most experiments have R markdown scripts that are broken down into data cleaning, data visualization, and data analysis. NOTE: make sure to unzip any zip files in the Data folder before running the scripts. Also, set your working directory to "Source File Location" for each script.

Experiments 1 and 2, and the norming experiments, also use a Python script called "process_raw_data.py" which processes the raw participant data collected by the web experiments. It transfers the raw data from .txt files to CSV files. The .txt files are not included here because they contained identifying information, but the anonymized CSV files are contained in the raw_data.zip folder in the Data section. 

Experiment 3 has additional scripts for processing Lookit data and Datavyu data. To duplicate the full analysis pipeline, they should be run in this order (though the output files for each are saved, so it is possible to skip straight to any script):
- Preprocess Lookit JSON
- Datavyu processing
- Visualization
- Analysis

All experiments also use a "helpers.R" script, which defines some common functions, such as calculating confidence intervals.

## Writing

Currently, this folder contains a write-up of Experiment 1 (a direct replication of Havron et al.) and a full report on all 3 experiments (Syntactic Adaptation and Word Learning).

