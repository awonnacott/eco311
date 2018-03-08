---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## \( U(c, l) = \log(c) + \log(l) \), \( f(n) = zn \)

1. \( c^*, l^* \Rightarrow \exists \alpha_i : \hat{c} = c^*, \hat{l} = c^* \).
2. Given \( \alpha_i , (\hat{c}, \hat{l}), \Rightarrow \exists t_i : \hat{c} = c^*, \hat{l} = l^* \).

### Household Problem

\( \max\limits_{\curly{c_i, l_i}_i} \log(c_i) + \log(l_i) \) such that \( c_i \leq (1-l_i) \eps_i w + \frac{1}{2} d + t_i \).

Lagrangian is \( \mathcal{L}(c_i, l_i, \lambda_i) = \log(c_i) + \log(l_i) + \lambda_i \paren{(1-l_i) \eps_i w + \frac{1}{2} d + t_i  - c_i} \).

First order conditions are \( \frac{1}{c_i^*} = \lambda_i \) and \( \frac{1}{l_i^*} = \lambda_i e_i w \);
Euler equation is \( \frac{c_i^*}{l_i^*} = \eps_i w \).

Plug in to the budget constraint \( \eps_i l_i^* w = (1-l_i^*) \eps_i w + \frac{1}{2} d + t_i \).
Then \( \l_i^* = \frac{ \eps_i w + \frac{1}{2} d + t_i}{2 \eps_i w} \) and \( c_i^* = \frac{\eps_i w + \frac{1}{2} d + t_i}{2} \).

Once we know the real wage and the dividends, we will know the equilibrium behavior of the worker.

### Firm Problem

\( \max\limits_{n \in [0, \eps_1 + \eps_2]} (z - w) n \) will be \( n^* = \eps_1 \) when \( z > w \), anywhere when \( z = w \), or \( 0 \) if \( z < w \).

Thus either profits are zero everywhere or we are at a corner solution.

### Competetive Equilibrium

Endogenous variables: allocations \(n^*, \curly{c_i^*, l_i^*}_i, d^* \) and prices \( w \).

1. Given \( w \) and \( d^* \), we have \( \curly{c_i^*, l_i^*}_i, \) solve the household problem.
2. Given \( w \), we have \( n^* \) solves the firm problem.
3. Labor market clearing: \( n^* = \sum\limits_i (1 - l_i^*) \eps_i \)
4. Skip goods market clearing condition by Walras' Law
5. Profits are transfered to dividends: \( d^* = (z - w) n^* \)

Consider Inada conditions: we know people will neither work always nor work never.
Thus we know \( z = w \) directly, which confirms \( d^* = 0 \).
Then we have \( l_i^* = \frac{1}{2} \) and \( c_i^* = \frac{\eps_i z}{2} \).
By (3), we have \( n^* = \frac{1}{2} \sum\limits_i \eps_i \).

### Social Planner Problem

\( \max\limits_{\curly{c_i, l_i}_i} \sum\limits_i \alpha_i (\log(c_i) + \log(l_i)) \) such that \( \sum\limits_i c_i \leq z \sum\limits_i (1 - l_i) \eps_i \) and \( \sum\limits_i \alpha_i = 1 \).

First order conditions are \( \frac{\alpha_i}{\hat{c_i}} = \lambda \) and \( \frac{\alpha_i}{\hat{l_i}} = \lambda \eps_i z \).
Then \( \frac{\hat{c_i}}{\hat{l_i}} = \eps_i z \).
This is exacly the same as the Euler equation from the HP, so we can definitely find \( \curly{\alpha_i}_i \) such that the CE is PO.
Also \( \frac{\hat{l_j}}{\hat{l_i}} = \frac{\alpha_j \eps_i }{\alpha_i \eps_j } \) and \( \frac{\hat{c_j}}{\hat{c_i}} = \frac{\alpha_j }{\alpha_i } \).

Then we have four equations and four variables and elimiate all variables but \( c_1 \) and get conditions such as \( \hat{l_i} = \frac{\alpha_i }{2 \eps_i} \sum\limits_j \eps_j \).
Then by taking the CE allocation for \( l_i^* \) we solve for \( \alpha_1 \) given \( l_i^* = \hat{l_i} \) we have \( \alpha_i = \frac{\eps_i}{\sum\limits_j \eps_j} \).

### First Welfare Theorem

To show the CE is PO, show the allocations (\(c\)-\(l\) FOCs) for a given household are the same in CE and PO.

### Second Welfare Theorem

Then, take the Pareto outcome as given: \( \hat{l_i} = \frac{\alpha_i }{2 \eps_i} \sum\limits_j \eps_j\) and \( l_i^* = \frac{\eps_i z + t_i}{2 \eps_i z} \).
We know \( \sum\limits_i t_i = 0 \).

Taking \( \alpha_i \) as given and setting \( \hat{l_i} = l_i^* \),
\( \frac{\alpha_i }{2 \eps_i} \sum\limits_j \eps_j = l_i^* = \frac{\eps_i z + t_i}{2 \eps_i z} \)
When \( N = 2 \) as throughout, \( \alpha_1 z \eps_2 - \alpha_2 z \eps_1 = t \).
