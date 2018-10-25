# Differentially Private Change-point Detection

Paper will appear at NIPS this winter.

## Change-point problem

Classical statistical problem: identify distributional changes in a stream of
data.

$x_1, \ldots, x_k \sim P_0$ 
$x_{k+1}, \ldots, x_n \sim P_1$

## Differential Privacy

[Differential Privacy](https://en.wikipedia.org/wiki/Differential_Privacy) is a
technique to bound the effect that a single data point can have on a specific
aggregate computation.  

The intution is that if you look at all data, you don't want to be able to
remove an individual's data from the aggregate to determine the individual's
data.

* Post-processing: Any functions applied to the result of a computation from a DP algorithm is DP
* Composition: The use of results from $n$ $\epsilon_i$ DP computations is $\sum_i \epsilon_i$ DP

## Offline PCPD

Mashup of [ CUSUM Algorithm ](https://en.wikipedia.org/wiki/CUSUM) with the 
DP max algorithm.

Main result is an $$(\alpha, \beta)$$-accurate bound on the error of the
private algorithm.  

## Online PCPD

Idea: 

1. Chunk the incoming stream into groups $X_i$ of $n$ data points and privately
   detect if there exists a query $f$ such that $f(X_i) > T$
2. Run Offline PCPD on the chunk if the query is greater than $T$

## Questions

Why laplace error?

    The laplace distribution is situated nicely for errors since the tails are
    exponential.  It makes the math nice.

Is there something to be gained by viewing this as a statistical problem?

The results you showed us were one-dimensional temporal streams.  Have you done
any work with multi-dimensional and spatio-temporal data?

    Not on this problem, but we'd be interested in working on this later.

How do bring CS / Stat people together?

    Need to get a common language between CS and Stat people.  The error bounds
    that CS people use are very different than the asymptotic bounds that 
    statiticians use.
