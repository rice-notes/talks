# Rethinking concepts in ML: Implicit Reg., over-parameterization, momentum acceleration

## three hypotheses

* adaptive optimization methods such as adagrad / adam perform worse than
  classicaly gradient descent
* gradient descent implicitly regularizes our model
* should we use adaptive optimization blindly?

## adaptivity in gradient methods

setup toy problem of linear regression: $d >> n$, outputs $y_i \in \{-\alpha,
+\alpha\}$.  Each example of $X$ has the true label in the first position, the
rest of the are binary patterns which do not repeat.  So that the optimal
solution is a vector of ones with 

### results

* for $\alpha = 1$, SGD able to find optimal
