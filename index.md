---
layout: default
title: Suites
---

# Exercice

Soit $z \in \mathbb{C}, |z| \neq 1$, une racine de $P$, existant
par le théorème de d'Alembert-Gauss, car $P \neq (X-1)^n$.

Supposons par l'absurde que $\vert z\vert>1$.

On a alors, $$P(z)=0$$
$$nz^n - \sum_{k=0}^{n-1}z^k=0$$ $$\sum_{k=0}^{n-1}z^n = \sum_{k=0}^{n-1}z^k$$   
Or, comme $|z| > 1$, pour tout $k\in [|0,n-1|]$
$|z|^n>|z|^k$, il vient que : 
$$\sum_{k=0}^{n-1}|z|^n > \sum_{k=0}^{n-1}|z|^k $$
Or, d'après la box rouge,  
$$n|z^n|= \sum_{k=0}^{n-1}|z^n| = |\sum_{k=0}^{n-1}z^k| \leq \sum_{k=0}^{n-1}|z^k| $$
$$\text{Donc : }\sum_{k=0}^{n-1}|z^k| \geq \sum_{k=0}^{n-1}|z|^n > \sum_{k=0}^{n-1}|z|^k $$
$$\sum_{k=0}^{n-1}|z^k| > \sum_{k=0}^{n-1}|z|^k 
$$
Ce qui est absurde. 