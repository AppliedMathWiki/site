---
tags:
  - model
  - convex
---

# Lasso

## Model

For a matrix $\mathsf{A \in \mathbb{R}^{m\times n}}$, a vector $\mathsf{b \in \mathbb{R}^m}$, and a scalar $\mathsf{\lambda > 0}$, the model is

$$
    \mathsf{\underset{x \in \mathbb{R}^n }{min} \ |Ax - b|_2^2 + \lambda |x|_1. }
$$

## Overview

The Least Absolute Shrinkage and Selection Operator (Lasso) function is commonly used in statistics and machine learning for variable selection and regularization. Introduced by Tibshirani[^1], it is primarily used in linear regression models, but its principles can be extended to other models as well. The key idea of the Lasso function is to add a penalty term to least squares regression that is the sum of absolute values of the coefficients.

<br>

<center>
  
| Property                |       |  
|:-----------------------:|:-----:| 
| Convex                  | ✅    |     
| Strongly Convex         | 🟡    | 
| Unbiased Estimator[^2]  | ✅    |
| Feasible Estimator      | 🟡    |

</center>

<br>

## Code

=== "CVXPY"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

=== "SCIP"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "Gurobi"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

=== "CPLEX"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```    

## Applications

- Statistics... 
- Compressed sensing...


## See Also

- [Wikipedia - Lasso (statistics)](https://en.wikipedia.org/wiki/Lasso_(statistics))

<!--- References --->

[^1]: Tibshirani. "Regression shrinkage and selection via the lasso." _Journal of the Royal Statistical Society Series B: Statistical Methodology_. 1996

[^2]: Fan, Li. "Variable selection via nonconcave penalized likelihood and its oracle properties." _Journal of the American statistical Association_. 2001.


