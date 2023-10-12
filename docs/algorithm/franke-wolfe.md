---
hide:
  - navigation
tags:
  - algorithm
  - franke-wolfe
  - conditional-gradient
---

# Franke-Wolfe

## Iteration

For a constraint set $\mathcal{C} \subseteq \mathbb{H}$[^5]  and a function[^4] $\ \mathsf{f\colon \mathbb{H} \rightarrow \overline{\mathbb{R}}}$ that is differentiable at $\mathsf{x^k \in \mathbb{H}}$, the Franke-Wolfe update $\mathsf{x^{k+1}}$ is defined by[^6]

[^5]: We let $\mathbb{H}$ be a real-valued finite dimensional Hilbert space (_e.g_ $\mathbb{H} = \mathbb{R}^{\mathsf{n}}$).

[^4]: Here $\overline{\mathbb{R}}\triangleq \mathbb{R} \cup \infty.$

[^6]: The objective in the update is equivalent to minimizing the linearization of $\mathsf{f}$ about $\mathsf{x^k}$, i.e. $\mathsf{f(x^k)+\left<\nabla f(x^k),\ x - x^k\right>}.$

$$
    \mathsf{x^{k+1} \triangleq \underset{x\in \mathcal{C}}{argmin} \left< \nabla f(x^k),\  x \right> }.
$$

## Overview

Maintains feasibility. Is equivalent to minimizing linearizations.

## Properties

**Convergence Theorem**[^1] 

If $\mathsf{f}$ is convex and Lipschitz differentiable over a convex and compact set $\mathcal{C}$, then there is a constant $\mathsf{C> 0}$ such that

$$
\mathsf{f(x^k) \leq f(x^\star) + \dfrac{C}{k+2},}
$$

where $x^\star$ is a minimizer of $\mathsf{f}$ over $\mathcal{C}$.

**Zigzag Behavior**[^2] 

Oscillations can occur...

**Invariant to Coordinate System**[^3]

Can rescale or re-jigger coordinates without any change in outcomes.

**Projection-Free**

No projections needed if $\mathcal{x^1 \in \mathcal{C}.}$


[^1]: Jaggi. _Revisiting Frank-Wolfe: Projection-free sparse convex optimization._ ICML. 2013.

[^2]: Insert citations to Jaggi paper.

[^3]: Use Taylor's theorem or something...
 

## Code

=== "Python"

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

- variations of franke-wolfe.
