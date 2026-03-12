\documentclass[10pt]{article}

% --------- FORMAT PAGE ----------
\usepackage[a4paper,landscape,margin=1.5cm]{geometry}
\setlength{\columnsep}{0.5cm}
\usepackage{multicol}

% --------- LANGUE ----------
\usepackage[french]{babel}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}


% --------- MATHS ----------
\usepackage{amsmath, amssymb, amsfonts}

% --------- COULEURS + BOX ----------
\usepackage[most]{tcolorbox}
\usepackage{xcolor}

\definecolor{mainred}{RGB}{140,140,140}
\definecolor{subred}{RGB}{180,20,20}
\definecolor{subred2}{RGB}{255,220,220}
\definecolor{lightred}{RGB}{220,220,220}
\definecolor{maingreen}{RGB}{100,200,100}
\definecolor{lightgreen}{RGB}{150,245,170}
% Box principale
\newtcolorbox{demonstration}[1][]{
    colback=lightred,
    colframe=mainred,
    fonttitle=\bfseries,
    title=#1,      
    arc=0pt,
}
\newtcolorbox{correction}[1][]{
    colback=lightgreen,
    colframe=maingreen,
    fonttitle=\bfseries,
    title=#1,      
    arc=0pt,
}
\newtcolorbox{indication}[1][]{
    colback=subred2,
    colframe=subred,
    fonttitle=\bfseries,
    title=#1,
    arc=0pt,
    fontupper=\small
}
% Box remarque
\newtcolorbox{remarque}{
    colback=yellow!15,
    colframe=orange,
    arc=1pt,
}


% --------- TYPO PLUS MODERNE ----------
\usepackage{lmodern}
\usepackage{microtype}

% --------- PAS D'INDENTATION ----------
\setlength{\parindent}{0pt}

% --------- DOCUMENT ----------
\begin{document}

\begin{center}
    \begin{demonstration}
    {\LARGE \bfseries Démonstrations importantes : Réels}    
    \end{demonstration}
\end{center}

\vspace{0.3cm}

\begin{multicols}{2}
\begin{minipage}{\linewidth}

\begin{demonstration}[Exercice 3.20]
1) Par contraposée :\\
On suppose que $A \cup B \neq E$, il existe alors 
$x \in E\setminus{A\cup B}$.
\\Alors $x \notin A, x\notin B$ donc $\{x\}\cap A = \emptyset$
et $\{x\}\cap B = \emptyset$.
\\ 

\end{demonstration}    
\begin{demonstration}[Exercice 5.7]
Méthode 1 :\\ 
$x=\lfloor{x}\rfloor + \{x\}$,
\\ 
$\lfloor nx \rfloor = \lfloor n \lfloor x \rfloor + n \{x\} \rfloor
= n \lfloor x \rfloor +\lfloor n \{x\} \rfloor$
\\ Donc
$$\displaystyle{ \lfloor \frac{\lfloor nx \rfloor}{n} \rfloor 
= \lfloor \lfloor x \rfloor +
 \frac{\lfloor n \{x\} \rfloor}{n}\rfloor 
= \lfloor x \rfloor + \lfloor \frac{\lfloor n \{x\} \rfloor}{n} \rfloor
 }
 $$
Or, $0 \leq \{x\} < 1 $, $0\leq n\{x\}< n$,
\\ Donc, $0 \leq \lfloor n \{x\} \rfloor < n $
Ainsi, $\displaystyle {0 \leq \frac{\lfloor n \{x\} \rfloor}{n}< 1}$. $\square$


\end{demonstration}

\begin{indication}[Intuitions / Remarques]
On utilise 
\end{indication}
\begin{demonstration}[Exercice 20]
Soit $x_0 \in \mathbb{R}$ tel que 
$f \circ f (x_0)=x_0$. On pose
$g:x \rightarrow f(x) -x$, continue sur $\mathbb{R}$
comme somme de fonctions continues. 
\\ > Si $f(x_0)=x_0$ alors c'est bon ! 
\\ > Sinon, supposons que $f(x_0)<x_0$, (l'autre cas étant symétrique)
alors, on a : 
$$g(f(x_0))=f \circ f(x_0) - f(x_0) = x_0 - f(x_0) > 0 $$
$$ g(x_0) = f(x_0)-x_0 < 0$$
Comme $g$ est continue sur $]f(x_0),x_0[$ et que
$g(x_0)g(f(x_0))<0$, en vertu du théorème des
valeurs intermédiaires il existe $a \in ]f(x_0),x_0[$
tel que $$g(a)=0$$
C'est à dire : 
$$f(a)=a \square$$



\end{demonstration}

\end{minipage}

\begin{demonstration}
On pose 
\begin{equation} f:x\rightarrow\left\{
\begin{aligned}
  1 &\text{ si } x\leq0 \\
  -1 &\text{ sinon } 
\end{aligned}
\right. 
\end{equation}
f n'admet pas de point fixe, étant strictement positive 
sur les négatifs et strictement négative sur les positifs.
Cependant, $f \circ f$ admet un point fixe, 
en effet, $$f \circ f(-1) = f(f(-1)) =f(1) = -1$$
\end{demonstration}

\begin{demonstration}[Bourringan]
    Soit $z \in \mathbb{C}, |z| \neq 1$, une racine de $P$, existant
    par le théorème de d'Alembert-Gauss, car $P \neq (X-1)^n$.
    \\
    Supposons par l'absurde que $|z|>1$.
    \\
    On a alors, $$P(z)=0$$
    $$nz^n - \sum_{k=0}^{n-1}z^k=0 $$
    \begin{indication}
        $$\sum_{k=0}^{n-1}z^n = \sum_{k=0}^{n-1}z^k$$    
    \end{indication}
    Or, comme $|z| > 1$, pour tout $k\in [|0,n-1|]$
    $|z|^n>|z|^k$, il vient que : 
    $$\sum_{k=0}^{n-1}|z|^n > \sum_{k=0}^{n-1}|z|^k $$
    Or, d'après la box rouge,  
    $$n|z^n|= \sum_{k=0}^{n-1}|z^n| = |\sum_{k=0}^{n-1}z^k| \leq \sum_{k=0}^{n-1}|z^k| $$
    $$\text{Donc : }\sum_{k=0}^{n-1}|z^k| \geq \sum_{k=0}^{n-1}|z|^n > \sum_{k=0}^{n-1}|z|^k $$
    $$\sum_{k=0}^{n-1}|z^k| > \sum_{k=0}^{n-1}|z|^k $$
Ce qui est absurde. 
\end{demonstration}
\vspace{0.3cm}


\end{multicols}

\end{document}
