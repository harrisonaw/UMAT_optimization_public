# Code description
## UMAT_U2_OPTIMIZATION/
### Code
  1. STEP1_dataProcessing_cross_loading.m <br />
  `This matlab script pre-process the experimental data in terms of Effective plastic strain and true stress.`
        - /Data/EDDQ-TDT-RD45T.csv to /Data/Output/EDDQ-TDT-RD45T.mat <br />
        `Stress-strain data for cross loading. 1st load = direction for pre-strain. 2nd load = direction for second-loading.`
  2. STEP1_dataProcessing_cyclic_loading.m <br />
  `This matlab script process the anisotropy of a material in terms of (1) Normlaized flow stress and (2) R-value`
        - /Data/AA6022_EXP_9CYCLE.csv to /Data/Output/AA6022_EXP_9CYCLE.mat <br />
        `Stress-strain data for cross loading. 1st load = direction for pre-strain. 2nd load = direction for second-loading.`
  3. STEP1_dataProcessing_YLD.m <br />
    `This matlab script pre-process the experimental data in terms of Effective plastic strain and true stress.`
        - /Data/AA2090_DATA.csv to /Data/Output/AA20290_DATA.mat
        `Angle (+ biaxial angle), Normalized flow stress, and R-Value for 2090 test`
  4. STEP2_Identification_YLD.m <br />
  ``

# UMAT_OPTIMIZATION
The optimization code for
  1. Anisotropic Yield function
        - Hill 1948
        - Yld2000-2d
        - Yld2004-18p
        + Any other anisotropic yield function
  2. Anisotropic Hardening models
        - Chaboche-type
        - Yoshida-Uemori
        - HAH11 / HAH14 / HAH20 / HEXAH (HAH22)
        + Any other anisotropic hardening models
  3. Dislocation hardening model
        - RGBV (K. Kitayama et al.)

# Available deformation mode
  1. Uniaxial tension
  2. Forward-reverse loading
  3. Cross-loading
  
# Optimization algorithm
  1. Nelder-Mead
  2. Genetic algorithm (Multi processor)
  3. Pattern search (Multi processor)
  4. Global search

# Prerequisites
  1. MATLAB
  2. Optimization toolbox
  3. Global optimization toolbox
  4. MATLAB-Mex

# Note
  1. The optimized model coefficients will be written in the form of material property file with the name of ***'PROPS_FINAL.CSV'***
  2. Step1: Experiment data pre-processing: This must be done before starting the optimization code
  3. Step2: Optimization code: you can select proper reference deformation modes.
  
# Screeshots
1. Anisotropic yield function
<p align="center"><img src="https://github.com/theysy/UMAT_OPTIMIZATION_PUBLIC/blob/main/Screenshots/AA2090_YLD2004_OPT.png"></p>

2. Anisotropic hardening model: Cyclic loading
<p align="center"><img src="https://github.com/theysy/UMAT_OPTIMIZATION_PUBLIC/blob/main/Screenshots/HAH20_CYCLIC_OPT.png"></p>

3. Anisotropic hardening model: Cross loading
<p align="center"><img src="https://github.com/theysy/UMAT_OPTIMIZATION_PUBLIC/blob/main/Screenshots/HAH20_CROSS_OPT.png"></p>
