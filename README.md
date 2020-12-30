# her6noise
This is custom MATLAB software for timeseries analysis used in Soto & Biga et al. (2020) EMBO Journal.

The analysis of periodicity is adapted from Phillips et al. (2017) PLOS Comp Biol. Users can find the orginal
version at https://github.com/ManchesterBioinference/GPosc. The code uses the GPML toolbox by Rassmusen and Hannes.
For any use of these routines please include the citations as well as follow any further guidance defined for GPosc.

An important modification of the GOPosc pipeline include the background normalisation pre-processing step. This is
done by dividing Venus::Her6 fluorescence by mKeima-H2B nuclear fluorescence for each track (corresponding to a single
cell) at each available timepoint. Another main modification is the use of a prior for the oscillatory lengthscale. 
This improves log-likelihood and aides in the selection of the correct model (periodic or aperiodic) as described in
the Methods @ Soto & Biga 2020. Further other modifications were made to account for particular requirements of the data
such as the use of pairwise CTRL and mBSM (mutant) datasets. 

Before running the code please download the customised GPML toolbox version shared at 
https://github.com/ManchesterBioinference/GPosc/tree/master/General-tool/GPML.zip and make sure that an unarchived copy of
this is located in the same directory as the periodicity routines. Full use of GPML requires running the startup.m routine which has
been included in the custom code for convenience. Following this simply run main_periodicity.m.

No issues were observed when using different MATLAB versions and the code has been tested on R2019a. 



