---
title: 'Generating Random Variables'
date: 2023-12-13
header-includes: |
    \usepackage{amsthm}
permalink: /posts/2023/12/2023-12-13-Generating-Random-Variables/
tags:
  - Computational Statistics
#  - category2

---
<style>
	.theorem {
  	display: block;
  	font-style: italic;
 	font-size: 20px;
  	font-family: "Monospace";
  	color: black;
  	border-radius: 10px;
  	background-color: rgba(240,255,240,255);
  	box-shadow: 5px 10px 8px #888888;
	}
	.theorem::before {
  	content: "Theorem. ";
  	font-weight: bold;
  	font-style: normal;
  	display: inline-block;
  	width: -webkit-fill-available;
  	color: black;
  	border-radius: 10px 10px 0 0;
  	%padding: 10px 5px 5px 15px;
  	background-color: rgb(240,255,240); %rgb(38, 38, 134);
	}
	.theorem[text]::before {
  	content: "Theorem (" attr(text) ") ";
	}
	.theorem p {
  	padding: 15px 15px 15px 15px;
	}
</style>

In this post, we will look at various methods for generating random variates. It goes without saying that simulation of random variables from specified probability distribution is one of the fundamental tools in computational statistics.

### 1. The Inverse Transform Method

This method is based on an important observation stated below:
		
<div class="theorem" text='Probability Integral Transform'>
	If $X$ is a continuous random variable with cdf (cumulative distribution function) $F_X(x)$, then $U = F_X(X) \sim Uniform(0,1).$ 
</div>
<br />
It is easy to observe this fact empirically 



















