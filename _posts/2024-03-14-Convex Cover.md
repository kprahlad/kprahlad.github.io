---
layout: post
title:  "Constant-Factor Approximation Algorithms for Convex Cover and Hidden Set in a Simple Polygon"
date:   2024-03-14
mathjax: true
excerpt: Consider a simple polygon <i>P</i>. What is the minimum number of convex subsets of <i>P</i> are required to completely cover <i>P</i>? This fundamental problem (called <i>Convex Cover</i>) in computational geometry has proven to be frustratingly hard to solve exactly and/or to approximate for over fifty years. In this work, we provide the first constant-factor approximation for Convex Cover. This algorithm runs in (nearly) quadratic time. En route, we also provide a constant-factor approximation algorithm for the <i>Hidden Set</i> problem, where we need to find the maximum number of points inside <i>P</i> which do not see each other. This is the first approximation algorithm for Hidden Set in literature.       
tags:   ["Academics","Publications"]
---

Consider the following polygon $$P$$:

![]({{site.baseurl}}/images/ConvexCover/polygon.png){:style="display:block; margin-left:auto; margin-right:auto"}*A polygon.*

The *Convex Cover* problem seeks to cover $$P$$ with the fewest convex polygons that lie within $$P$$. Here, the minimum number of convex polygons required is 3:

![]({{site.baseurl}}/images/ConvexCover/convex_cover.png){:style="display:block; margin-left:auto; margin-right:auto"}*An optimal convex cover of our polygon.*

Convex Cover is a fundamental problem in Computational Geometry; it was first studied in the late 60s [[1]](https://www.sciencedirect.com/science/article/abs/pii/003132036890006X) and in 2003 an $$\mathcal{O}(\log{n})$$-approximation (and and APX-Hardness reduction) was discussed in [[2]](https://epubs.siam.org/doi/10.1137/S0097539702405139) ($$n$$ is the number of vertices of $$P$$). This algorithm is extremely slow (runtime in the order of $$n^{29}$$). Recently, in [[3]](http://ieee-focs.org/FOCS-2021-Papers/pdfs/FOCS2021-5stbVHiOp5jRHWlSl41FkR/205500a375/205500a375.pdf), Abrahamsen showed that Convex Cover is $$\exists\mathbb{R}$$-hard. 

In this paper, we provide the first constant-factor approximation for Convex Cover. The approximation factor is 6: that is, given any polygon $$P$$, our algorithm will return a convex cover of $$P$$ whose cardinality is at most six times that of the optimal cover. Moreover, our algorithm has a much more palatable runtime of (nearly) quadratic time.

En route, we also provide a constant-factor approximation algorithm with the same runtime for the *Hidden Set* problem - here, we want to maximize the number of points that we can place inside $$P$$ which do not see each; see the example below:

![]({{site.baseurl}}/images/ConvexCover/hidden_set.png){:style="display:block; margin-left:auto; margin-right:auto"}*An optimal hidden set of our polygon.*

Our algorithm returns a hidden set whose size is at least an eighth of the optimal hidden set size. This is the first approximation algorithm for Hidden Set.

My coauthors for this work were [Reilly Browne](https://rajalo.github.io), [Joe Mitchell](https://www.stonybrook.edu/commcms/ams/people/_faculty_profiles/mitchell), and [Valentin Polischuk](https://itn-web.it.liu.se/~valpo40/). This was published at FOCS 2023 ([DOI](https://ieeexplore.ieee.org/document/10353176)). A longer version of the talk that Reilly presented at FOCS is available on his [YouTube channel](https://www.youtube.com/watch?v=WOQ4_-7XsEw). Feel free to [email me](mailto: prahladnarasim.kasthurirangan@stonybrook.edu){:target="_blank"} if you want to discuss this topic! The pre-print of this paper can be downloaded as a PDF from below: 

#### <center><a href = "{{site.baseurl}}/documents/cchs.pdf" download>Pre-Print</a></center>