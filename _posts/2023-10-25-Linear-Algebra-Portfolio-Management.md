---
title: 'Applications of Linear Algebra in Portfolio Management'
date: 2023-10-25
header-includes: |
    \usepackage{tikz,pgfplots}
permalink: /posts/2023/10/Linear-Algebra-Portfolio-Management/
tags:
  - Linear Algebra
  - Portfolio Management
#  - category2

---
<!---
%<script
 % src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
%  type="text/javascript">
%</script>
--->
Linear algebra is a branch of mathematics developed to solve a system of linear equations and has found many applications in applied sciences- computer science(image processing) and mathematical finance(portfolio management).  In this article, we shall compute standard deviation of a portfolio using tools from linear algebra. Before we jump to this computation it is good to recall certain basic concepts from linear algebra.

### Linear Algebra Basics




### Standard Deviation of a Portfolio

For the sake of demonstration, let us suppose that our portfolio consists of two securities $A_1$ and $A_2$ whose returns, standard deviation and weights in the portfolio are summarized in the following table.

| Asset    | Weight    | Std. Deviation(%)| Return(%)   | 
|------------|-------------|------------------------|-----------------|
|Asset1   |$x_1$  |$\sigma_1$       |$r_1$            |
|Asset2   |$x_2$  |$\sigma_2$       |$r_2$            |

The portfolio return ($r$) is the weighted average of the individual asset returns. It is given by
\begin{equation}
	r = x_1r_1 + x_2r_2.
\end{equation}

On the other hand, the standard deviation or the volatility ($\sigma$) of the portfolio is given by
\begin{equation}\label{formula}
	\sigma = \left(x_1^2 \sigma_1^2 + x_2^2 \sigma_2^2 + 2\rho_{12}(x_1 \sigma_1)(x_2 \sigma_2)\right)^{\frac{1}{2}}
\end{equation}
where $\rho_{12}$ is the correlation between assets $A_1$ and $A_2$. 

At this juncture we make an important observation that is essential in developing general case of $n$ assets in the portfolio. We note that $\sigma^2$ is expressed as a quadratic form given by

$$
\sigma^2 =  \begin{pmatrix} 
	x_{1} & x_{2}
\end{pmatrix}
\begin{pmatrix} 
	\sigma_{1}^2 & \sigma_{1}\sigma_{2}\rho_{12} \\
	\sigma_{1}\sigma_{2}\rho_{12} & \sigma_{2}^2
\end{pmatrix}
\begin{pmatrix} 
	x_{1} \\
	x_{2}
\end{pmatrix}
\label{QF}$$

On the right hand side of the above expression, sandwiched between the weights vectors is the variance-covariance matrix. As far as the computation is concerned, the expression \eqref{QF} is more helpful than \eqref{formula}.

When we have $n$ assets ($A_1, A_2, \dots, A_n$) in the portfolio, the portfolio variance, $\sigma^2$ is given by the quadratic form
\begin{equation}\label{formula2}
	\sigma^2 =  \sum_{i=1}^{n}x_i^2\sigma_i^2 + 2 \sum_{i=1}^{n} \sum_{\substack{j=1, \\ j\neq i}}^{n}   \rho_{ij} (x_i \sigma_i) (x_j\sigma_j)
\end{equation}
Now, what is the symmetric positive definite matrix defining this quadratic form? The answer is variance-covariance matrix. To elaborate on this, consider the matrix S defined by

$$
	S = \begin{pmatrix} 
	\sigma_{1} & & \\
    	& \ddots & \\
        & & \sigma_{n}
	\end{pmatrix}
$$

where $\sigma_i$ is the standard deviation of an asset $A_i$. Note that $S$ is diagonal matrix with $S_{ii} = \sigma_i$ and $S_{ij} = 0$ for $i\neq j$. The matrix $S$ contains standard deviations of each asset as its diagonal entries. 

Next, consider the correlation matrix $C$ defined by

$$
	C = \begin{pmatrix} 
	1                  & \rho_{12} & \dots         &  \rho_{1n} \\
	\rho_{21} & 1                  & \dots         &  \rho_{1n} \\
    	\vdots          & \ddots          & \dots         & \vdots        \\
        \rho_{n1}     & \dots          &  \rho_{nn-1} & 1
	\end{pmatrix}.
$$

The variance-covariance matrix (V) is then given by

$$
	V = S \times C \times S.
$$

Subsequently, the portfolio variance is expressed as

$$
	\sigma^2 = 
	\begin{pmatrix} 
		x_{1} & x_{2} & \dots & x_n
	\end{pmatrix}
	V
	\begin{pmatrix} 
		x_{1} \\
		x_{2}\\
		\vdots\\
		x_n
	\end{pmatrix}

$$



















