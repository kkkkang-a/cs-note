# Asymptotic Growth Analysis

Let $T(n)$ be the worst-case number of steps of our algorithm on an instance of size $n$.

Asymptotic growth analysis provides a coarser but sufficient way to summarise how $T(n)$ behaves when $n$ increases.

## Big-O Notation

> $T(n) = O(f(n))$ if there exist $n_0, c > 0$ such that $T(n) \leq cf(n)$ for all $n > n_0$.

When we say $T(n) = O(f(n))$, we mean that the growth rate of $T(n)$ is bounded above by a constant multiple of $f(n)$ for sufficiently large $n$.

## Big-Omega Notation

> $T(n) = \Omega(f(n))$ if there exist $n_0, c > 0$ such that $T(n) \geq cf(n)$ for all $n > n_0$.

When we say $T(n) = \Omega(f(n))$, we mean that the growth rate of $T(n)$ is bounded below by a constant multiple of $f(n)$ for sufficiently large $n$.

## Theta Notation

> $T(n) = \Theta(f(n))$ if $T(n) = O(f(n))$ and $T(n) = \Omega(f(n))$.

When we say $T(n) = \Theta(f(n))$, we mean that the growth rate of $T(n)$ matches exactly with the growth rate of $f(n)$ for sufficiently large $n$.