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

We can disprove this by a counterexample: Take $L_1$ = {$x \in \{0, 1\}^*$ | number of 0s in x is even}, $L_2$ = {$x \in \{0, 1\}^*$ | number of 1s in x is even}, $L_3 = \{0, 1\}^*$. It needs to be checked whether this fulfills the requirements. $L_2 \subseteq L_3$ obviously holds, and if we take $f$ to just invert all 0s and 1s, we can also easily prove that $L_1 \leq_P L_2$: $x \in L_1 \leftrightarrow f(x) \in L_2$.

We cannot however find a $g$, such that $x \in L_1 \leftrightarrow g(x) \in L_3$, because $L_3$ accepts all strings, but $L_1$ does reject some strings. It is therefore not possible to do anything to the strings $L_1$ rejects that would make $L_3$ reject them, so $L_1 \not \leq_P L_3$, and we have successfully disproven the theorem.

# 4
## 4a
NPC (NP-complete) is defined as $NP \cap NPH$. If we want to prove something to be an element of NPC, we need to prove that it is a member of both sets.

To prove that a problem $L$ is NP hard, we need to find a known NP hard problem $L_{NPH}$ (e.g. SAT), and show that it reduces to the problem at hand: $L_{NPH} \leq_P L$. Because of the transitivity of $\leq_P$ we only need to do this for a single problem.
