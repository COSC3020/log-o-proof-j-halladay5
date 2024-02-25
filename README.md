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

Substitute $\ T(n) = log_{5} n : \exists c, n_0: log_{5} n \leq c \cdot f(n), \forall n \geq n_0$

Substitute $\ f(n) = log_{2} n : \exists c, n_0: log_{5} n \leq c \cdot log_{2} n ,\forall n \geq n_0$

Plug in c = $\\frac{1}{log_{2} 5},  n_0 = 1 : log_{5} n \leq \frac{1}{log_{2} 5} \cdot log_{2} n ,\forall n \leq 1$

Log base change formula : $\ log_{5} n \leq log_{5} n ,\forall n \leq 1$

True by mathematical reasoning : $\log_{5} n = log_{5} n ,\forall n \geq 1$

In O, log bases do not matter because they are related by a constant factor. Using the base change formula, you can easily change the base of a logarithm and find that constant.
In O analysis we disregard constant factors, so they are the same thing. 
