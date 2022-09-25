# Code description
## UMAT_optimization_public/
  1. UMAT_U2_OPTIMIZATION/
        - STEP1_dataProcessing_cross_loading.m 
        > This matlab script pre-process the experimental data in terms of Effective plastic strain and true stress.

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
