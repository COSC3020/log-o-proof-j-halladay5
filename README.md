[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

Definintion of O: $T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n), \forall n \geq n_0$

Substitute $\ f(n) = log_{2} n : T(n) \in O(log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot log_{2} n ,\forall n \geq n_0$

Change of base formula: $\ log_{b} a = \frac{log_{c} a}{log_{c} b} $

Split $\ log_{2} n $ to find constant needed for change of base to base 5: $\ log_{2} n = \frac{log_{5} n}{log_{5} 2} $

Plug in constant : $\ T(n) \in O(log_{2} n) \iff \exists c, n_0 : T(n) \leq c \cdot (\frac{1}{log_{5} 2}) \cdot log_{5} n , \forall n \geq n_0 $

$\ \frac{c}{a constant}$ is still a constant. Change $\ \frac{c}{log_{5} 2} to \ c_1 $

$\ T(n) \in O(log_{2} n) \iff \exists c_1, n_0: T(n) \leq c_1 \cdot log_{5} n, \forall n\geq n_0 $.

Therefore by O definition, $\ T(n) \in O(log_{2} n) \implies T(n) \in O(log_{5} n) $

Implies only works one way, so we need to prove that $\ T(n) \in O(log_{5} n) \implies T(n) \in O(log_{2} n)$

Definintion of O: $T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n), \forall n \geq n_0$

Substitute $\ f(n) = log_{5} n : T(n) \in O(log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot log_{5} n ,\forall n \geq n_0$

Change of base formula: $\ log_{b} a = \frac{log_{c} a}{log_{c} b} $

Split $\ log_{5} n $ to find constant needed for change of base to base 2: $\ log_{5} n = \frac{log_{2} n}{log_{2} 5} $

Plug in constant : $\ T(n) \in O(log_{5} n) \iff \exists c, n_0 : T(n) \leq c \cdot (\frac{1}{log_{2} 5}) \cdot log_{2} n , \forall n \geq n_0 $

$\ \frac{c}{a constant}$ is still a constant. Change $\ \frac{c}{log_{2} 5} to \ c_2 $

$\ T(n) \in O(log_{5} n) \iff \exists c_2, n_0: T(n) \leq c_2 \cdot log_{2} n, \forall n\geq n_0 $.

Therefore by O definition, $\ T(n) \in O(log_{5} n) \implies T(n) \in O(log_{2} n) $

If $\ T(n) \in O(log_{2} n) \iff T(n) \in O(log_{5} n) $

In O, log bases do not matter because they are related by a constant factor. Using the base change formula, you can easily change the base of a logarithm and find that constant.
In O analysis we disregard constant factors, so they are the same thing. If all functions in T(n) are in $\ log_{2} n$ and all functions in T(n) are in $\ log_{5} n $, then $\ log_{2} n = log_{5} n$
