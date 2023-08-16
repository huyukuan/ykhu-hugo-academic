---
title: A global optimization approach for multimarginal optimal transport problems with Coulomb cost
authors:
- admin
- Huajie Chen
- Xin Liu
date: "2023-06-12T00:00:00Z"
doi: "10.1137/21M1455164"

# Schedule page publish date (NOT publication's date).
#publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*SIAM Journal on Scientific Computing*, 45(3): A1214--A1238"
publication_short: ""

abstract: In this work, we construct a novel numerical method for solving the multimarginal optimal transport problems with Coulomb cost. This type of optimal transport problem arises in quantum physics and plays an important role in understanding the strongly correlated quantum systems. With a Monge-like ansatz, we transfer the original high-dimensional problems into mathematical programmings with generalized complementarity constraints, and thus the curse of dimensionality is surmounted. However, the latter ones are themselves hard to deal with from both theoretical and practical perspectives. Moreover, in the presence of nonconvexity, brute-force searching for global solutions becomes prohibitive as the problem size grows large. To this end, we propose a global optimization approach for solving the nonconvex optimization problems, by exploiting an efficient proximal block coordinate descent local solver and an initialization subroutine based on hierarchical grid refinements. We conduct numerical simulations on some typical physical systems to show the efficiency of our approach. The results match well with both theoretical predictions and physical intuitions and provide indications for Monge solutions in two-dimensional contexts. In addition, we give the first visualization of approximate optimal transport maps for some two-dimensional systems.

# Summary. An optional shortened abstract.
#summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Source Themes
featured: false

links:
- name: "Preprint"
  url: "https://arxiv.org/pdf/2110.07352.pdf"
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