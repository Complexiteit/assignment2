---
title: Assignment 2
author: Hendrik Werner s4549775
date: \today
fontsize: 12pt
geometry: margin=5em
---

# 1

# 2
We want to prove that given $L_1, L_2 \in P$, that $\{u \in L_1 | u \not \in L_2\} \in P$. If we look at the definition of $P$:

$P = \{L \subseteq \{0, 1\}^* | \exists k. \exists A \in O(|x|^k): \{0, 1\}^* \rightarrow \{0, 1\}. A(x) = 1 \leftrightarrow x \in L\}$

We see that we have two polynomial algorithms $A, B$, for which $A(x) = 1 \leftrightarrow x \in L_1$, and $B(x) = 1 \leftrightarrow x \in L_2$. We can chain polynomial functions and the compound function remains polynomial. The set can also be defined as $\{x \in \{0, 1\}^* | A(x) = 1 \land B(x) = 0\}$. Obviously this set is an element if $P$.

# 3
It is given that $L_1 \leq_P L_2$, which means that we have a polynomial $f: \{0, 1\}^* \rightarrow \{0, 1\}^*$ for which is holds that $\forall x \in \{0, 1\}^*. x \in L_1 \leftrightarrow f(x) \in L_2$. It is also given that $L_2 \subseteq L_3$. We want to prove or disprove that $L_1 \leq_P L_3$ follows from there prerequisites.

# 4
