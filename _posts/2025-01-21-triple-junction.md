---
layout: post
title: a post with math
date: 2025-01-21 19:12:00+0800
description: an example of a blog post with some math
tags: formatting math
categories: sample-posts
related_posts: false
---

This theme supports rendering beautiful math in inline and display modes using [MathJax 3](https://www.mathjax.org/) engine. You just need to surround your math expression with `$$`, like `$$ E = mc^2 $$`. If you leave it inside a paragraph, it will produce an inline expression, just like $$ E = mc^2 $$.

To use display mode, again surround your expression with `$$` and place it as a separate paragraph. Here is an example:

$$
\sum_{k=1}^\infty |\langle x, e_k \rangle|^2 \leq \|x\|^2
$$

You can also use `\begin{equation}...\end{equation}` instead of `$$` for display mode math.
MathJax will automatically number equations:

\begin{equation}
\label{eq:cauchy-schwarz}
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
\end{equation}

and by adding `\label{...}` inside the equation environment, we can now refer to the equation using `\eqref`.

Note that MathJax 3 is [a major re-write of MathJax](https://docs.mathjax.org/en/latest/upgrading/whats-new-3.0.html) that brought a significant improvement to the loading and rendering speed, which is now [on par with KaTeX](http://www.intmath.com/cg5/katex-mathjax-comparison.php).

| 符号                   | 含义                        | 定义域                  |
|------------------------|-------------------------------------|-------------------------|
| $T_k$                | 第$k$个三重点              | $k=1,\ldots,I_T$|
| $s_j^k$              | $T_k$关联的第$j$个界面编号          | $j=1,2,3$|
| $b_{s_j^k}^\pm$      | 界面$\Gamma_{s_j^k}$的体域编号   |$\{1,\ldots,I_R\}$  |
| $R_\ell$         | 第$\ell$个体域                      | $\ell=1,\ldots,I_R$ |
| $\Gamma_i(t)$    | 第$i$个界面                         | $i=1,\ldots,I_S$    |