---
layout: post
title: Wave-Equation
date: 2025-03-15 12:12:00+0800
description: 
tags: PDE
categories: PDE
related_posts: false
---


Lagrange [130] was the first to derive the wave equation as a first-order approximation of the water wave system, that is, the Euler equation with free boundary (also derived by him in [130]), in a linear, extremely long wave regime.

In one spatial dimension the wave equation reads as

$$
\frac{\partial^2 u(x, t)}{\partial t^2}=c^2 \frac{\partial^2 u(x, t)}{\partial x^2}
$$

where $c$ is the constant speed of the waves. D'Alembert gave the general solution of this equation in the form

$$
u(x, t)=f(x-c t)+g(x+c t)
$$

where $f$ and $g$ are two arbitrary twice differentiable functions of a single variable which are uniquely fixed by some initial equations, see Fig. 2.1 as an example. Clearly the initial data travel along the characteristics $x \pm$ ct without the waves changing form. This means the equation is not dispersive. Since the wave equation is linear, the wave packets are simply superposed when they pass through each other.

A convenient way to analyze the dispersive properties of linear PDEs is to use Fourier transforms $\hat{u}(k, \omega)=\int_{\mathbb{R}^2} u(x, t) \mathrm{e}^{i(k x-\omega t)} \mathrm{d} x$, which leads for the wave equation (2.3) to the dispersion relation $\omega(k)= \pm c k$. This means that the group velocity $v_g=\frac{\mathrm{d} \omega}{\mathrm{d} k}$ is constant. Thus an initial wave packet propagated by the wave equation is not dispersed and keeps its original shape. Both $f$ and $g$ in (2.4) describe traveling waves which are in this example localized in $x$ and thus solitary waves.