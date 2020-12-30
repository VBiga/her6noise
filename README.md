# her6noise
This is custom MATLAB software for timeseries analysis used in Soto & Biga et al. (2020) EMBO Journal.

The analysis of periodicity is adapted from Phillips et al. (2017) PLOS Comp Biol. Users can find the orginal
version at https://github.com/ManchesterBioinference/GPosc. The code uses the GPML toolbox by Rassmusen and Hannes.
For any use of these routines please include the citations as well as follow any further guidance defined for GPosc.

An important modification of the GPosc pipeline include the background normalisation pre-processing step. This is
done by dividing Venus::Her6 fluorescence by mKeima-H2B nuclear fluorescence for each track (corresponding to a single
cell) at each available timepoint. Another main modification is the use of a prior for the oscillatory lengthscale. 
This improves log-likelihood and aides in the selection of the correct model (periodic or aperiodic) as described in
the Methods @ Soto & Biga et al. Further other modifications were made to account for particular requirements of the data
such as the use of pairwise CTRL and mBSM (mutant) datasets. 

To run the routines download the folder named GP Periodicity and unarchive it. You will also need to
download the customised GPML toolbox version shared at https://github.com/ManchesterBioinference/GPosc/tree/master/General-tool/GPML.zip 
and make sure that an unarchived copy of GPML (as a folder) is located in the same directory as the periodicity routines. Full use of GPML requires running the startup.m routine which hasbeen included in the custom code for convenience. All that is left is to run main_periodicity.m.

No issues were observed when using different MATLAB versions and the code has been tested on R2019a. 



