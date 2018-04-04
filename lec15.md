---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

*Missed the first 30 minutes or so of this lecture*

\( \gamma \) is risk aversion and \( \frac{1}{\gamma} \) is wont to smooth consumption

Equity premium \( \frac{\Ex{R^e(s)} - R^b}{R^b} = -\operatorname{cov}\paren{R^e(s), m(s)} \)

\( m(s) = \pfrac{c_1}{c_2(s)}^{\gamma} \)

Note \( \operatorname{cov}\paren{R6e(s), c_2(s)} > 0 \)

Special cases
1. \( R^e(s) \) is constant (not volatile) then \( \pi = 0 \)
2. \( \gamma = 0 \) (risk neutrality) then \( m(s) \) is constant so \( \pi = 0 \)

## Bubbles

Asset purchased at time \(t\) at price \( p_t \) yields dividends \( \curly{y_{t+j}}_{j=0}^{\infty} \) and can be solde at time \( t+1 \) for price \( p_{t+1} \).

Examples:
1. Tree
2. Housing (rent, forgone rent)

When \( \gamma = 0 \) then \( y_t - p_t + \beta p_{t+1} = 0 \) so \( p_t = y_t + \beta p_{t+1} \). This is the price difference equation.

The fundamental value of the asset \( p_t^F = \sum\limits_{j=0}^{\infty} \beta^j y_{t+j} \)

### Bubble example

Assume \( \forall t, y_t = 0 \), then \(\forall t, p_t = \beta p_{t+1} \) and \( \forall t, p_t^F = 0 \).

The bubble solution says \( p_t^B = \kappa * \beta^{-t} = \beta\paren{\kappa \beta^{-(t+1)}} = \beta p_{t+1}^B \).

Note whenever \( \kappa > 0 \) then the price will grow across time because people buy the asset expecting price to go up, and the price only grows because it was expected to grow and more people are buying it by that reasoning.

Note \( p_t = p_t^F + (p_t^B - p_t^F) \) and suppose the fruit is constant so \( p_t^F = p_{t'}^F \) then note when speculators want the price to go up the price does rise above the correct \( \frac{\bar{y}}{1 - \beta} \) and this will continue until the speculators' expectations changes at which point \( p_t^B - p_t^F \) quickly drops back to 0 and so \( p_t \to p_t^F \).
