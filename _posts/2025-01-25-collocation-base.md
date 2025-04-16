---
layout: post
title: collocation and Gauss quadrature
date: 2025-01-25 12:12:00+0800
description: collocation and Gauss quadrature
tags: formatting math
categories: collocation
related_posts: false
---

# Gauss and Radau IIA Quadrature Formulas

## Gauss Quadrature

### Orthogonal Polynomials

Let $ P_n(x) $ be the Legendre polynomials orthogonal on $[-1,1]$ with weight function $ w(x) \equiv 1 $:

$$
\int_{-1}^1 P_m(x)P_n(x)dx = \frac{2}{2n+1}\delta_{mn}
$$

The Rodrigues' formula gives:

$$
P_n(x) = \frac{1}{2^n n!}\frac{d^n}{dx^n}\left[(x^2-1)^n\right]
$$

### Quadrature Nodes

The Gauss nodes $x_k$ are the roots of $ P_n(x) $:

$$
P_n(x_k) = 0,\quad k=1,\dotsc,n
$$

These roots satisfy:
- **Symmetry**: $ x_k = -x_{n+1-k} $
- All roots are simple and lie in $(-1,1)$

### Quadrature Weights

The weights are given by:

$$
w_k = \int_{-1}^1 \prod_{\substack{j=1\\j\neq k}}^n \frac{x-x_j}{x_k-x_j} dx = \frac{2}{(1-x_k^2)[P_n'(x_k)]^2}
$$

---

## Radau IIA Quadrature

### 和Legendre多项式的关系

$$
R_n(x) = P_n(x) - P_{n-1}(x)
$$

### Radau right polynomial

$$
\frac{d^n}{dx^n}\left[(x+1)^n (x-1)^{n+1}\right] 
$$

### Quadrature Nodes

The Radau IIA nodes $x_k$ consist of:
- The root $ x=1 $
- The roots of $ R_{n-1}(x) $ in $(-1,1)$

### Quadrature Weights

Weights are determined by:

$$
w_k = \int_{-1}^1 \ell_k(x)dx,\quad \ell_k(x)
$$

### [Lobatto积分](https://en.wikipedia.org/wiki/Gaussian_quadrature#Gauss%E2%80%93Lobatto_rules)是先分部积分，然后使用Gauss-Legendre求解公式吗？

Lobatto quadrature of function $f(x)$ on interval $[-1,1]$ : 

$$
\int_{-1}^1 f(x) d x=\frac{2}{n(n-1)}[f(1)+f(-1)]+\sum_{i=2}^{n-1} w_i f\left(x_i\right)+R_n
$$


Abscissas: $x_i$ is the $(i-1)$ st zero of $P_{n-1}^{\prime}(x)$, here $P_m(x)$ denotes the standard Legendre polynomial of $m$-th degree and the dash denotes the derivative.

Weights:

$$
w_i=\frac{2}{n(n-1)\left[P_{n-1}\left(x_i\right)\right]^2}, \quad x_i \neq \pm 1
$$


## Properties Comparison

| Property            | Gauss       | Radau IIA   |
|---------------------|-------------|-------------|
| Nodes               | All interior| Contains $ x=1 $ |
| Degree of exactness | $ 2n-1 $  | $ 2n-2 $  |
| Node symmetry       | Yes         | No          |