# M1M3_ML
LSST M1M3 optical analyses for tests at UofA Mirror Lab

The repo contains the analyses performed with data we took at the UofA Mirror Lab. These are mostly documented with Jupyter notebooks, which uses Python 3 and other standard Python libraries.

To execute these notebooks require data from two sources.
* a data package (~50GB) that was delivered to LSST by the Mirror Lab 
* a EFD database (~20T) that contains all the telemetry data published by the mirror control software. At this time, there is no plan to make these publicly available. The notebooks are therefore saved with all the plots and outputs.

The test plan, with follow-up information on when and how each section was executed during the test campaigns, are found as LSST document-xxxxx.

A summary of what tests have been performed for each of the major tasks can be found in summary_by_task.txt in the repo.

Here is a detailed description of the content of this repo:

Filename | Description
------- |---------------------------
190114.ipynb, 190115.ipynb, 190116.ipynb, 190117.ipynb, 190118.ipynb, 190122.ipynb, 190124.ipynb, 190125.ipynb, 190211.ipynb, 190212.ipynb, 190213.ipynb, 190214.ipynb, 190215.ipynb, 190218.ipynb, 190219.ipynb, 190220.ipynb, 190221.ipynb | A day-by-day description of what was done, and what results were obtained
FATABLE.py | Some parameters for the mirror and cell, and basic functions by the control system
FB_diagnostics.ipynb | A demostration of how the Force Balance system works
M1M3tools.py | Some common tools used by the notebooks 
M_HP.ipynb | A demostration of how the Hard Point Matrix is calculated
checkTfromEFD.ipynb | To check temperature spatial distribution and time variation
finalBendingModes.ipynb | Calculation of the final bending modes to go onsky with M1M3 
finalLUT.ipynb | Calculation of the zenith optimized forces to go onsky with M1M3
getVdayForces_190214.ipynb | A look at the optimized force set used on 190214
get_Fxyz_from_EFD_190125.ipynb | A look at the optimized force set used on 190125. A demostration of how to get forces from the EFD, and the various components of the forces
sec3.2InitialForces.ipynb | Calculation of the initial force set used during campaign 1 (did not correctly account for dual-axis actuator weights)
sec3.3_initialOptimization.ipynb | An example of looking at results from surface optimization (put together in real time)
sec3.7bendingModesStress.ipynb | A look at the stress on the glass produced by individual bending modes
sec3.8_SingleActuator.ipynb | A notebook used during testing for prioritizing the single actuator influence function measurements
sec4.3InitialForces.ipynb | Calculation of the initial force set used during campaign 2 (correctly accounted for dual-axis actuator weights)
summary_by_task.txt | A summary of what tests have been performed for each of the major tasks
data/LSST_BM_scale.txt | LSST bending modes scaling factors (need to be multiplied with FEA mode shapes)
data/M1M3_1um_156_force.txt | Calibrated force sets that produce 1 micron RMS of LSST bending modes
data/M1M3_1um_156_grid.txt | LSST bending mode shapes
data/MHP.txt | LSST M1M3 Hard Points Matrix
data/ML_BM_XTalk.txt | Mirror Lab bending modes cross-talk
data/ML_BM_scale.txt | Mirror Lab bending modes scaling factors (need to be multiplied with FEA mode shapes)
data/ML_IF_scale.txt | Mirror Lab influence function scaling factors (need to be multiplied with FEA influence functions)
data/finalLUT.csv | Zenith-pointing optimized forces to go onsky with M1M3
data/forces_190125_Chris.csv | Force set that produced the optimized surface on 190125, as from the control system, and provided by Chris
data/myUdn3norm_156.mat | LSST FEA bending modes and forces. This is a Matlab mat file, but can be read-in using Python.
data/sec4.3Forces.csv | Initial force set used during campaign 2 (correctly accounted for dual-axis actuator weights)

Other related Documents:
---
* data analysis plan presented at readiness review
* data processing precedure description
* M1M3 performance analysis at mirror acceptance
* FEA bending mode calculation procedure
* initial force calculation
* load spreader moments
* force offset measurements on spare actuators
* structure function results
* horizon test force determination
* horizon test optimization results
* bending mode 27

To-do List:
---
* re-fit LSST bending modes. update cross-talk matrix. update finalBendingModes.ipynb.
* Repeat all Mirror Lab fits.
* check T: EFD against Mirror Lab log
* The surface RMS values in the data are not consistent with what they quoted during testing. Are we looking at the right data files?

