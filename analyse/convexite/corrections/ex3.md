---
layout: default
title: Exercice 3 - Convexité
---
# Exercice 3 - Convexité 

Il existe $a<b$ tels que $f(a)<f(b)$.
Pour $x>b$, par inégalité des trois pentes.
$$
\displaystyle{\frac{f(x)-f(a)}{x-a}\geq\frac{f(b)-f(a)}{b-a}}
$$

ie 
$$

f(x)\geq \frac{f(b)-f(a)}{b-a}(x-a)+f(a)
$$

Par encadrement, ce dernier terme tend vers $+\infty$ donc
$\lim_{x \to \infty} f(x)=+\infty$
$\square$
