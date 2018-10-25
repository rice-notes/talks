# Stochastic Geometry and Wireless Network Modeling

* very legit guy
* elec / math background

## Motivation and Setting

probabilistic models of cellular networks
* positions of base stations (cell towers) and mobile users in euclidean plane
  are viewed as realizations of [**stochastic point
  processes**](https://en.wikipedia.org/wiki/Point_process)
* would like to measure functionals of these processes (shannon rate)

## poisson-voronoi cellular networks

* base stations arranged by homogenous poisson point process
* create voronoi cells by intersection of half planes, each half plane defined
  by a line halfway between two base stations

### coverage / shannon rate in p-v networks

SNR experienced: 
* signal: power from closest BS
* noise: power from all BSs outside v cell

### signal fading

Signals sent out from an antenna can bounce and interact with each other at
difference phases, resulting in incorrectly amplified or even destroyed
waveforms.

"Rayleigh fading"

Coverage / Shannon Rate:

$$
p_c(T, \lambda, \beta) = P(\text{SINR} > T) = P(\text{shannon rate} > B \log{ (?) })
$$

interpretation of this:  
* probability a random user has SINR T
* average number of users with SINR T
* average T-coverage of the cell

### main result + proof

A lot of complex math, see [this paper (appendix
B)](https://arxiv.org/pdf/1009.0516) for the details.

Basically, they are able to build a closed form formula for the $p_c$ we 
defined above.  With certain assumptions this simplifies down to some
pretty simple fractions.  However the assumptions are not necessary

## ongoing research and motivations

kinda got lost -- discussed space-time interactions in wireless networks

* bound of time it will take to transfer files in noisy environments
* wrote a book on stochastic geometries / networks
* new generative way of clustering that arises from the dynamics
