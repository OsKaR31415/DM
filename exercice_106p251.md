---
title: Exercice 106 p 251
subtitle: L'algorithme PageRank
author: Oscar Plaisant
---

# 1. Relations de réccurence

## a)

\huge
[insérer image]
\normalsize

## b)
$a_{n+1}$ est la somme de :

 - la valeur que lui envoie la page B, qui divise sa valeur entre A et E, soit $0,425b_n$
 - la valeur que lui envoie la page C, qui divise sa valeur entre A, B, D et E, soit $0,2125c_n$
 - la valeur que lui envoie la page D, qui divise sa valeur entre A et C, soit $0,425d_n$
 - la valeur de $k$ (soit $\dfrac{0,15}{5} = 0,03$)

On a donc bien $a_{n+1} = 0,03 + 0,425b_n + 0,2125c_n + 0,425d_n$

## c)

On obtient de la même manière les relationd de réccurence suivantes :

 - $a_{n+1} = 0,03 + 0,425b_n + 0,2125c_n + 0,425d_n$
 - $b_{n+1} = 0,03 + 0,85a_n + 0,2125c_n$
 - $c_{n+1} = 0,03 + 0,425d_n$
 - $d_{n+1} = 0,03 + 0,2125c_n$
 - $e_{n+1} = 0,03 + 0,425b_n + 0,2125c_n$


