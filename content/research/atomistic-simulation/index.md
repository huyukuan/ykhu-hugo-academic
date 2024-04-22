---
title: Optimization for atomistic simulation
#subtitle: With broad applications though, strongly correlated quantum systems are the famous examples where the popular Kohn-Sham density functional theory induces non-negligible systematic errors. My collaborators and I have been devoted to investigating other formulations that well describe the behavior of electrons in this setting and developing numerical approaches for the associated optimization problems.

# Summary for listings and search engines
summary: Atomistic simulation sets the basis and computational bottleneck in high-througput materials design, phase diagram calculations, etc. Following molecular statics, my collaborators and I formulate the related optimization problems with physical constraints and develop globally convergent algorithms and robust packages. 

# Link this post with a project
projects: []

# Date published
date: '2023-10-20T00:00:00Z'

# Date updated
lastmod: '2023-10-22T00:00:00Z'

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

Nowadays, people adopt atomistic simulation to elucidate the mechanisms of experimentally known phenomena and to develop new materials by analyzing elemental combinations and structures. Building on *ab-initio* or (semi-)empirical force fields, atomistic simulation models materials at the level of atoms and seeks equilibrium states (including saddle points) and transition paths over the potential energy surface. One of the most fundamental tasks for these purposes goes to structure relaxation (also known as structure/geometry optimization)[^1]. 

Structure relaxation can be formulated as an optimization problem in atomic positions (and also lattice vectors, if you consider crystals). Conventional methods are conjugate gradient methods (CG[^2]) and quasi-Newton methods (QN[^3]), as seen in the off-the-shelf materials simulation software. From the practical aspect, CG favors better robustness but is unsatisfactory in efficiency, while QN converges fast only around local minima. In theory, both these two lack global convergence guarantees, particularly when physical constraints are present. The physical constraints, however, are of significance in reducing the dimensionality of the configurational space and can be found in various downstream applications. 

Regarding structure relaxation, my interests basically concern with **developing computationally efficient and theoretically convergent optimization methods catering for various applications**. Currently, my collaborators and I mainly work on

* crystal structure relaxation under physical constraints.

By the way, I also pay attention to the effect of inexact oracles (or error propagation) on structure relaxation. 

### <a id="crystal-structure-relaxation-under-physical-constraints">**Crystal structure relaxation under physical constraints**</a>

**Collaborators:**
* [Xingyu Gao](http://www.iapcm.ac.cn/teaching_detail_103.html) (China Academy of Engineering Physics);
* [Xin Liu](http://lsec.cc.ac.cn/~liuxin/) (Chinese Academy of Sciences);
* [Haifeng Song](http://www.iapcm.ac.cn/teaching_detail_136.html) (China Academy of Engineering Physics);
* Yafan Zhao (China Academy of Engineering Physics);
* Xin Chen (China Academy of Engineering Physics);
* Junlei Yin (Northwest Polytechnical University);
* Zhen Yang (University of Science and Technology Beijing).

We consider requirements from several contexts, encompassing relaxation 

1. with fixed lattice vectors; 
2. with fixed unit cell volumes; 
3. under given external pressures. 

Notably, (2) is frequently seen in the calculations of the equations of state as well as material response functions, (3) finds itself in structure searches under high external pressures. Mathematically, (2) corresponds to a nonconvex determinant constrained problem, to which little attention has been paid from the optimization community. 

Our works largely improve the execution of the line minimization process, in which CG can easily get trapped. Roughly speaking, the developed methods imitate the Newton method by exploiting the curvature of the potential energy surface, yet with computational costs in line with that of CG. The overall convergence is ensured by an improved nonmonotone stopping rule for the line minimization process. **Across a benchmark set with good universality, our methods achieve over 50% speedup against CG without any failure.**

<font color=#D64D8A>*We have developed a suite called* "ProMe-SuRe" *for crystal structure relaxation with the above functions realized. The suite can be interfaced to some off-the-shelf materials simulation package. Static-link library files are available upon request!*</font>

**References**

* Y. Hu, X. Gao, Y. Zhao, X. Liu, and H. Song. Force-based gradient descent method for *ab initio* atomic structure relaxation. <font face="Times New Roman">*Physical Review B*</font>, 2022, 106(10): 104101. ([link](https://doi.org/10.1103/PhysRevB.106.104101))

* Force-based projected gradient descent method for volume constrained *ab initio* crystal structure relaxation. <font face="Times New Roman">*In preparation*</font>.

**Patents and Copyrights**

* X. Gao, X. Liu, Y. Hu, H. Song, X. Chen, Y. Wang, and L. Wang. 晶体结构弛豫软件包 ProMe-SuRe. <font face="Times New Roman">*CN Software Copyright*</font>, 2023, 2023SR1558824.

* X. Gao, X. Liu, H. Song, Y. Hu, X. Chen, Y. Wang, J. Fang, L. Wang, and L. Zhang. 固定晶格体积晶体结构弛豫的计算方法及装置. <font face="Times New Roman">*CN Patent*</font>, 2023, ZL 202211210741.3.

* X. Gao, X. Liu, H. Song, Y. Hu, J. Fang, Z. Yang, Y. Zhao, L. Wang, and H. Liu. 原子结构弛豫的非单调线搜索方法及装置. <font face="Times New Roman">*CN Patent*</font>, 2022, ZL 202111534901.5.

**Ongoing works**

* Optimization methods for crystal structure relaxation that preserve symmetry.
* Analysis for error propagation on structure relaxation.

[^1]: We consider here molecular statics, in comparison with molecular dynamics. 
[^2]: https://en.wikipedia.org/wiki/Nonlinear_conjugate_gradient_method.
[^3]: https://www.sciencedirect.com/science/article/abs/pii/0009261480803964?via%3Dihub.
