---
tags:
  - algorithm
  - frank-wolfe
  - conditional-gradient
  - first-order
  - projection-free
---

# Frank-Wolfe

!!! warning "Note from Editors"

    This article has been flagged as incomplete for the following:

    - [ ] Incomplete / poorly formatted list of properties
    - [ ] Incomplete code in programing examples
    - [ ] Inadequate references to applications (Section: Applications)    
    - [ ] Inadequate references to related works (Section: See Also)

## Definition

For a constraint set $\mathcal{C} \subseteq \mathbb{H}$[^5]  and a function[^4] $\ \mathsf{f\colon \mathbb{H} \rightarrow \overline{\mathbb{R}}}$ that is differentiable over $\mathcal{C}$, consider the constrained minimization problem

$$
    \mathsf{\underset{x \in \mathcal{C}}{min} \ f(x).}
$$

Frank-Wolfe is an iterative scheme for solving this problem with update $\mathsf{x^{k+1}}$ defined by 

[^5]: We let $\mathbb{H}$ be a real-valued finite dimensional Hilbert space (_e.g_ $\ \mathbb{H} = \mathbb{R}^{\mathsf{n}}$).

[^4]: Here $\overline{\mathbb{R}}\triangleq \mathbb{R} \cup \infty.$

\begin{aligned}
    \mathsf{s^{k+1}} & \mathsf{\triangleq \underset{x\in \mathcal{C}}{argmin} \ \left< \nabla f(x^k),\  x \right>, } \\
    \mathsf{x^{k+1}} & \mathsf{\triangleq x^k + \alpha_k \left( s^k - x^k \right),}
\end{aligned}

with a step size rule typically given by either

$$
\mathsf{\alpha_k = \dfrac{2}{k+1} \quad {or} \quad \alpha_k = \underset{\alpha\in[0,1]}{argmin} \ f\left(x^k + \alpha (s^k - x^k)\right).}
$$

## Overview

The Frank–Wolfe (FW) algorithm, also called "conditional gradient", is an iterative first-order algorithm for solving constrained convex problems. The method was proposed by Marguerite Frank and Philip Wolfe in 1956.[^6] Each update minimimizes the linearization of $\mathsf{f}$ about $\mathsf{x^k}$ over the domain $\mathcal{C}$. This ensures each iteration is feasible. Several standard convergence properties hold for FW and its variants.

[^6]: Frank, M., Wolfe, P. _An algorithm for quadratic programming_. Naval Research Logistics Quarterly. 1956.

## Properties

**Convergence Theorem**[^1] 

If $\mathsf{f}$ is convex and Lipschitz differentiable over a convex and compact set $\mathcal{C}$, then there is a constant $\mathsf{C> 0}$ such that

$$
\mathsf{f(x^k) \leq f(x^\star) + \dfrac{C}{k+2},}
$$

where $\mathsf{x^\star}$ is a minimizer of $\mathsf{f}$ over $\mathcal{C}$.

**Zigzag Behavior**[^2] 

Oscillations can occur...

**Invariant to Coordinate System**[^3]

Can rescale or re-jigger coordinates without any change in outcomes.

**Feasible + Projection-Free**

No projections needed if $\mathsf{x^1 \in \mathcal{C}.}$


[^1]: Jaggi, M. _Revisiting Frank-Wolfe: Projection-Free Sparse Convex Optimization._ ICML. 2013.

[^2]: Insert citations to Jaggi paper.

[^3]: Use Taylor's theorem or something...
 

## Code

=== "Python (Linear Constraint)"

    ``` python
    # Constraint: C = { x : A * x = b }
    A = np.randn(100, 5)
    b = np.randn(5, 1)

    def get_fw_solution(gradf, A, b, num_iters=100):
        """ Compute Frank-Wolfe solution

            args:
                gradf: gradient operator for objective
                A:     matrix defining linear constraint
                b:     vector defining linear constraint

            returns:
              x: solution estimate
        """
        x = init # find a feasible point

        for _ in range(num_iters):
            x = x - grad_f(x)
        
        return x
    ```
=== "Python (Ellipsoid Constraint)"

    ``` python
    # Constraint: C = { x : A * x = b }
    A = np.randn(100, 5)
    b = np.randn(5, 1)

    def get_fw_solution(gradf, A, b, num_iters=100):
        """ Compute Frank-Wolfe solution

            args:
                gradf: gradient operator for objective
                A:     matrix defining linear constraint
                b:     vector defining linear constraint

            returns:
              x: solution estimate
        """
        x = init # find a feasible point

        for _ in range(num_iters):
            x = x - grad_f(x)
        
        return x
    ```         

## Applications

- Statistics.
- Compressed sensing.

## See Also

- [Wikipedia: Frank-Wolfe algorithm](https://en.wikipedia.org/wiki/Frank%E2%80%93Wolfe_algorithm)
- Sparse Franke-Wolfe.
