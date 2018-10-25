# Bayesian Joint Graphical Modeling Approaches for Covariance and Dynamic Functional Connectivity Analysis from Neuro-Imaging Data

## background

* recent renewed interest in graphical models
* recent interest in "dynamic functional connectivity"
* connectivity btwn areas of the brain?

## neuroimaging background

* fMRI's image bloodflow in response to neural activity
* neurons fire, use oxygen? and then blood flows to replenish that oxygen
* can use heirarchical or joint modeling to share graphical structures between
  brains / scans / ...

## contributinos

* gaussian graphical model for understanding functional brain activity
* recently developed prior 
* HMM model applied to 


## project 1 

* data: binary matrix I = k x t indicating binary sensor inputs (sound / no
  sound, light / no light) and fmri scan signal matrix O = M x T indicating
  responses from brain

goal: understand if a particular stimulus triggered a response from a
particular brain region

hemodynamic linear model:
response is inherently delayed - the body can't react instantly, so they 
actually delay the input data to appropriately reflect that (by convolving
poisson density with the raw data)

### jointly modeling the functional networks

"markov random field" prior - prior on the existence of edges in the various
graphs: $E_ij = [e_ij^1, \ldots, e_ij^s]$, $E_ij \sim \text{MRF}(\nu_ij,
\theta_ij)$.

SimTB toolbox used to generate realistic simulated fMRI data.

### results

* sufficient information in how brain regions co-vary to understand what task
  is being performed - the mean is regressed out, we're just considering if
  part A / B are working together or not
* incredibly accuracte state prediction
