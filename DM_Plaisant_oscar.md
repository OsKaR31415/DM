---
title: D.M. de mathématiques
subtitle: option mathématiques expertes
author: Oscar Plaisant
documentclass: scrartcl
header-includes: |
   \usepackage[top=2cm, bottom=2.5cm, left=2cm, right=2cm]{geometry}
   \usepackage{enumitem}
---

# Exercice 82p243

## a)
On sait que :

$$A = \left( \begin{array}{cc} 0,995 & 0,005\\ 0,6 & 0,4 \end{array} \right)$$
$$P = \left( \begin{array}{cc} 1 & -1\\ 1 & 120 \end{array} \right)$$

On commence par chercher le déterminant de $P$.

$\left|P\right| = (1\cdot 120) - (1\cdot -1) = 121$

Puisque $\left|P\right| > 0$, on sait que $P$ est inversible, et on à :

$\begin{array}{rcl} P^{-1} & = & \dfrac{1}{\left|P\right|}\times\left( \begin{array}{cc} 120 & 1\\ -1 & 1 \end{array} \right) = \dfrac{1}{121}\times \left( \begin{array}{cc} 120 & 1\\ -1 & 1\end{array}\right)\\[4ex] & = & \left( \begin{array}{cc} \frac{120}{121} & \frac{1}{121}\\[1ex] -\frac{1}{121} & \frac{1}{121} \end{array} \right) \end{array}$

## b)
On a $D = P^{-1}AP$. Avec la calculatrice, on obtient $D = \left( \begin{array}{cc} 1 & 0\\[1ex] 0 & \frac{79}{200} \end{array} \right)$

## c)
On utilise une démonstration par réccurence.

On définit la proposition $P_n: A^n = PD^nP^{-1}$. On cherche donc à montrer que $\forall n\in \mathbb{N}^*, P_n$

##### Initialisation

Pour $n=1$, on a :

$$
\begin{array}{rcl}
P_n &\iff& P_1\\
&\iff& A^1 = PD^1P^{-1}\\
&\iff& A = PDP^{-1}\\
\end{array}
$$

Or, on a : $PDP^{-1} = \begin{array}{cc} 0,995 & 0,005\\ 0,6 & 0,4\end{array}$

On a donc bien $A = PDP^{-1}$, et $P_1$ est vraie.


##### Hérédité

On cherche a montrer que $\forall n\in\mathbb{N}^*, P_n \implies P_{n+1}$, soit que $\forall n\in\mathbb{N}^*, A^n=PD^nP^{n-1} \implies A^{n+1} = PD^{n+1}P^{-1}$.

Pour cela, on suppose que, pour $n$ fixé, $P_n$ est vraie, soit que $A^n = PD^nP^{-1}$.

On a donc:

$$
\begin{array}{rcl}
PD^{n+1}P^{-1} &=& PD^nDP^{-1}\\
               &=& PD^nP^{-1}APP^{-1}\\
               &=& PD^nP^{-1}A\\
               &=& A^nA\\
               &=& A^{n+1}
\end{array}
$$

On a donc bien $\forall n\in\mathbb{N}*, P_n\implies P_{n+1}$ 


##### Réccurence


Puisque $P_1$ est vraie et que $\forall n\in\mathbb{N}^*, P_n \implies P_{n+1}$, on peut dire que $P_n$ est vraie pour tout $n$ entier naturel positif.

On a donc bien, pour tout $n$ entier naturel positif, on a bien $A^n = PD^nP^{-1}$.

## d)

$D = \left( \begin{array}{cc} 1 & 0\\ 0 & 0,395\end{array} \right) = \left( \begin{array}{cc} 1 & 0\\ 0 & \frac{79}{200} \end{array} \right)$

$D^2 = \left( \begin{array}{cc} 1 & 0\\ 0 & \frac{6241}{40000}\end{array} \right)$

$D^3 = \left( \begin{array}{cc} 1 & 0\\ 0 & \frac{493 039}{8000000}\end{array} \right)$

On remarque que $\dfrac{6241}{40000} = \left( \dfrac{79}{200} \right)^2$ et que $\dfrac{493 039}{8 000 000} = \left( \dfrac{79}{200} \right)^3$.

On peut donc conjectuer que :

$D^n = \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^n \end{array} \right)$

Cette conjecture fonctionne également pour $n = 4$

Pour la démontrer, on utilise une démonstration par réccurence.

On définit $P_n: D^n = \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^n \end{array} \right)$

On cherche donc à montrer que $P_n$ est vraie pour tout $n$ entier naturel positif.

##### Initialisation

On veut montrer que $P_1$ est vraie.

$P_1 \iff D^1 = \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^1 \end{array} \right) \iff D = \left( \begin{array}{cc} 1 & 0\\ 0 & \frac{79}{200} \end{array} \right)$

Or, on sait que $D = \left( \begin{array}{cc} 1 & 0\\ 0 & \frac{79}{200} \end{array} \right)$, on peut donc dire que $P_1$ est vraie.

##### Hérédité

On cherche à démontrer que $P_n \implies P_{n+1}$, soit que :

$$
\forall n\in \mathbb{N}, D^n = \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^n \end{array} \right) \implies D^{n+1} = \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^{n+1} \end{array} \right)
$$

Pour cela, on suppose, pour $n$ fixé, que $P_n$ est vraie.

On a donc :

$\begin{array}{rcl} D^{n+1} &=& D^nD\\ &=& \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^n \end{array} \right) \left( \begin{array}{cc} 1 & 0\\ 0 & \frac{79}{200} \end{array} \right)\\ &=& \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^{n+1} \end{array} \right)\end{array}$


##### Réccurence

Puisque $P_1$ est vraie, et que $\forall n\in\mathbb{N}^*, P_n \implies P_{n+1}$, on peut dire que : $\forall n\in\mathbb{N}^*, P_n$, soit que :

$$\forall n\in\mathbb{N}^*, P_n, D^n = \left( \begin{array}{cc} 1 & 0\\ 0 & \left( \frac{79}{200} \right)^n \end{array} \right)$$

## e)

On a vu dans le c) que $A^n = PD^nP^{-1}$. On peut donc dire que :

$\begin{array}{rcl} A^n &=& PD^nP^{-1}\\ &=& \left( \begin{array}{cc} 1 & -1\\[1ex] 1 & 120 \end{array} \right) \left( \begin{array}{cc} 1 & -1\\[1ex] 0 & \left( \frac{79}{200} \right)^n \end{array} \right) \left( \begin{array}{cc} \frac{120}{121} & \frac{1}{121}\\[1ex] -\frac{1}{121} & \frac{1}{121} \end{array} \right)\\[5ex] &=& \left( \begin{array}{cc} 1 & -1-\left( \frac{79}{200} \right)^n\\ 1 & -1+120\left( \frac{79}{200} \right)^n \end{array} \right)\\[5ex] &=& \left( \begin{array}{cc} \frac{121\times 200^n + 79^n}{121\times 200^n} & -\frac{79^n}{121\times 200^n}\\[2ex] \frac{121\times 200^n - 120\times 79^n}{121\times 200^n} & \frac{120\times 79^n}{121\times 200^n}\end{array} \right)\end{array}$


$\frac{1}{121} \left( \begin{array}{cc} 120 + \left( \frac{79}{200} \right)^n & 1 - \left( \frac{79}{200} \right)^n\\[2ex] 120\left( 1 - \left( \frac{79}{200} \right)^n \right) & 1 + 120\left( \frac{79}{200} \right)^n \end{array} \right) 
= \left( \begin{array}{cc} \frac{120\times 200^n+79^n}{121\times 200^n} & \frac{200^n - 79^n}{121\times 200^n}\\[2ex] \frac{120\times 200^n - 120\times 79^n}{121\times 200^n} & \frac{200^n + 120\times 79^n}{121\times 200^n}\end{array} \right)$











# Exercice 90p245

## 1.

### a)

$\begin{array}{rcl}p_1 &=& 0,9\times p_0 + 0,4\times q_0\\ &=& 0,9\times 0 + 0,4\times 1\\ &=& 0,4\end{array}$

\hspace{1em}

$\begin{array}{rcl}q_1 &=& (1-0,9)\times p_0 + (1 - 0,4)\times q_0\\ &=& 0,1\times 0 + 0,6\times 1\\ &=& 0,6\end{array}$


### b)

Le programme pourrait etre écrit plus correctement comme suit :

```python
def F(n):
    p = 0
    q = 1
    for _ in range(n):
        p = 0.9 * p + 0.4 * q
        q = 1 - p
    p = round(p, 2)
    q = round(q, 2)
    return p, q
```

Si on appelle cette fonction avec `n = 4`, elle retournera le couple $p_4, q_4$.

## 2.

### a)

On pose $M = \left( \begin{array}{cc} a & b\\ c & d \end{array} \right)$, avec $a$, $b$, $c$ et $d$ réels.

On cherche donc maintenant $a, b, c$ et $d$ tels que :

$X_{n+1} = \left( \begin{array}{cc} a & b\\ c & d\end{array} \right) \left( \begin{array}{c} p_n\\ q_n \end{array} \right)$

Or, on peut dire, d'après l'énoncé, que :

$X_{n+1} = \left( \begin{array}{c} 0,9p_n + 0,4q_n\\ 0,1p_n + 0,6q_n\end{array} \right)$

soit que :

$\left( \begin{array}{c} 0,9p_n + 0,4q_n\\ 0,1p_n + 0,6q_n\end{array} \right) = \left( \begin{array}{cc} a & b\\ c & d\end{array} \right) \left( \begin{array}{c} p_n\\ q_n \end{array} \right)$

On en déduit que :

$\left( \begin{array}{cc} a & b\\ c & d\end{array} \right) = \left( \begin{array}{cc} 0,9 & 0,4\\ 0,1 & 0,6 \end{array}\right)$

On peut conclure que :

$M = \left( \begin{array}{cc} 0,9 & 0,4\\ 0,1 & 0,6\end{array} \right)$

### b)

$A = \left( \begin{array}{cc} 0,8 & 0,8\\ 0,2 & 0,2 \end{array} \right)$
\hspace{2em}
$B = \left( \begin{array}{cc} 0,2 & -0,8\\ -0,2 & 0,8\end{array} \right)$


$0,5B = \left( \begin{array}{cc} 0,1 & -0,4\\ -0,1 & 0,4 \end{array} \right)$

$A + 0,5B = \left( \begin{array}{cc} 0,8 & 0,8\\ 0,2 & 0,2 \end{array} \right) + \left( \begin{array}{cc} 0,1 & -0,4\\ -0,1 & 0,4 \end{array} \right) = \left( \begin{array}{cc} 0,9 & 0,4\\ 0,1 & 0,6 \end{array} \right)$

Or, $M = \left( \begin{array}{cc} 0,9 & 0,4\\ 0,1 & 0,6 \end{array} \right)$, on a donc bien $M = A+0,5B$

### c)

$A^2 = \left( \begin{array}{cc} 0,8 & 0,8\\ 0,2 & 0,2 \end{array} \right)^2 = \left( \begin{array}{cc} 0,8^2 + 0,8\times 0,2 & 0,8^2 + 0,8\times 0,2\\ 0,8\times 0,2 + 0,2^2 &  0,8\times 0,2 + 0,2^2 \end{array} \right) = \left( \begin{array}{cc}0,8 & 0,8\\ 0,2 & 0,2\end{array} \right) = A$


$B^2 = \left( \begin{array}{cc} 0,2 & -0,8\\ -0,2 & 0,8 \end{array} \right)^2 = \left( \begin{array}{cc} 0,2^2 + 0,2\times 0,8 & -0,8\times 0,2 - 0,8^2\\ -0,2^2 - 0,2\times 0,8 & 0,2\times 0,8 + 0,8^2 \end{array} \right) = \left( \begin{array}{cc} 0,2 & -0,8\\ -0,2 & 0,8 \end{array} \right) = B$

$AB = \left( \begin{array}{cc} 0,2\times 0,8 - 0,2\times 0,8 & -0,8^2 + 0,8^2\\ 0,2^2 - 0,2^2 & -0,8\times 0,2 + 0,8\times 0,2 \end{array} \right) = \left( \begin{array}{cc} 0 & 0\\ 0 & 0 \end{array} \right)$


$BA = \left( \begin{array}{cc} 0,8\times 0,2 - 0,2\times 0,8 & 0,8\times 0,2 - 0,2\times 0,8\\ -0,8\times 0,2 + 0,2\times 0,8 & -0,8\times 0,2 + 0,2\times 0,8 \end{array} \right) = \left( \begin{array}{cc} 0 & 0\\ 0 & 0 \end{array} \right)$


### d)

On utilise une démonstration par réccurence.

On définit pour tout $n\in\mathbb{N}$, la proposition $P_n : M^n = A + 0,5^nB$.

##### Initialisation

$P_1 \iff M^1 = A + 0,5^1B \iff M = \left( \begin{array}{cc} 0 & 0\\ 0 & 0 \end{array} \right)$

##### Hérédité

On cherche à démontrer que pour tout $n$ entier naturel positif, $P_n \implies P_{n+1}$, soit que $M^n = A + 0,5^nB \implies M^{n+1} = A + 0,5^{n+1}B$.

Pour cela, on suppose que $P_n$ pour $n$ fixé.

On a donc :

$$
\begin{array}{rcl}
P_{n+1} &\iff& M^{n+1} = A + 0,5^{n+1}B\\
&\iff& 
\end{array}
$$



### e)

On sait que $X_{n+1} = MX_n$. On peut donc dire, par réccurence, que $X_{n+1} = M^nX_0$.

Puisque $X_0 = \left( \begin{array}{c} 0\\ 1 \end{array} \right)$, on peut dire que $X_{n+1} = (A + 0,5^nB)X_0 = \left( \left(  \right) \right)$


### f)

On cherche à calculer $\displaystyle\lim_{n\rightarrow +\infty} \left( 0,8 - 0,8\times 0,5^n \right)$.

$\displaystyle\lim_{n\rightarrow +\infty}\left( 0,5^n \right) = \lim_{n\rightarrow +\infty}\left( \dfrac{1}{2^n} \right)$. Puisque $\displaystyle\lim_{n\rightarrow +\infty}(2^n) = +\infty$, on a $\displaystyle\lim_{n\rightarrow +\infty}\left( \dfrac{1}{2^n} \right) = 0$, soit $\displaystyle\lim_{n\rightarrow +\infty}(0,5^n) = 0$

Par produit, puis pas somme, on obtient :

$\displaystyle\lim_{n\rightarrow +\infty}(0,8 - 0,8\times 0,5^n) = 0,8$

Quand le nombre de jours tend vers $+\infty$, la probabilité que le fumeur fume toujours tend vers 0,8. On peut donc dire que le fumeur n'est pas sur d'arréter de fumer à terme (il à seulement une probabilité de 0,2 de ne plus fumer à terme).




