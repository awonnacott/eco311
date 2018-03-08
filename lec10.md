---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Income and Substitution Effects from Rising Interest Rate

\[
\begin{array}{r|cc|cc|cc}
    & a_1 = 0 & & a_1 > 0 & \mbox{Saver} & a_1 < 0 & \mbox{Borrower} \\
    & c_1 & c_2 & c_1 & c_2 & c_1 & c_1 \\
\hline \mbox{Income}
    & - & - & \uparrow & \uparrow & \downarrow & \downarrow \\
\hline \mbox{Substitution}
    & \downarrow & \uparrow & \downarrow & \uparrow & \downarrow & \uparrow \\
\hline \mbox{Sum}
    & \downarrow & \uparrow & \updownarrow & \uparrow & \downarrow & \updownarrow \\
\end{array}
\]

## Permanant Income Hypothesis

Milton Friedman (Chicago School) Nobel for Economics

Context: Keynes establishes \( c = f(y) = \alpha + \beta y\) (Keynesian consumption) and marginal propensity to consume (MPC) \( \beta \) and incorporates this into macroeconomic policy, but also claims that consumption responds to any change in income the same way regardless of the source of income.

Friedman: Given transitory income \( y^T \) paid in only one period, permanant income \( y^P \) paid in all periods, \( \max\limits_{c_1, c_2} \log c_1 + \beta \log c_2 \) such that \( c_1 + s = y^T + y^P \) and \( c_2 = s(1+r) + y^P \).
That is, we optimize our utility assuming that we only make our annual wage (and not our bonuses) in the future, but with knowledge of our past bonuses.
Intertemporally:
\[ c_1 + \frac{c_2}{1 + r} = y^T + \paren{1 + \frac{1}{1+r}} y^P \]
\[ \mathcal{L} = \log c_1 + \beta \log c_2 + \lambda\paren{ y^T + \paren{1 + \frac{1}{1+r}} y^P - c_1 - \frac{c_2}{1 + r} } \]
\[ \mathcal{L}_{c_1} = 0 \Rightarrow \frac{1}{c_1} = \lambda\]
\[ \beta \mathcal{L}_{c_2} = 0 \Rightarrow \frac{\beta}{c_2} = \frac{\lambda}{1+r} \]
\[ \frac{c_2}{c_1} = \beta (1 + r) \]

Now for simplicity set \( \beta (1 + r) = 1 \) by assumption (which follows from a stationary equilibrium, e.g.\ an equliibrium where \( \forall \varphi, \varphi_t = \varphi_{t'} \) ).
That is, \( c^* := c_1 = c_2 \).
This simplifies the above math:
\[c^* \left( 1 + \frac{1}{1+r}\right) = y^T + \left( 1 + \frac{1}{1+r} \right) y^P \Rightarrow c^* = \frac{1+r}{2+r}y^T + y^P\]
So the marginal propensity to consume changes with the type of income.

Another assumption which holds "approximately very well": \( r \approx 0 \).
The utility-maximizing behavior for log utility is to save transitory income to be consumed an equal amount across all periods accounting for interest.
This is called "interetemporal consumption smoothing."

\newpage
### Infinite horizon case

A convenient approximation of very large \(N\) for better approximation the stationarity of the dynamic problem.

Parent (lives for \(N\) periods) \( U^P = \sum\limits_{t=0}^{N-1} \beta^t u(c_t) \).
Child (lives for \(N\) periods) \( U^C = \sum\limits_{t=N}^{2N-1} \beta^{t-N} u(c_t) \).

Parent discounts the utility of the child at rate \( \delta \beta \) for \( \delta \in [0, \bar{\delta}] \) such that \( \delta \beta < 1 \).
\( U = U^P + \paren{\beta \delta}^N U^C \)

In pure altruism ( \( \delta = 1 \) ) with infinite generations, this collapses to \( U = \sum\limits_{t=0}^{\infty} \beta^t u(c_t) \).

With log utility this is \( \max\limits_{\curly{c_t}_{t=0}^\infty} \sum\limits_{t=0}^\infty \beta^t \log(c_t) \) such that \( c_0 + s_0 = y^T + y^P \) and \( \forall t \geq 1, c_t + s_t = y^P + (1+r) s_{t-1} \).

Lifetime budget constraint given \( \sum\limits_{t=0}^\infty \frac{c_t}{(1+r)^t} = y^T + y^P \sum\limits_{t=0}^\infty \frac{1}{(1+r)^t} \), or \( \sum\limits_{t=0}^\infty \beta^t c_t = y^T + y^P \pfrac{1+r}{r} \) for \( r > 0 \).

The Euler equation is \( \frac{c_t'}{c_t} = \paren{\beta(1+r)}^{t'-t} \), then when we hold \( \beta (1 + r) = 1 \) we have \( c^* = \pfrac{r}{1+r} y^T + y^P \), the permanant income hypothesis in the infinite horizon.
Now when \( r \approx 0 \) we have \( c^* = y^P \).

### Finite time case

\[ c^* \sum\limits_{t=0}^{N-1} \pfrac{1}{1+r}^t = y^T + y^P \sum\limits_{t=0}^{N-1} \pfrac{1}{1+r}^t \]

\[ c^*
    = y^T \frac{1}{\frac{1 - \pfrac{1}{1+r}^N}{1 - \frac{1}{1+r}}}+ y^P
    = y^T \pfrac{r}{1+r} \pfrac{1}{1 - \pfrac{1}{1+r}^N} + y^P
    \approx \frac{1}{N} y^T + y^P
\]

### Summary

Permanant income hypothesis: \( MPC^T \approx \frac{1}{N} \); \( MPC^P \approx 1 \)
