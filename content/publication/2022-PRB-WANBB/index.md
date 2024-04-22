---
title: Force-based gradient descent method for ab initio atomic structure relaxation
authors:
- admin
- X. Gao
- Y. Zhao
- X. Liu
- H. Song
date: "2022-09-01T00:00:00Z"
doi: "10.1103/PhysRevB.106.104101"

# Schedule page publish date (NOT publication's date).
#publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Physical Review B*, 2022, 106(10): 104101"
publication_short: ""

abstract: Force-based algorithms for *ab initio* atomic structure relaxation, such as conjugate gradient methods, usually get stuck in the line minimization processes along search directions, where expensive *ab initio* calculations are triggered frequently to test trial positions before locating the next iterate. We present a force-based gradient descent method, WANBB, that circumvents the deficiency. At each iteration, WANBB enters the line minimization process with a trial step size capturing the local curvature of the energy surface. The exit is controlled by a nonrestrictive criterion that tends to accept early trials. These two ingredients streamline the line minimization process in WANBB. The numerical simulations on nearly 80 systems with good universality demonstrate the considerable compression of WANBB on the cost for the unaccepted trials compared with conjugate gradient methods. We also observe across the board significant and universal speedups as well as the superior robustness of WANBB over several widely used methods. The latter point is theoretically established. The implementation of WANBB is pretty simple, in that no a priori physical knowledge is required and only three parameters are present without tuning.

# Summary. An optional shortened abstract.
summary: "We develop a force-based nonmonotone method for atomic structure relaxation, a ubiquitous yet expensive task in materials simulation and design. Conventional methods such as conjugate gradient methods are computationally robust but usually require a lengthy relaxation process, resulting in their inefficiency.

###### Method

The inefficiency of conjugate gradient methods can be credited to the improper line minimization (LM) process therein. We devise a novel method named WANBB with an improved LM process, featuring

- curvature-informed initial trial step sizes;

- a reweighted nonmonotone line minimization criterion.


The convergence of WANBB to equilibrium is also rigorously established.

###### Results

We test WANBB against conjugate gradient methods and quasi-Newton methods over a benchmark set containing nearly 80 systems with good universality. 

- Convergence of WANBB on all systems (with a high-entropy alloy as demonstration).

- Speedup factor over conjugate gradient methods > 1.5.

### Important Note

WANBB has been integrated into a suite for crystal structure relaxation called ProMe-SuRe, which can be interfaced to some widely used materials simulation software. **Static-link library files are available upon request!**"

featured: false

links:
- name: "Preprint"
  url: "https://arxiv.org/pdf/2206.02091.pdf"
url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
#image:
#  caption: ''
#  focal_point: ""
#  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ''
---
