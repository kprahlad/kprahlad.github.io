---
layout: post
title:  "Terrain Guarding"
date:   2020-05-11
image:  
tags:   ["Academics"]
---

Consider the following problem: You are the head of a village which lives on a two-dimensional mountain range which has \\(n\\) peaks. These peaks are home to *Vibranium* reserves that the village must protect at all costs from *Wakanda,* the neighbouring village. You have \\(k\\) able bodied warriors who are available to guard these peaks. These warriors  can guard anything that they can see and can be placed anywhere on the  mountain range. Can you guard all the peaks? If so, can you figure out  where to place your warriors so that they guard all the *Vibranium* reserves? What if you can only place your warriors at the peaks and nowhere else?

In math-y terms, you are given a set \\(V\\) which consists of \\(n\\)-many points on the plane and these points are sorted according to their \\(x\\)-coordinate. A terrain is a polygonal chain whose vertex set is \\(V\\). Two points on the terrain see each other if the line joining these two points lies above the terrain. We are required to place \\(k\\)-many guards on the terrain such that every point in \\(V\\) is seen by some guard. This is referred to as the *Continuous Terrain Guarding* problem. If the guards can only be placed on \\(V\\), then it is referred to as the *Discrete Terrain Guarding* problem.

It turns out these problems are computational nightmares - they are NP Hard [[King and Krohn, 2009](https://www.researchgate.net/publication/220779363_Terrain_Guarding_is_NP-Hard)]. To make matters worse, it turns out that solving these problems for what seemed to be a easier class of terrains - those which are made with  only horizontal and vertical lines (orthogonal terrains), is still NP  Hard [[Bonnet and Giannopoulos, 2017](https://arxiv.org/abs/1710.00386)]. Knowing this, we ask the next best thing - are these problems FPT with respect to number of guards \\(k\\)? That is, does there exist an algorithm which solves *Continuous Terrain Guarding* and *Discrete Terrain Guarding* in \\(f(k) \cdot n^c\\) time, where \\(f\\) is some computable function and \\(c\\) is some constant independent of \\(n\\) and \\(k\\)? We only know the answer for this question for orthogonal terrains. Both  the versions of the orthogonal terrain guarding problem are FPT with respect to \\(k\\) [[Ashok et al., 2018](https://dl.acm.org/doi/10.1145/3186897)]. 

I've made a report which seeks to let anyone who has done a basic course in  algorithms understand (almost) current research in this topic. Two of  the major theorems presented in the report are, to the best of my  knowledge, not present in existing literature. I've done my best to iron out typos and avoid mistakes. If you find any typos, mistakes or just  want to talk about this topic, [email me](mailto:kprahlad.narasimhan@niser.ac.in)!

#### <center><a href = "{{site.baseurl}}/documents/A_FPT_Algorithm_for_the_Orthogonal_Terrain_Guarding_Problem.pdf" download> Report </a></center>