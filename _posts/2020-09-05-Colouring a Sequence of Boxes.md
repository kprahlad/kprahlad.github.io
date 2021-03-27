---
layout: post
title:  Colouring a Sequence of Boxes
date:   2020-09-05
image:  
tags:   ["Random Problems", "Academics"]
---
One of my friends was applying to Google for a job and got this problem  in one of the final written rounds. This was a fun little problem that  helped me procrastinate...  

**Problem.** We are given a sequence of finitely many  boxes, say \\(b\_1, b\_2 \dots b\_n\\), where each box is coloured black or  white. We can perform two operations on these boxes:

1. Reverse the colour of the box.
2. Place the first \\(k\\) many boxes (where \\(k < n\\)) after the last box in the same order.

 The second operation can be performed at most once. We are required to  find the least number of times that we need to perform the first  operation such that no two neighbouring boxes have the same colour.

**Solution.** Let the two sequences of length \\(n\\) defined on \\(\\{0,1\\}\\) which have no two consecutive elements which are equal be \\(v\_1 = (0,1,0 \dots)\\)  and \\(v\_2 = (1,0,1 \dots)\\). We define \\(H(u,v)\\) (the *Hamming distance* between two vectors) as the number of bits where \\(u\\) and \\(v\\) differ for any two \\(n\\)-length bit vectors \\(u\\) and \\(v\\). Label a box with \\(1\\) if it black and with \\(0\\) otherwise. Let \\(\alpha\_i\\) denote the  \\(n\\)-length bit vector corresponding to \\(b\_i, b\_{i+1}, \dots b_n, b\_1, b\_2, \dots b\_{i-1}\\). Thus, our problem reduces to finding the \\(min\_{i,j}  H(\alpha\_i,v\_j)\\) where \\(1 \leq i \leq n\\) and \\(j \in \\{1,2\\}\\). Since the time taken to compute the hamming distance between two \\(n\\)-length bit vectors is \\(\mathcal{O}(n)\\) and there are \\(n\\) many  \\(\alpha\_i\\)s and constant many \\(v\_j\\)s to check, a straightforward  algorithm which checks all these possibilities solves this in  \\(\mathcal{O}(n^2)\\) time.

We can do better and produce a linear  time algorithm by using a recurrence relation to derive  \\(H(\alpha\_{i+2},v\_j)\\) from \\(H(\alpha\_i,v\_j)\\) for all \\(i \leq n-2\\)  and \\(j \in \\{1,2\\}\\). We take two cases: when \\(n\\) is even and when  \\(n\\) is odd.

*Case 1:* \\(n\\) *is even.* 

In this  case, \\(v\_1 = (0,1,0 \dots 0, 1)\\) and \\(v\_2 = (1,0,1 \dots, 1, 0)\\).  Note that \\(H(\alpha\_i,v\_j)\\) is equal to either \\(H(\alpha\_1,v\_1)\\) or  \\(H(\alpha\_1,v\_2)\\) for any \\(i \leq n\\) and \\(j \in \\{1,2\\}\\). We  compute these two quantities and report the smaller one in  \\(\mathcal{O}(n)\\) time.

*Case 2:* \\(n\\) *is odd.*  

In this case, \\(v\_1 = (0,1,0 \dots 1, 0)\\) and \\(v\_2 = (1,0,1 \dots, 0,  1)\\). Unfortunately, \\(H(\alpha\_i,v\_j)\\) may not be equal to either  \\(H(\alpha\_1,v\_1)\\) or \\(H(\alpha\_1,v\_2)\\) for an arbitrary \\(i \leq n\\) and \\(j \in \\{1,2\\}\\). Thus, we have to compute all \\(H(\alpha\_i,v\_j)\\) for each \\((i,j)\\) pair. We take \\(j=1\\) and repeat the same procedure  for \\(j=2\\). Note that the possible difference in the hamming distance  between \\(H(\alpha\_{i+2},v\_1)\\) from \\(H(\alpha\_i,v\_1)\\) will arise  because of the \\(b\_i\\) and \\(b\_{i+1}\\) boxes. Thus, to compute  \\(H(\alpha\_{i+2},v\_1)\\) we just need to compute the difference between  \\(H(\alpha'\_{i+2},(b\_i,b\_{i+1}))\\) and \\(H(\alpha'\_i,(b\_i,b\_{i+1}))\\)  and add it to \\(H(\alpha\_i,v\_1)\\) where \\(\alpha'\_i\\) is the vector  corresponding to the \\((b\_i,b\_{i+1})\\) boxes in \\(\alpha\_i\\).  \\(\alpha'\_{i+2}\\) is defined similarly. For each \\(i\\), this takes  constant time. Thus, given the values of \\(H(\alpha\_1,v\_1)\\) and  \\(H(\alpha\_2,v\_1)\\) (which can be computed in linear time), we can find  the values of \\(H(\alpha\_i,v\_1)\\) for any \\(i \leq n\\) in linear time.  Thus, \\(H(\alpha\_i,v\_j)\\) can be computed in linear time for any  \\((i,j)\\) pair.

A sketch of the algorithm is given below.

- Take \\(n\\) and \\(\alpha\_1\\) as the input
- Compute \\(\alpha\_2\\)
- Define \\(prev\_{\gamma\_1}\\) and \\(prev\_{\gamma\_2}\\) as the first two indices of \\(\alpha\_1\\) and \\(\alpha\_2\\)
- Define \\(v'\_1\\) and \\(v'\_2\\) as the first two indices of \\(v\_1\\) and \\(v\_2\\)
- Compute \\(H(\alpha\_1,v\_1)\\), \\(H(\alpha\_2,v\_1)\\), \\(H(\alpha\_1,v\_2)\\) and \\(H(\alpha\_2,v\_2)\\)
- \\(i \leftarrow 1\\)
- \\(prev\_{H1} \leftarrow H(\alpha\_1,v\_1)\\), \\(prev\_{H2} \leftarrow H(\alpha\_1,v\_2)\\)
- \\(curr\_{H1} \leftarrow H(\alpha\_1,v\_1)\\), \\(curr\_{H2} \leftarrow H(\alpha\_1,v\_2)\\)
- \\(min\_1 \leftarrow H(\alpha\_1,v\_1)\\), \\(min\_2 \leftarrow H(\alpha\_1,v\_2)\\)
- **if** \\(n\\) is even, compute the smaller of the above two values and **return** that
- **while** \\(i \leq n\\) **do**
  - Define \\(curr\_{\gamma\_1}\\) and \\(curr\_{\gamma\_2}\\) to be  the vector corresponding to the \\(b\_i\\) and \\(b\_{i+1}\\) boxes of  \\(\alpha\_1\\) and \\(\alpha\_2\\) respectively
  - \\(curr\_{H1} \leftarrow prev\_{H1} - H(prev\_{\gamma\_1},v'\_1) + H(curr\_{\gamma\_1},v'\_1)\\)
  - \\(curr\_{H2} \leftarrow prev\_{H2} - H(prev\_{\gamma\_2},v'\_2) + H(curr\_{\gamma\_2},v'\_2)\\)  
  - **if** \\(curr\_{H1} < min\_1\\) **then** \\(min\_1 \leftarrow curr\_{H1}\\) and **if** \\(curr\_{H2} < min\_2\\) **then** \\(min\_2 \leftarrow curr\_{H2}\\)
  - \\(i \leftarrow i+2\\)

- Repeat the previous loop starting from \\(i=2\\) this time
- Compute the smaller of \\(min\_1\\) and \\(min\_2\\) and **return** that