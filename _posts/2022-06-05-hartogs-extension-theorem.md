---
title: 'Hartogs extension theorem'
date: 2022-06-05
permalink: /posts/2022/06/hartogs-extension-theorem
tags:
  - Several complex variables
  - Complex geometry
---

> **_Hartogs Extension Theorem:_** Let $f$ be an analytic function on the neighborhood of the closed unit disk such that $\|f\| \lt 1$ on the boundary. Show that $f$ has a unique fixed point. 

The reason I wrote this note because I made a stupid mistake on MSE and provided an incorrect solution, so I am writing down it here to remind myself. 


**Proof**: 

Consider the function $\psi(z) = f(z)-z$. Then clearly we have 

$$|\psi(z)+z| = |f(z)-z+z|= |f(z)| < 1 = |z|$$

on the curve $\gamma = \partial B(0,1)$. By Rouche's theorem, $\psi(z)$ and $z$ has the same number of solution inside the unit disk $B(0,1)$. This implies immediately that $f$ has a unique fixed point. 

What happens if we instead have $|f(z)| \le 1$? In this case we then are able to show that the number of fixed points is either 0 or 1. The upper bound of the number of point follows from the following lemma:

Lemma: Let $f: B(0,1) \to B(0,1)$ be an analytic map. If $f$ has two fixed point, then $f$ is identity map. 

Proof:  Assume that $f(a)=a \in B(0,1)$. Then we consider the map

$$
\phi_a(z) = \frac{a-z}{1-\overline{a}z}
$$

The map $\phi_a$ is a biholomorphic map on the unit disk, and $\phi_a \circ f \circ \phi_{a} : B(0,1) \to B(0,1)$ is a map that maps origin to origin and has another fixed point (Verify this!). By Schwarz's lemma, which says that if $|f(z)|=|z|$ for some non-zero $z$ inside the unit disk, then $f$ is a rotation, we can conclude that $\phi_a \circ f \circ \phi_{a}(z)$ is a rotation. But the fact that it has a non-zero fixed point then $f$ must be the identity map. ☺ 

Now comeback to out question:First we could see that $f(B(0,1) \subset B(0,1)$ by maximum modulus theorem.  If it has 1 fixed point, then we are done. Now we need to construct an example where it has no fixed point. Note that, the unit disk is biholomorphic to the upper half complex plane, and the map $g(z) = z+1$ has no fixed point on the upper half plane, so there exists a self-map on $B(0,1)$ that has no fixed point. $\square$