---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Risk Aversion

Consider a bet \( z \) with \( \mu = 0 \).
Would pay \( \Pi \) to avoid the bet where \( u(c-\Pi) = \Ex{u(c+z)} \).

Consider the Taylor expansion around \( \Pi^* = 0 \):
\[ \Ex{u(c+z)} \approx \Ex{u(c+z^*) + u'(u+z^*)(z-z^*) + \frac{1}{2} u''(c+z^*)(z-z^*)^2} \mid_{z = z^* = 0} \]
\[ = u(c) + 0 + \frac{1}{2}u''(c)\Ex{z^2} - \Ex{z}^2 \]
\[ u(c) - u'(c) \Pi = u(c) + \frac{1}{2} u''(c) \sigma^2 \]
\[ \Pi = \frac{-\sigma^2u''(c)}{2u'(c)} \]

where \( \rho^{\mathrm{ABS}}(c) = \frac{-u''(c)}{u'(c)} \) is the coefficient of absolute risk aversion, desire to smooth utility across outcomes.

With log utility,
\( u(c) = \log c \) then \( u'(c) = \frac{1}{c} \) and \( u''(c) = \frac{-1}{c^2} \).
Then \( \rho^{\mathrm{ABS}}(c) = \frac{1}{c} \).

With C-S utility,
\( u(c) = \frac{c^{1-\gamma}}{1-\gamma} \) then \( u'(c) = \frac{1}{c^{\gamma}} \) and \( u''(c) = \frac{-\gamma}{c^{\gamma+1}} \) has \( \rho^{\mathrm{ABS}}(c) = \frac{\gamma}{c} \).

These two examples are Decreasing Absolute Risk Aversion (\(\frac{d\rho^{\mathrm{ABS}}}{dc} < 0 \)).

With \( u(c) = \frac{-1}{e^{gamma c}} \) then \( u'(c) = \frac{\gamma}{e^{\gamma c}} \) and \( u''(c) = \frac{-\gamma^2}{e^{\gamma c}} \) so \( \rho^{\mathrm{ABS}}(c) = \gamma \) (Constant Absolute Risk Aversion).

With \( u(c) = \alpha c - \frac{\beta}{2}c^2 \) then \( \rho^{\mathrm{ABS}}(c) = \frac{\beta}{\alpha - \beta c}\) (Increasing Absolute Risk Aversion).

Note \(\rho^{\mathrm{ABS}}(c) \geq 0\) but \(\frac{d\rho^{\mathrm{ABS}}}{dc}\) can have any sign. But DARA fits data best.

## Precautionary Savings

\( \max\limits_{c_0, c_1} u(c_0) + \beta \Ex{u(c_1)} \) such that \( c_0 + a_1 = y_0 \) and \( c_1 = Ra_1 + y_1 \) where \( y_1 = \bar{y} + \eps_1\) and assume \( \beta R = 1 \).

When \( \Var{\eps_1} = 0 \) then \( y_1 = \bar{y} \) we have \( \Ex{u'(Ra_1+\bar{y})} = u'(Ra_1+\bar{y}) \).

When \( \Var{\eps_1} > 0 \) we have \( \Ex{u'(Ra_1 + \bar{y} + \eps_1)} > u'\paren{\Ex{Ra_1 + \bar{y} + e_1}}  = u'(Ra_1 + \bar{y})\).

The above by convexity of marginal utility \( u''' > 0 \) ("prudence") and Jensen's inequality.

Thus when the utility function displays prudence the equilibrium of the maximization problem at a higher variance is at a higher \( a_1 \) and so the household responds to risk by saving.
