# adaptive-decline

Instructions for navigating the code for the article "Prudent predators: How does landscape structure influence adaptive decline?"

Authors: Leithen K M'Gonigle, Emma L Green, Philip B Greenspoon
Corresponding author e-mail: lmgonigl@sfu.ca.

This code is used to simulate data for the named article. All code is written in R (V4.4.2).

The src folder contains the functions that form the backbone of simulation and does not need to be accessed directly. The script run_dynamics.R will source the files in src, provided working directories are changed accordingly. The remainder of the script will then run two iterations of the model (one for a single patch and one for 200 patches) and then generate Fig. 2 from the manuscript (showing model dynamics for these two runs).

The core "biology" of the model can be found in src/population.R.

A full list of model parameters and default values can be found in prms.R. These can be changed or modified by adding additional lines in the call to the base.prms() function, as we do in run_dynamics.R. For example, one could change d.1 to 0.7 (instead of the default value of 0.5) by adding 'd.1=0.7' as an argument in the call to base.prms.
