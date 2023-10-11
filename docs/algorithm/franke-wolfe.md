---
hide:
  - navigation
---

# Franke-Wolfe

(Assume everything is a real-valued and finite dimensional Hilbert space.)

## Iteration

For a finite dimensional Hilbert space $\mathbb{H}$ (_e.g_ $\mathbb{H} = \mathbb{R}^{\mathsf{n}}$) constraint set $\mathcal{C} \subseteq \mathbb{H}$, and a function[^4] $\mathsf{f\colon \mathbb{H} \rightarrow \overline{\mathbb{R}}}$ that is differentiable at $\mathsf{x^k \in \mathbb{H}}, the update $\mathsf{x^{k+1}}$ in gradient descent is defined by

[^4]: Here $\overline{\mathbb{R}}\triangleq \mathbb{R} \cup \infty.$

$$
    \mathsf{x^{k+1} \triangleq \underset{x\in \mathcal{C}}{argmin} \left< \nabla f(x^k), x \right> }.
$$

## Overview

Maintains feasibility. Is equivalent to minimizing linearizations.

## Properties

**Convergence Theorem**[^1] If $\mathsf{f}$ is convex and differentiable over $\mathcal{C}$ and the set $\mathcal{C}$ is convex and compact, then the sequence $\mathsf{\{x^k\}}$ converges to a minimizer of $\mathsf{f}$ over $\mathcal{C}$.

Zigzag Behavior[^2] Oscillations can occur...

Invariant to Coordinate System[^3] Can rescale or re-jigger coordinates without any change in outcomes.


[^1]: Insert citation to classic work.

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
