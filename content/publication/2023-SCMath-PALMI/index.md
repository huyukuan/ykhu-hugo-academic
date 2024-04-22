---
title: The convergence properties of infeasible inexact proximal alternating linearized minimization
authors:
- admin
- X. Liu
date: "2023-09-26T00:00:00Z"
doi: "10.1007/s11425-022-2074-7"

# Schedule page publish date (NOT publication's date).
#publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Science China Mathematics*, 2023, 66(10): 2385-2410"
publication_short: ""

abstract: The proximal alternating linearized minimization (PALM) method suits well for solving block-structured optimization problems, which are ubiquitous in real applications. In the cases where subproblems do not have closed-form solutions, e.g., due to complex constraints, infeasible subsolvers are indispensable, giving rise to an infeasible inexact PALM (PALM-I). Numerous efforts have been devoted to analyzing the feasible PALM, while little attention has been paid to the PALM-I. The usage of the PALM-I thus lacks a theoretical guarantee. The essential difficulty of analysis consists in the objective value nonmonotonicity induced by the infeasibility. We study in the present work the convergence properties of the PALM-I. In particular, we construct a surrogate sequence to surmount the nonmonotonicity issue and devise an implementable inexact criterion. Based upon these, we manage to establish the stationarity of any accumulation point, and moreover, show the iterate convergence and the asymptotic convergence rates under the assumption of the Łojasiewicz property. The prominent advantages of the PALM-I on CPU time are illustrated via numerical experiments on problems arising from quantum physics and 3-dimensional anisotropic frictional contact.

# Summary. An optional shortened abstract.
summary: "We study the theoretical properties of proximal alternating linearized minimization (PALM) method, which is a popular unified framework for multi-block nonconvex optimization.

###### Setting

The subproblems are solved by infeasible subsolvers, yielding infeasible iterates. Examples are ubiquitous; for example, consider a feasible set described by a severely under-determined linear system. However, there are few existing works in this aspect. 

###### Theoretical results

- Implementable inexact criterion for solving subproblems based on error bounds.

- Global convergence to stationarity and novel asymptotic convergence rates."

featured: false

links:
- name: "Preprint"
  url: "https://arxiv.org/pdf/2204.06182.pdf"
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
