---
layout: post
title:  "Guarding Terrains and Covering Chordal Graphs"
date:   2021-02-12
image:  
excerpt: The <i>Discrete Terrain Guarding</i> problem (discussed in one of my <a href = "https://kprahlad.github.io/2020/05/11/Terrain-Guarding/">previous posts</a>) has been shown to be NP_Hard, but it remains to be seen if it is FPT with respect to the size of the solution size. In this direction, <a href= "https://dl.acm.org/doi/10.1145/3186897">Ashok <i>et al.</i></a> proved in 2015 that <i>Orthogonal Discrete Terrain Guarding</i> is FPT. They used a lemma proved by <a href = "https://doi.org/10.1016/j.comgeo.2007.02.002">Katz and Roisman</a> which established a relationship between this problem and the <i>Clique Cover</i> problem in chordal graphs. My (first!) paper extends this lemma and takes a step forward in understanding the fixed-parameterized tractability of <i>Discrete Terrain Guarding</i>.
tags:   ["Academics"]
---

In one of my [previous posts]({{ site.baseurl }}{% post_url 2020-05-11-Terrain Guarding %}), I had described the *Discrete Terrain Guarding* problem. Quickly, the problem is to place guards on the vertices of a \\(x\\)-monotone polygonal chain such that each vertex of that chain is seen by one of these guards. This problem turns out to be NP-Hard but admits a PTAS. A major open question is whether or not this problem is FPT with respect to the size of the guard set.

It was proved in 2018 by [Ashok *et al.*](https://dl.acm.org/doi/10.1145/3186897) that a restriction of this problem (where the edges describing the terrain are parallel to one of the axes) is indeed FPT with respect to the solution size. One of the results that they used to design their algorithm was the following: if there exists a set of vertices \\(U\\) of the terrain which cannot be seen by \\(k\\)-many guards, there exists a \\(U' \subseteq U\\) of size \\(k+1\\) that cannot be seen by \\(k\\)-many guards. This result followed, as a corollary, from a lemma proved by [Katz and Roisman](https://doi.org/10.1016/j.comgeo.2007.02.002) which established a relationship between the *Orthogonal Terrain Guarding* problem and the *Clique Cover* problem in chordal graphs.

My paper ([DOI](https://doi.org/10.1007/978-3-030-67899-9_10)) extends the result proved by Katz and Roisman to all terrains and thus extends the corollary given by Ashok *et al.* to general terrains. This is done by an extensive use of the *Order Claim*, first stated by [Ben-Moshe *et al.*](https://doi.org/10.1137/S0097539704446384) in 2007, on the various cases that pop up depending on the positions of the guards and the vertices that they are guarding. It will be interesting to see if this can be used to prove (or disprove) that *Terrain Guarding* is FPT.

This is my first academic publication! This paper is a result of my COVID-induced-6-month-long break. I presented this paper at [CALDAM-2021](https://www.iitrpr.ac.in/caldam2021/index.html). Unfortunately, this was done from my hostel room in NISER (during end-semester exam week, *sigh*) and not in the foothills of the Shivaliks at IIT-Ropar due to the pandemic. Since this was a solo paper, it was extremely demanding - especially since my manuscript came back for corrections during the busiest part of my semester. I made a lot of mistakes and thus learnt a truckload. A huge thanks to my mentor [Dr. Aritra Banik](www.niser.ac.in/~aritra/) for initial discussions and support during the final stages! 

Feel free to [email me](mailto:kprahlad.narasimhan@niser.ac.in) if you want to discuss this topic! The pre-print of this paper can be downloaded as a PDF from here: 

#### <center><a href = "{{site.baseurl}}/documents/One-Sided Discrete Terrain Guarding and Chordal Graphs.pdf" download> Pre-Print </a></center>