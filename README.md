# Weibull-Hawkes Model

Chapter 2 of thesis formulates the model and its two versions (single and mixture Weibull) and presents simulation study and case study results. Chapter 4 explores Goodness of Fit tests. 

## Cues

Contains files relating to the fitting of the whale cue data.  

Included are the results, both frequentist and Bayesian, for the whale introduced in Section 2.4. However the cue data itself is not public.


Bayesian.R: code to run Markov Chain Monte Carlo (MCMC) chain in the R package NIMBLE. Fits cue data to first model.<br />

Bayesian-Mixture.R: as above but for the second, mixture model.<br />

Frequentist.R and Frequentist-Mixture: code to fit cue data by MLE with the R package TMB.<br />

whales\_cues.cpp and whales\_cues\_mix.cpp: TMB C++ templates that calculate the likelihood of each model, with baseline given by Equation 2.9.<br />



## Figures

 

Contains plots of the simulation study results

 

WIHP-\<param\>byK.jpeg: Histograms of the bias in \<param\> grouped by the true value of k for the first simulation study.<br />

MWIHP-\<param\>byK1.jpeg: Histograms of the bias in \<param\> grouped by the true value of k<sub>1</sub> for the second simulation study.<br />

MWIHP-K2byK2.jpeg: Histograms of the bias in k<sub>2</sub> grouped by the true value of k<sub>2</sub> for the second simulation study.<br />

 

 

## SimResults

 

Contains the raw results of the two simulation studies, being the matrix output from WIHPsimulations.R and MWIHPsimulations.R

 

WIHPsims\_i\_.csv (where i = 1:64) contain simulation results for the first simulation study.<br />

MWIHPsims\_i\_.csv (where i = 1:192) contain simulation results for the second simulation study.<br /> 


 

## Simulations

 

Contains files for running the two simulation studies.

 

WIHPsimulations.R: simulates the first model with a single Weibull.<br />

MWIHPsimulations.R: simulates the mixture model.<br />

Simulate.R: contains functions called by the three above R scripts that implement the algorithms described in Appendix A.3. 

weibull\_hawkes\_inhomog.cpp and mix\_weibull\_hawkes\_inhomog.cpp: TMB templates with the baseline function used in the simulation studies.<br /> 