---
layout: post
title:  "Geometric Hitting Set Problems"
date:   2021-11-30 
excerpt: A <i>Local Search</i> algorithm, for a maximization problem, works as follows - start with a small set which satisfies the required property; check if there is a "small" subset of it can be swapped with a "slightly larger" set so that the remaining set still satisfies this property; swap if possible and repeat the procedure or return the set that is obtained. For my 8<sup>th</sup> and 9<sup>th</sup> semester projects, I worked on this algorithm when applied to the geometric setting. I wrote a report that discusses the construction of a PTAS using this paradigm and its optimality in certain conditions.
tags:   ["Academics","Reports"]
---

A <i>Local Search</i> algorithm, for a maximization problem, works as follows: start with a small set which satisfies the required property; check if there is a "small" subset of it can be swapped with a "slightly larger" set so that the remaining set still satisfies this property; swap if possible and repeat the procedure or return the set that is obtained. This simple algorithmic framework was used to produce a polynomial-time approximation scheme (PTAS) for problems that satisfy a certain condition (called the *locality condition*) by [Mustafa and Ray](https://link.springer.com/article/10.1007/s00454-010-9285-9){:target="_blank"} in 2010. Thereafter, this PTAS has been modified to solve several geometric hitting set problems. 

My introduction to this paper was through one such use case - this framework was used to produce a PTAS for the *Terrain Guarding* Problem (see [this post]({{ site.baseurl }}{% post_url 2020-05-11-Terrain Guarding %}) and [this post]({{ site.baseurl }}{% post_url 2021-02-12-One-Sided Discrete Terrain Guarding and Chordal Graphs%}) for more information on the problem) in [2014](https://jocg.org/index.php/jocg/article/view/2931){:target="_blank"}. 

In 2018, [Jartoux and Mustafa](https://drops.dagstuhl.de/opus/volltexte/2018/8761/){:target="_blank"} proved that local search is optimal (up to a sublinear factor) for those problems that give rise to arbitrarily large "grid-like" *locality graphs*. They also proved that certain well-known problems such as *Minimum Hitting Set* and *Maximum Independent Set* derived from disks on a plane can give rise to these locality graphs. However, it is an open question if terrains can give rise to such graphs and thus whether the PTAS that we have for the problem is optimal. 

For my 8<sup>th</sup> and 9<sup>th</sup> semester projects, I worked on this algorithm when applied to the geometric setting. I wrote a report that discusses the construction of a PTAS using this paradigm and its optimality in certain conditions. I made some preliminary progress answering the open question regarding terrains, but since it is an work in progress, I have not included it in this report.

I've done my best to iron out typos and avoid mistakes. If you find any typos, mistakes or just  want to talk about this topic, [email me](mailto:kprahlad.narasimhan@niser.ac.in){:target="_blank"}!

#### <center><a href = "{{site.baseurl}}/documents/Geometric Hitting Set Problems.pdf" download> Report </a></center>
