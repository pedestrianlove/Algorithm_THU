# Chapter 3. Characterizing Running Times

## 3.1 Asymptotic notation (漸近式表示法)

### Tight-Bound ($\Theta$-notation)
$$
\Theta(g(n)) = \{f(n) | 0 \leq c_1g(n) \leq f(n) \leq c_2g(n) \forall n\geq n_0 \}
$$
Then
$$
f(n) \in \Theta(g(n))
$$
- 也就是說在超過某個自然數$n_0$之後，函數值$f(n)$皆會被常數倍(常數是固定的)的$g(n)$所bound住。

#### Example
- $6n^3$ does not belongs to $\Theta(n^2)$.
- $\frac{n^2}{2} - 3n$ belongs to $\Theta(n^2)$.
- Note: 可以同除$n^2$，然後使用不等式找出除完後的最大值/最小值，也就是$c_1, c_2$.

#### Remark
In general, given any $p(n) = \sum_{i = 0}^$


### Asymptotic Upper-Bound ($O$-notation)
$$
O(g(n)) = \{f(n) | 0 \leq f(n) \leq c_1g(n) \forall n\geq n_0 \}
$$
Then
$$
f(n) \in O(g(n))
$$

### Asymptotic Lower-Bound ($\Omega$-notation)
$$
\Omega(g(n)) = \{f(n) | 0 \leq c_1g(n) \leq f(n) \forall n\geq n_0 \}
$$
Then
$$
f(n) \in \Omega(g(n))
$$

### Theorem 3.1
For any two functions $f, g$, $f(n) = \Theta(g(n))$ if and only if $f(n) = O(g(n))$ and $f(n) = \Omega(g(n))$.


## Polynomial & Exponentials
### Polynomials
A function is **Polynomial bounded** if $f(n) = n^{O(1)}$.

### Exponentials
Any positive exponential function grows faster than any polynomial.

### Logarithms

### Factorials
