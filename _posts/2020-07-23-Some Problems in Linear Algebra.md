---
layout: post
title:  Some Problems in Linear Algebra
date:   2020-07-23
image:  
excerpt: I came across a couple of fun problems when I was going through <i>"<a href = "https://link.springer.com/book/10.1007/978-3-319-11080-6">Linear Algebra Done Right</a>"</i> by Axler. I really enjoyed this book and it was great for a "second reading" of the basics of Linear Algebra.
tags:   ["Problems", "Academics"]
---
I came across these problems when I was going through *"[Linear Algebra Done Right](https://link.springer.com/book/10.1007/978-3-319-11080-6)"* by Axler. I really enjoyed this book and it was great for a "second reading" of the basics of Linear Algebra.

**Problem 1.** Let \\(V\\) be an inner product space over \\(C\\) where \\(C\\) denotes the set of complex numbers. For \\(u,v \in V\\)  define \\(d(u,v) = \|\| u-v \| \|\\).

1. Prove that \\(d\\) is a metric on \\(V\\).
2. Prove that if \\(V\\) is finite-dimensional, \\(V\\) is a Hilbert space.
3. Prove that every finite-dimensional subspace of \\(V\\) is closed.

**Proof.** Part (1) of the problem follows from the definition of the norm. Now, assume that \\(V\\) is finite-dimensional. Thus, there exists an orthonormal  basis, say \\(B=\\{e_1, e_2, \dots e_m\\}\\), of \\(V\\). To prove that \\(V\\)  is a Hilbert space, it suffices to prove that the space is complete  since it is given to be an inner product space. Let \\(\\{x_n\\}\_n\\) be a  Cauchy sequence in \\(V\\). Since \\(B\\) is a basis of \\(V\\), each \\(x_n\\)  in the sequence can be written as \\(\sum\_{i=1}^m a_i^{(n)}e_i\\). Let  \\(y^{(i)}\\), where \\(1 \leq i \leq m\\), denote the complex sequence  \\(\\{a_i^{(n)}\\}\_n\\). We will prove that each of these sequences are  Cauchy sequences and using the completeness of \\(C\\), we will prove that \\(\\{x\_n\\}\_n\\) converges to a point in \\(V\\). Since \\(\\{x\_n\\}\_n\\) was  arbitrary, this will complete the second part of the problem. Let  \\(\epsilon > 0\\) be given. Since \\(\\{x\_n\\}\_n\\) is a Cauchy sequence,  there exists a natural number \\(M \\), such that for all \\(k,l \geq M\\)  where \\(k,l \\) are natural numbers, we have
\begin{align\*}
  &d(x\_k,x\_l) < \epsilon \\newline
  \implies&||x\_k - x\_l|| < \epsilon \\newline
  \implies&||\sum\_{i=1}^m (a\_i^{(k)} - a\_i^{(l)}) e\_i||^2 < \epsilon^2 \\newline
  \implies&\sum\_{i=1}^m (|a\_i^{(k)} - a\_i^{(l)}|^2 \cdot ||e\_i||^2) < \epsilon^2 & (\text{Pythagoras' Theorem})\\newline
  \implies&\sum\_{i=1}^m |a\_i^{(k)} - a\_i^{(l)}|^2 < \epsilon^2 \\newline
  \implies& |a\_i^{(k)} - a\_i^{(l)}| < \epsilon \text{ for any \\(i\\).} 
\end{align\*}
Thus, the sequence \\(y^{(i)}\\) is a Cauchy sequence in \\(C\\) for every \\(i\\). Since \\(C\\) is complete, this sequence converges to a point, say  \\(b\_i\\), in \\(C\\). Now, let \\(v\\) denote the vector in \\(V\\) which is  \\(\sum\_{i=1}^m b\_ie\_i\\). Now, the distance between a point \\(x\_n\\) of  the sequence and \\(v\\) is \\(||\sum\_{i=1}^m (a\_i^{(n)} - b\_i) e\_i|| \leq  \sum\_{i=1}^m |a\_i^{(n)} - b\_i|\\) by the triangle inequality. Since there are finitely many \\(y^{(i)}\\), we can choose a natural number \\(N\\)  such that \\(|a\_i^{(n)} - b\_i| < \epsilon/m\\) for all \\(n \geq N\\) and for all \\(i\\). Thus, \\(d(x\_n,v) < \epsilon\\) for all \\(n \geq N\\).  Since \\(\epsilon\\) was arbitrary, \\(\\{x\_n\\}\_n\\) converges to \\(v \in  V\\). Since the sequence itself was arbitrary, this proves the second  part of the problem. Using (2) and the fact that any complete metric  space is closed, the last part of the problem becomes straightforward.

**Problem 2.** Let \\(C\_{R}([-1,1])\\) denote the vector space of continuous real-valued  functions on the interval \\([-1,1]\\) with inner product given by
\\[\langle f,g \rangle = \int\_{-1}^{1} f(x)g(x) dx\\]
for \\(f,g \in C\_{R}[-1,1]\\). Let \\(U\\) be the subspace of \\(C\_{R}([-1,1])\\) defined by \\[U = \\{f \in C\_{R}([-1,1]) : f(0) = 0\\}\\]Prove that  \\(U^\perp = \\{0\\}\\).

**Proof.** Consider a function  \\(f \in U^\perp\\). Assume that \\(f(x) \neq 0\\) at some \\(x \in [-1,1]\\). Without loss in generality, we can assume that \\(f(x)>0\\) (if  \\(f(x)<0\\), then \\(-f \in U^\perp\\) evaluated at \\(x\\) is greater  than \\(0\\)). Then, since \\(f\\) is continuous, there exists an interval  containing \\(x\\), say \\((a,b)\\), such that \\(f\\) is positive in this  interval. Thus, there exists an interval \\((2p,2q) \subseteq (a,b)\\)  such that \\(0 \notin (2p,2q)\\). Let \\(l\_1(x)\\) denote the line joining  \\((2p,0)\\) and \\((0,1)\\) and \\(l\_2(x)\\) denote the line joining  \\((2q,0)\\) and \\((0,1)\\). Consider the function \\(g \in U\\) which is  defined as follows:
\\(g(x) = 0 \\) for \\(x \in [-1,2p) \cup [2q,1]\\); \\(g\\) agrees with \\(l\_1\\) and \\(l\_2\\) in \\([2p,p+q)\\) and \\([p+q,2q)\\) respectively. Thus, \\(f(x)g(x) \geq 0\\) for all \\(x\\) and is strictly greater than 0 in  \\((2p,2q)\\). Thus, \\(\langle f,g \rangle \neq 0\\) contradicting our  initial assumption that \\(f \in U^\perp\\). Thus, \\(U^\perp = \\{0\\}\\).

**Problem 3.** Let \\(R\\) denote the set of real numbers and \\(p\\) be a positive real.  Prove that there is an inner product on \\(R^2\\) such that the associated norm is given by \\(\|\| (x , y) \|\| = (x^p + y^p)^{\frac{1}{p}}\\) for all  \\(x , y \in R^2\\) if and only if \\(p = 2.\\)

**Proof.** If \\(p= 2\\), then \\(\|\| (x , y) \|\|\\) defined by \\((x^2 +  y^2)^{\frac{1}{2}}\\) is the usual \\(l\_2^{2}\\) norm on \\(R^{2}\\) and it  inherits a natural inner product defined as follows
\\[\text{for all} \;u = (u\_1,u\_2) \;\text{and} \;v = (v\_1,v\_2) \in R^2, \langle (u , v) \rangle := u\_1 v\_1 + u\_2 v\_2.\\]
 Now, for the converse, assume there is a inner product on \\(R^2\\) with the  given norm for some \\(p > 0\\). We prove that \\(p = 2\\).
 Consider  \\((0,-1) \in R^2\\) and assume \\(\|\| (0 , -1) \|\| = k\\). By definition,  \\(k\\) is a positive real. Substituting, we get that \\((-1)^p = k^p >  0\\). Since  \\(e^{\iota p\pi} = -1\\), we get that \\(\cos p\pi + i \sin  p\pi \in R\\). Thus, \\(\sin p\pi = 0\\) implying that \\(p\\) is an integer . Since \\(p > 0\\), this implies that \\(p \in N\\). Note that \\(\|\|  u+v \|\|^{2} + \|\| u-v \|\|^{2} = 2(\|\| u \|\|^{2} + \|\| v \|\|^{2} )\\) for all  \\(u,v \in R^2\\). On taking \\(u = (1,0)\\) and \\(v = (0 ,1)\\) we get that  \\(2^{\frac{2}{p}} +((1 + (-1)^p)^{\frac{2}{p}} = 4\\). The quantity \\(((1 + (-1)^p)^{\frac{2}{p}}\\) can be \\(0\\) or \\(2^{\frac{2}{p}}\\) depending on whether \\(p\\) is even or odd. If \\(p\\) is odd ,the above quantity is \\(0\\) and we have \\(2^{\frac{2}{p}} = 4\\) which implies that \\(p = 1\\). However, if \\(p = 1\\), we have \\(\|\| (0 , -1) \|\| = -1 < 0\\) which  doesn't satisfy the property of norm. Thus, \\(p\\) is not odd. If \\(p\\)  is even, then \\(2(2^{\frac{2}{p}}) = 4\\) implying that \\(p = 2\\). If  \\(p = 2\\), from the earlier part of the problem we already know this  defines an inner product.

**Problem 4.** Suppose  \\(v\_1, v\_2, \cdots v\_m\\) is linearly independent list in \\(V\\), a vector space over \\(C\\). Prove that there exists \\(w \in V\\) such that  \\(\langle w,v\_j \rangle > 0\\) for all \\(j \in \\{1,2, \cdots ,m\\}\\).

**Proof.** Let \\(U = span(v\_1, v\_2, \cdots v\_m)\\). Define \\(\varphi : U \rightarrow  C\\) by \\(\Sigma\_{i=1}^{m} \alpha\_i v\_i \mapsto \Sigma\_{i=1}^{m}  \alpha\_i\\). Now, \\(U\\) is a finite dimensional vector space over \\(C\\)  and \\(\varphi\\) is a linear functional on \\(U\\). By Riesz Representation Theorem, there is a unique vector \\(w \in U \subseteq V\\) such that  \\(\varphi(v) = \langle v,w \rangle\\) for all \\(v \in U\\). Note that  \\(\varphi(v\_j) = 1\\) for all \\(j \in \\{1,2, \cdots ,m\\}\\). Thus, for all \\(j\\), we have \\(\langle v\_j,w \rangle = 1 = \overline{1} = \langle  w,v\_j \rangle\\). Thus, \\(\langle w,v\_j \rangle > 0\\) for all \\(j \in \\{1,2, \cdots ,m\\}\\).