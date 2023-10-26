---
title: 'Applications of Linear Algebra in Portfolio Management'
date: 2023-10-25
permalink: /posts/2023/10/Linear-Algebra-Portfolio-Management/
tags:
  - Linear Algebra
  - Portfolio Management
#  - category2

header-includes: |
    \usepackage{tikz,pgfplots}
    \usepackage{fancyhdr}
    \pagestyle{fancy}
    \fancyhead[CO,CE]{This is fancy}
    \fancyfoot[CO,CE]{So is this}
    \fancyfoot[LE,RO]{\thepage}
abstract: This is a pandoc test with Markdown + inline LaTeX
---

%<script
 % src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
%  type="text/javascript">
%</script>

Linear algebra is a branch of mathematics developed to solve a system of linear equations and has found many applications in applied sciences- computer science(image processing) and mathematical finance(portfolio management).  In this article, we shall compute standard deviation of a portfolio using tools from linear algebra. Before we jump to this computation it is good to recall certain basic concepts from linear algebra.

### Linear Algebra Basics




### Standard Deviation of a Portfolio

For the sake of demonstration, let us suppose that our portfolio consists of two securities $$A_1$$ and $$A_2$$ whose returns, standard deviation and weights in the portfolio are summarized in the following table.

| Asset    | Weight    | Std. Deviation(\%) | Return(\%)       | 
|------------|-------------|--------------------------|---------------------|
|Asset1   |$$x_1$$  |$$\sigma_1$$         |$$r_1$$            |
|Asset2   |$$x_2$$  |$$\sigma_2$$         |$$r_2$$            |



\begin{tikzpicture}
\begin{axis}
\addplot[color=red]{exp(x)};
\end{axis}
\end{tikzpicture}
%Here ends the furst plot
\hskip 5pt
%Here begins the 3d plot
\begin{tikzpicture}
\begin{axis}
\addplot3[
    surf,
]
{exp(-x^2-y^2)*x};
\end{axis}
\end{tikzpicture}