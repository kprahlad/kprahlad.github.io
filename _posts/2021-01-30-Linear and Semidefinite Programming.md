---
layout: post
title:  "Linear and Semidefinite Programming"
date:   2021-01-30
image:  
excerpt: Optimization has a very simple premise - you want to maximize or minimize something with respect to a bunch of constraints. In <i>Linear Programming</i>, we further restrict our study to the case where the constraints are also linear and the condition imposed on each of these functions is that they must be  at most a fixed value. In <i>Semidefinite Programming</i>, we impose another restriction - the matrix described by the variables must be positive (that is, it must be both positive semidefinite and self-adjoint or, equivalently, it must be a matrix whose eigenvalues are positive reals). For my 7<sup>th</sup> semester math project, I wrote a report that discusses these two optimiization constructs. The report assumes literacy in basic algorithms, linear algebra and (a tiny bit of) probability.
tags:   ["Academics","Reports"]
---

Optimization has a very simple premise: you want to maximize or minimize something with respect to a bunch of constraints. More precisely, you are looking to optimize (maximize or minimize) a real-valued function \\(f\\) on, say,  \\(R^n\\) subject to real-valued functions \\(f_1, f_2 \dots f_m\\) defined on \\(R^n\\) satisfying certain conditions. One of the more useful types of functions that we look to optimize are linear functions. In *Linear Programming*, we further restrict our study to the case where the constraints are also linear and the condition imposed on each of these functions is that they must be  at most a fixed value. More precisely, if we write a linear function on \\(R^n\\) as \\(a^Tx\\) for the corresponding vector \\(a \in R^n\\), we have:   

\\begin{align}
    &\\text{Optimize }  c^Tx \\text\{ subject to\}\\newline
    &(Ax)\_i \\leq b\_i \\text\{ for all \} 1 \\leq i \\leq m
\\end{align}

where \\(b = (b\_1,b\_2 \dots b\_m) \\in R^m\\), \\(c \\in R^n\\), and \\(A\\) is a matrix with \\(m\\) rows and \\(n\\) columns. In *Semidefinite Programming*, we impose another restriction: the matrix described by the variables must be positive (that is, it must be both positive semidefinite and self-adjoint or, equivalently, it must be a matrix whose eigenvalues are positive reals). That is, we deal with systems of the following type: 

\\begin{align}
    &\\text{Maximize or minimize}  \\sum^n\_{i,j=1} c\_{i,j}x\_{i,j} \\text{ subject to} \\newline
    &\\sum^n\_{i,j=1} a^{(k)}\_{i,j}x\_{i,j} = b\_k\\text{ for all } 1 \\leq k \\leq m \\newline
    &x\_{i,j} \\in R \\text{ for all } 1 \\leq i,j \\leq n \newline
    &X = (x\_{i,j}) \\text{ is a positive operator}
\end{align}

where \\(b\_k\\)​, \\(a^{(k)}\_{i,j}\\)​, \\(​c\_{i,j} \in R​\\) for all \\(1 \\leq i,j \\leq n\\), \\(1 \\leq k \\leq m\\).

This report discusses these two optimization constructs. In the first section, two computational problems are discussed in detail (the *Set Cover* problem and the *Maximum Flow* problem) to understand the use of linear programming in designing approximation algorithms. The second section is devoted to proving an import result: the *Strong Duality* theorem. This is done using *Farkas' Lemmas*. Finally, positive operators are discussed in the third section and is used in the fourth section to describe an approximation algorithm for the *Max-Cut* problem using semidefinite programming. I've done my best to iron out typos and avoid mistakes. If you find any typos, mistakes or just  want to talk about this topic, [email me](mailto:kprahlad.narasimhan@niser.ac.in)!

#### <center><a href = "{{site.baseurl}}/documents/Linear_and_Semidefinite_Programming.pdf" download> Report </a></center>