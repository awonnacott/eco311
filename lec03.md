---
header-includes: |
    \usepackage[margin=0.5in]{geometry}
    \usepackage{mathrsfs}
---

## Assumptions:

* Rationality
* Competitive behavior
* Prices as parameters (no adverse selection)

## Household problem

\(\max\limits_{c, l} U(c, l) + V(g)\) such that \(c \leq w(1-l) + d - t\), \(c \geq 0\), \(l \geq 0\), \(l \leq 1 \)

Note from Inada Conditions the nonnegativity of \(c, l\) are not binding conditions, and optimization of \(V(g)\) is independent of optimization of \(U(c, l)\) (though non-independence could be a good exam question!)

Now reduced to \(\max\limits_{c, l} U(c, l)\) such that \(c \leq w(1-l)+d-t\), \(l\leq 1\)

Solve using Lagrangian \( \mathscr{L}(c, l, \lambda, \mu) = U(c, l) + \lambda\left[w(1-l)+d-t-c\right]+\mu(1-l)\)

Note \(\lambda\) is the marginal utility of an value, \(\mu\) is the marginal utility of time.

\( \frac{\partial \mathscr{L}}{\partial c} = 0 \Rightarrow U_c(c*, l*) - \lambda = 0 \Rightarrow U_c(c*, l*) = \lambda \)

Assuming the latter constraint is slack, e.g.\ at the solution (\(\mu = 0\))

\( \frac{\partial \mathscr{L}}{\partial l} = 0 \Rightarrow U_l(c*, l*) - \lambda w = 0 \Rightarrow \Rightarrow U_l(c*, l*) = \lambda w \)

The marginal rate of subsitution is equal to the ratio of the prices (wage being price of time): in real terms, \( MRS_{c*, l*} = w\) (``Cornerstone of marginal economics'')

The solution is where the indifference curve is tangent to the budget constraint.

To solve for \( c^*, l^*\), use \( \frac{U_l(c^*, l^*)}{U_c(c^*, l^*)} = w \) and \( c^* = w(1-l^*) + d - t\).

The household problem has a unique solution because the indifference curve will only lie tangent to the budget constraint once by convexity of preferences.

If the optimum has \(l^* > 1\) then the optimum feasible has \( l^* = 1\), \(c^* = d - t\) as a corner solution.

Example: \(U(c, l) = \log c + A\log l \) (natural log)

* \( \mathscr{L}(c, l, \lambda, \mu) = \log c + A \log l + \lambda\left[w(1-l)+d-t-c\right] + \mu(1-l)\)

* FOC for \( c \) is \( \frac{1}{c} = \lambda \); for \( l \) is \( \frac{A}{l} = \lambda w \). Then \( \frac{Ac}{l} = w\).

* Substitute for budget constraint then \( A\left[w(1-l)+d-t\right] = wl \) has \( l^* = \frac{A(w+d-t)}{(1+A)w} \),
\( h^* = 1 - l^* = \frac{1-A\left(\frac{d-t}{w}\right)}{1+A}\)

* Solve budget constraint, get \( c^* = \frac{w+d-t}{1+A} \)

* Agent thinks of the above as functions of the parameters \( d, t, w \)

* Effect of an increase in nonwage income (proxy for wealth) \( d-t \) resulting in both increased leasure and consumption (sanity-check: both are normal goods). ``Negative wealth effect on labor supply.''

From \( c + w l = w + (d - t) \), you see that high net worth individuals behavior is dominated by the substitution effect, whereas others' behaviors are dominated by the income effect.

## Firm Problem

Maximize profits \( \max\limits_n \Pi^N(\overline{k}, n) = py - w^Nn \) where \( py \) is total production value and \(n\) is salary. \( y = zf(\overline{k}, n) \)

Real: \( \max\limits_n \Pi(k, m) = y - wn \). First order condition: \( zf_n(\overline{k}, n*) = w\).

Marginal product of labor \( MPL(\overline{k}, m^*) = w \) is monotonically increasing concave down, initially very steep. Optimal is when slope of MPL is equal to wage.
