---
title: Force-based gradient descent method for ab initio atomic structure relaxation
authors:
- admin
- Xingyu Gao
- Yafan Zhao
- Xin Liu
- Haifeng Song
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
publication: "*Physical Review B*, 106(10): 104101"
publication_short: ""

abstract: Force-based algorithms for *ab initio* atomic structure relaxation, such as conjugate gradient methods, usually get stuck in the line minimization processes along search directions, where expensive *ab initio* calculations are triggered frequently to test trial positions before locating the next iterate. We present a force-based gradient descent method, WANBB, that circumvents the deficiency. At each iteration, WANBB enters the line minimization process with a trial step size capturing the local curvature of the energy surface. The exit is controlled by a nonrestrictive criterion that tends to accept early trials. These two ingredients streamline the line minimization process in WANBB. The numerical simulations on nearly 80 systems with good universality demonstrate the considerable compression of WANBB on the cost for the unaccepted trials compared with conjugate gradient methods. We also observe across the board significant and universal speedups as well as the superior robustness of WANBB over several widely used methods. The latter point is theoretically established. The implementation of WANBB is pretty simple, in that no a priori physical knowledge is required and only three parameters are present without tuning.

# Summary. An optional shortened abstract.
#summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Source Themes
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