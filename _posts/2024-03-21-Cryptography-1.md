---
layout: post
date: 2024-03-21
---

<td>
  <a target="_blank" href="https://colab.research.google.com/drive/1nWwQLzSBcx9umh-zOA3bvY2itj6_Wm1o?usp=sharing"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Google_Colaboratory_SVG_Logo.svg/320px-Google_Colaboratory_SVG_Logo.svg.png" height=32 /></a>
</td>

# Modular arithmetic

## Modulus

Given two integers $a$ and $m$ such that $m\ne 0$. Taking $a$ **modulo** $m$ means calculating the remainder of $a$ divided by $m$.  The number $m$ is called the **modulus**.

**Notation:** $a\bmod m$.

*Note.* The remainder of $a$ divided by $b$ is an unique integer $r$ such that $0\le r< |m|$$ and there exists an integer $q$ satisfying $a=qm+r$.

We say that $a$ is congruent to $b$ modulo $m$ if $a\bmod m=b\bmod m$.

**Notation:** $a\equiv b\pmod m$.


```python
remainder = 1234 % 9
print("remainder =", remainder)
quotient = 1234 // 9
print("quotient =", quotient)
print(quotient * 9 + remainder)
```

    remainder = 1
    quotient = 137
    1234


## Congruence classes
We call all numbers that differ by a **multiple of the modulus** **equivalent** or **congruent**.

The congruence relation modulo $m$ divides $$\mathbb{Z}$$ into $m$ congruence classes:
$$
\begin{align*}
\overline{0}&=\{\ldots,-2m,-m,0,m,2m,\ldots\} \\
\overline{1}&=\{\ldots,-2m+1,-m+1,1,m+1,2m+1,\ldots\} \\
\overline{2}&=\{\ldots,-2m+2,-m+2,2,m+2,2m+2,\ldots\} \\
\vdots \\
\overline{m-1}&=\{\ldots,-m-1,-1,m-1,2m-1,3m-1,\ldots\}
\end{align*}
$$
Here $$\overline{x}$$ denote the congruence class that contains $x$.

## Modular multiplicative inverse
An integer $b$ is called modular multiplicative inverse of $a$ modulo $m$ if $ab\equiv 1\pmod m$.

**Notation:** $b=a^{-1}$$.
