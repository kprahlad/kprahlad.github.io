---
layout: post
title:  "Dominator Coloring Parameterized by Cluster Vertex Deletion Number"
date:   2022-11-20
mathjax: true
excerpt: Given a simple graph <i>G</i> and a natural number <i>l</i>, <i>Dominator Coloring</i> asks if it possible to properly color <i>G</i> with at most <i>l</i> colors such that for every vertex <i>v</i> in the graph, there exists a color class <i>c</i> where every vertex colored <i>c</i> is in the neighborhood of <i>v</i>. This problem, first described in 2006 and studied in several papers since then, hosts several interesting open problems. In this combined work (with Prof Aritra Banik and Prof Venkatesh Raman), we initiate the study of the problem through the lens of structural parameterization. We prove that Dominator Coloring, parameterized by the input graph's Cluster Vertex Deletion number, is FPT. We also design faster, simpler, and randomized parameterized algorithms when the parameter is a special CVD set.      
tags:   ["Academics","Publications"]
---

This work started out as my MSc Thesis back in NISER! If you prefer a meme-filled introduction to the problem, check out my [twitter thread](https://twitter.com/pranarkas/status/1587841594769772546) :)

Two of the most prolific problems in graph theory are *Dominating Set* and *Graph Coloring*. Consider a simple graph $$G$$ and a natural number $$\ell$$. We say that vertex $$v$$ *dominates* a vertex $$u$$ if $$v = u$$ or $$u$$ is a neighbor of $$v$$. In the Dominating Set problem, we are required to report if there exists a set of vertices $$S$$ of size at most $$\ell$$ such that for every vertex $$v \in V(G)$$, there exists a $$s \in S$$ such that $$s$$ dominates $$v$$. In *Graph Coloring*, we must decide if it is possible to color the vertices of $$G$$ with at most $$\ell$$ colors such that no two neighboring vertices get the same color. Such a coloring of the vertices is referred to as a *proper coloring*.

*Dominator Coloring* combines these two problems. Once again, we are given a simple graph $$G$$ and a natural number $$\ell$$. We are required to decide if there exists a proper coloring of $$G$$ such that for every vertex $$v$$, there exists a color class $$c$$ where every vertex that is colored $$c$$ is dominated by $$v$$. In this paper, [Prof Aritra Banik](http://www.niser.ac.in/~aritra/), [Prof Venkatesh Raman](https://www.imsc.res.in/~vraman/), and I study the parameterized complexity of Dominator Coloring. 

The problem, which was [first described](https://faculty.nps.edu/rgera/papers/WestPoint_Dom_coloring_final_submitted_changed.pdf) in 2006 and studied in several papers since then, still hosts several important open questions. While it is known, due to [this work](https://www.semanticscholar.org/paper/Algorithmic-Aspects-of-Dominator-Colorings-in-Arumugam-Chandrasekar/649cbb0f199da4318456d775a36d2e3942c423f7) by Arumugam *et al.*, that the problem is FPT (Fixed-Parameter Tractable) when parameterized by $$(t,\ell)$$ where $$\ell$$ is the number of colors used and $$t$$ the *treewidth* of $$G$$, the structural parameterized landscape of the problem remains unexplored. We initiate the study of Dominator Coloring through the lens of structural parameterization. 

Our first result in this paper is a randomized $$O^*(c^k)$$ algorithm for the problem where $$c$$ is some constant and $$k$$ is the size of a graph's Clique Modulator, a set of vertices whose deletion results in a clique. This algorithm is obtained by a non-trivial adaptation of [the recent work](https://doi.org/10.1137/20M1323369) by Gutin *et al.* for List Coloring parameterized by the clique modulator that uses an inclusion-exclusion based polynomial sieving technique, and in addition uses a dynamic programming based exact algorithm we develop for Dominator Coloring. 

Later, we go on to prove the main result of the paper that Dominator Coloring is FPT when parameterized by the size of a graph's Cluster Vertex Deletion (CVD) Set, in contrast to the $$W[i]$$ hardness result for List Coloring parameterized by the CVD set size. En route, we design a simpler and faster deterministic FPT algorithm when the problem is parameterized by the size of a graph's Twin Cover. We believe that this algorithm's approach, which uses a relationship between Dominator Coloring and List Coloring that we establish, is of independent interest.

Feel free to [email me](mailto: prahladnarasim.kasthurirangan@stonybrook.edu){:target="_blank"} if you want to discuss this topic! The pre-print of this paper can be downloaded as a PDF from arXiv: 

#### <center><a href = "https://arxiv.org/abs/2210.17321">arXiv</a></center>
