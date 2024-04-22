---
title: Sampling-based methods for multi-block optimization problems over transport polytopes 
authors:
- admin
- M. Li
- X. Liu
- C. Meng
date: "2024-03-21T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
#publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "arXiv preprint, arXiv: 2306.16763"
publication_short: ""

abstract: The multimarginal optimal transport problem with Coulomb cost arises in quantum physics and is vital in understanding strongly correlated quantum systems. Its intrinsic curse of dimensionality can be overcome with a Monge-like ansatz. A nonconvex quadratic programmming then emerges after employing discretization and $\ell_1$ penalty. To globally solve this nonconvex problem, we adopt a grid refinements-based framework, in which a local solver is heavily invoked and hence significantly determines the overall efficiency. The block structure of this nonconvex problem suggests taking block coordinate descent-type methods as the local solvers, while the existing ones can get seriously afflicted with the poor scalability induced by the associated sparse-dense matrix multiplications. In this work, borrowing the tools from optimal transport, we develop novel methods that favor highly scalable schemes for subproblems and are completely free of the full matrix multiplications after introducing entrywise sampling. Convergence and asymptotic properties are built on the theory of random matrices. The numerical results on several typical physical systems corroborate the effectiveness and better scalability of our approach, which also allows the first visualization for the approximate optimal transport maps between electrons in three-dimensional contexts. 

# Summary. An optional shortened abstract.
summary: ""

featured: false

links:
- name: "Preprint"
  url: "https://arxiv.org/pdf/2306.16763.pdf"
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
