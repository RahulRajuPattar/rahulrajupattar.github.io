---
title: 'Generating Random Variables'
date: 2023-10-25
header-includes: |
    \usepackage{tikz,pgfplots}
permalink: /posts/2023/12/2023-12-13-Generating-Random-Variables/
tags:
  - Computational Statistics
#  - category2

---
In this post, we will look at various methods for generating random variates. It goes without saying that simulation of random variables from specified probability distribution is one of the fundamental tools in computational statistics.

### 1. The Inverse Transform Method

This method is based on an important observation stated below:
		
If $X$ is a continuous random variable with cdf (cumulative distribution function) $F_X(x)$, then $U = F_X(X) \sim Uniform(0,1).$ 
		
It is easy to observe this fact empirically 

```{theorem, label, name="Theorem name"}
Here is my theorem.
```

















