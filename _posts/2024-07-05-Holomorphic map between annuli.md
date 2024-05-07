---
title: 'HOLOMORPHIC MAP BETWEEN ANNULI'
date: 2024-05-07
permalink: /posts/2022/06/complex-annuli
categories:
  - Complex Analysis
  
---

First, we define an annulus in a complex plane
>**Definition:** An annulus in $\mathbb{C}$ is the set $$A(r,R) = \left\lbrace z \in \mathbb{C}: r < \left|z\right| <R \right\rbrace$$

Given two annuli $A_1 = A(r_1, R_1)$ and $A_2 = A(r_2, R_2)$, one may ask under which conditions
that two annuli are biholomorphic. It turns out that in a complex plane, the biholomorphic relation is defined using only
the ratio $r_1/r_2$ and $R_1/R_2$. This is shown in the following theorem

>**Theorem:** $A_1$ is biholomorphic to $A_2$ if and only if $\dfrac{R_1}{r_1} = \dfrac{R_2}{r_2}$.

**Proof:**

First suppose that $\dfrac{R_1}{R_2} = \dfrac{r_1}{r_2} =k$. Then clearly the linear map $f(z)=kz$
  is a biholomorphic map and $f(A_1) = A_2$. Thus $A_1$ is biholomorphic to $A_2$.

  Conversely, assume that $A_1$ is biholomorphic to $A_2$ under a map $f$. By scaling, we could further assume that $r_1=r_2=1$. Thus now we need to show that $R_1=R_2$.
  Fix some $1<r<R_2$ and let $C = \left\lbrace z \in A_2 \colon \|z\|=r\right\rbrace$.

  Since $f^{-1}$ is a continuous map, $f^{-1}(C)$ is a compact set. Thus we can find
  an $m>0$ such that $|x| \ge m$ for all $x \in f^{-1}(C)$. Choose $\delta>0$ small enough
  such that $1+\delta<m$. This implies the annulus $A_3 = A(1,1+\delta) \cap f^{-1}(C)=\emptyset$. Let
  $V = f(A_3)$. Since $A_3$ is connected set, so is $f(A_3)$. Thus $V$ is either inside
  $A_2\setminus A(1,r)$ or $A(1,r)$. By replacing $f$ with $R_2/f$, we can reduce to consider the former case.

  **Claim:** $\|f(z_n)\| \to 1$ whenever $\|z_n\| \to 1$.

  The claim can be proved as follows: Clearly we have $z_n = f^{-1}(f(z_n))$. If $f(z_n)$ converges to some points
  in $A_2$, $z_n$ must then converges to some points in $A_1$, contradicting the hypothesis that
  $\|z_n\| \to 1$. Thus $\|f(z_n)\|$ must converge to either $1$ or $R_2$, but the latter case is excluded as $V \subset A(1,r)$.

  In the same manner, we also have the following claim:

  **Claim:** $\|f(z_n)\| \to R_2$ whenever $\|z_n\| \to R_1$.

  Now set $\alpha = \log(R_1)/\log(R_2)$ and define a new function $g \colon A_1 \to \mathbb{R}$ by

  $$g(z) = \log\|f(z)\|^2 - \alpha\log\|z\|^2 = 2(\log\|f(z)\| - \alpha\log\|z\|).$$
  This is a harmonic function since $\log(\|f\|^2)$ is a harmonic over $\mathbb{C}$, where $f$ is a non vanishing analytic function. Indeed, we have

  $$\Delta\left(\log(\|f\|^2)\right)= \Delta\left(\log(f)+\log(\overline{f})\right)
    = 4\dfrac{\partial}{\partial z}\dfrac{\partial}{\partial \overline{z}}\log(f)+4\dfrac{\partial}{\partial \overline{z}}\dfrac{\partial}{\partial z}\log(\overline{f})=0$$

  Using the above claims, $g$ can be
  extended continuously to $\overline{A_1}$ and $g(z)=0$ for all $z \in \partial A_1$. By maximum
  modulus theorem for harmonic function, $g$ must be identically zero on the whole disk $\overline{A_1}$.
  In particular

  $$0 = \dfrac{\partial g}{\partial z} = \dfrac{f'(z)}{f(z)}-\dfrac{\alpha}{z}.$$

  Let $\gamma = \gamma(t)= ce^{it}$ for some $1<c<R_1$. Then we have
  
  $$\alpha = \dfrac{1}{2\pi i}\int_{\gamma}\dfrac{\alpha}{z} =\dfrac{1}{2\pi i}\int_{\gamma}\dfrac{f'(z)}{f(z)} $$

  By the Argument Principle, $\alpha$ must be an integer. A consequence is that
  
  $$\dfrac{d}{dz}(z^{-\alpha}f(z))= -\alpha z^{-\alpha-1}f(z)+z^{-\alpha}f'(z) = z^{-\alpha-1}(zf'(z)-\alpha f(z))=0.$$

  This forces $z^{-\alpha}f(z)=K$ for some constant $K$ on $A_1$. Thus $f(z)=Kz^{\alpha}$. As f is injective, $\alpha=1$ by the fundamental theorem of Algebra. $\square$