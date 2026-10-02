---
title: "Physics-Informed Neural Networks for Chaotic Dynamical Systems"
date: 2025-07-20T10:00:00+05:30
draft: false
publication_venue: "International Conference on Machine Learning (ICML)"
authors: "Lokesh Balasubramanian, Jane Doe"
arxiv_id: "2507.54321"
pdf_url: "https://arxiv.org/pdf/2507.54321.pdf"
code_url: "https://github.com/lokeshbalasubramanian/pinn-chaos"
project_url: "#"
selected: false
tags: ["Physics-Informed ML", "Dynamical Systems", "Deep Learning"]
bibtex: |
  @inproceedings{balasubramanian2025pinns,
    title={Physics-Informed Neural Networks for Chaotic Dynamical Systems},
    author={Balasubramanian, Lokesh and Doe, Jane},
    booktitle={International Conference on Machine Learning (ICML)},
    pages={4012--4025},
    year={2025},
    organization={PMLR}
  }
---

Solving chaotic systems like the double pendulum or Lorenz attractor using classical numerical methods can be computationally prohibitive over long integration times. We propose a custom Loss-Regularized Physics-Informed Neural Network (PINN) that embeds Hamiltonian conservation properties into the loss function.

Our framework significantly reduces cumulative integration errors and guarantees long-term energy conservation within 1e-4 tolerance, outperforming standard Runge-Kutta-4 baselines in highly chaotic regimes.
