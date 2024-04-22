---
title: Electronic structure calculations for strongly correlated quantum systems
#subtitle: With broad applications though, strongly correlated quantum systems are the famous examples where the popular Kohn-Sham density functional theory induces non-negligible systematic errors. My collaborators and I have been devoted to investigating other formulations that well describe the behavior of electrons in this setting and developing numerical approaches for the associated optimization problems.

# Summary for listings and search engines
summary: With broad applications though, strongly correlated quantum systems are the famous examples where the popular Kohn-Sham density functional theory induces non-negligible systematic errors. My collaborators and I have been devoted to investigating other formulations that well describe the behavior of electrons in this setting and developing numerical approaches for the associated optimization problems.

Height: 500

# Link this post with a project
projects: []

# Date published
date: '2023-10-19T00:00:00Z'

# Date updated
lastmod: '2024-04-22T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

math: true
# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 1
  preview_only: true

---

According to the celebrated density functional theory[^1], the ground state of a many-electron system can be determined by the single-particle density, eliminating the curse of dimensionality in principle. The variational argument leads to a universal functional comprising of kinetic and electron-electron interaction contributions, yet lacking a tractable expression.

The popular Kohn-Sham (KS) density functional theory[^2] takes a non-interacting reference system and lays emphasis on approximating the kinetic contribution. On account of this starting point, **the KS model can fail to capture the true things for strongly correlated systems** where the interaction energy dominates, even with the state-of-the-art exchange-correlation functionals[^3]. Since strongly correlated materials find **broad applications** (e.g., high-temperature superconductivity, thermoelectric materials, and magnetic storage), new mathematical models and approaches are in an urgent need.

So far, a plethora of models have been constantly emerging, where the issue of high dimensionality often underlies. My interests revolve around **analyzing their theoretical properties and developing scalable numerical approaches**. At this moment, my collaborators and I mainly work on

* strictly-correlated-electrons density functional theory[^4];

* variational Monte Carlo methods[^5].



### <a id="strictly-correlated-electrons-density-functional-theory">**Strictly-correlated-electrons density functional theory**</a>

**Collaborators:**

* [Huajie Chen](http://math0.bnu.edu.cn/~chenhuajie/) (Beijing Normal University);
* [Xin Liu](http://lsec.cc.ac.cn/~liuxin/) (Chinese Academy of Sciences);
* [Mengyu Li](https://mengyu8042.github.io) (Renmin University of China);
* [Cheng Meng](https://chengzijunaixiaoli.github.io) (Renmin University of China).

This model runs from the opposite face of the KS model and builds on a multimarginal optimal transport problem with Coulomb cost (MMOT). Leveraging a low-dimensional ansatz for the square modulus of wave function $|\Psi|^2$, which takes roots in optimal transport and encodes two-electron couplings, one could derive a nonconvex reformulation for the MMOT. The number of unknowns therein scales linearly with respect to the number of electrons. Due to the intricacies of the nonconvex problem, existing works in this aspect consider systems with only two electrons. 

Our contributions:

* **establish the theoretical properties of the nonconvex formulation.** Violating conventional constraint qualifications, the nonconvex formulation (denoted by (P)) itself is not appropriate for numerical resolution. Without extra assumptions in the literature, we establish the equivalence between (P) and a nonconvex quadratic programming (denoted by (P')). Interestingly, we numerically observe that (P') is "nearly" amenable to any local solvers;<p><br></p>
* **propose a global optimization framework trading off accuracy and efficiency.** Enlightened by the idea of multigrid methods and optimal transport, we starts with solving (P') globally over a coarse mesh and proceeds with merely local solvers for (P') over finer meshes. The local solvers are fed with initial points constructed from the previous solutions. In simulations, electron positions mappings are first visualized in two/three-dimensional contexts; <p><br></p>
* **devise sampling-based methods as local solvers without cubic complexities.** To alleviate the cubic computational burden in gradient calculations, we adopt Kullback-Leibler divergence and incorporate importance sampling-based matrix sparsification into iterative schemes. The resulted methods do not store and operate on dense matrices at all. Compared with conventional stochastic algorithms, our methods add randomness to constraints in essence. <p><br></p>
* **provide the first convergence results for the local solvers under realizable conditions.** For better efficiency, the involved local solvers may invoke infeasible methods for subproblems. With infeasible iterates, the nonmonotonicity of objective values is inevitable, complicating the convergence analyses. Unlike the existing works, we show the convergence under realizable conditions. Novel convergence rates are also derived. 

**References**

1. Y. Hu, H. Chen, and X. Liu. A global optimization approach for multimarginal optimal transport problems with Coulomb cost. <font face="Times New Roman">*SIAM Journal on Scientific Computing*</font>, 2023, 45(3): A1214-A1238. ([link](https://doi.org/10.1137/21M1455164))

2. Y. Hu and X. Liu. The convergence properties of infeasible inexact proximal alternating linearized minimization. <font face="Times New Roman">*Science China Mathematics*</font>, 2023, 66(10): 2385-2410. ([link](https://doi.org/10.1007/s11425-022-2074-7))

3. Y. Hu and X. Liu. The exactness of the $\ell_1$ penalty function for a class of mathematical programs with generalized complementarity constraints. <font face="Times New Roman">*Fundamental Research*</font>, available online. ([link](https://doi.org/10.1016/j.fmre.2023.04.006))

4. Y. Hu, M. Li, X. Liu, and C. Meng. Sampling-based methods for multi-block optimization problems over transport polytopes. <font face="Times New Roman">arXiv preprint</font>, arXiv: 2306.16763. ([link](https://arxiv.org/pdf/2306.16763.pdf))

**Ongoing works**
* Local solvers with nice scaling with respect to the number of electrons and discretization size.
* Landscape analysis for the nonconvex reformulation of the MMOT.
* Convergence analysis for the global optimization framework.
* Numerical approaches for the other reformulations of the MMOT. 

[^1]: https://en.wikipedia.org/wiki/Density_functional_theory.
[^2]: https://en.wikipedia.org/wiki/Kohn-Sham_equations.
[^3]: https://www.science.org/doi/abs/10.1126/science.1158722.
[^4]: https://link.springer.com/chapter/10.1007/978-3-031-22340-2_4.
[^5]: https://en.wikipedia.org/wiki/Variational_Monte_Carlo.
