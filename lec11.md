---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Economics with Uncertainty

Random variable \( s \in \mathcal{S} = \curly{\bar{s}_i}_{i=1}^N \) represents the state of nature, the world, the economy.

In the 2-period economy, at \( t = 1 \) we have no uncertainty, and at \( t = 2 \) we go to one of the outcomes of \( s \) with probability \( \Pi(s) \).

W.L.O.G.\ assume \( y_2(\bar{s}_i) \leq y_2(\bar{s}_j) \Leftrightarrow i \leq j \).
Then the household problem is:

\[ \max \Ex{\sum\limits_{t=1}^2 \beta^{t-1} u(c_t)}
    = \max u(c_1) + \beta \operatorname{Ex}_1\bracket{u(c_2(S))}
    = \max u(c_1) + \beta \sum\limits_{s \in \mathcal{S}} \Pi(s) u(c_2(s))
\]

such that the budget constraints \( c_1 + a_2 = y_1 \) and (w.p.\ \( \Pi(s) \)) \( c_2(s) = y_2(s) + R(a_2) \).
Note \( R = 1 + r \) is not dependent on \( s \) iff our savings are stored in a 'safe asset,' otherwise they are a 'risky asset.'

\[ \mathcal{L}
    = u(c_1) + \sum\limits_{s \in \mathcal{S}} \Pi(s) \paren{ \beta u(c_2(s)) + \lambda_s \paren{y_1 + \frac{y_2(s)}{R} - c_1 - \frac{c_2(s)}{R}}}
\]

\[ \frac{dL}{dc_1} = 0 \Rightarrow u_c(c_1) = \sum\limits_{s \in \mathcal{S}} \Pi(s) \lambda_s \]
\[ \frac{dL}{dc_2(s)} = 0 \Rightarrow \Pi(s) \beta u_c(c_2(s)) = \frac{\Pi(s) \lambda_s}{R} \]
\[ \beta \sum\limits_{s \in S} \Pi(s) u_c(c_2(s)) = \frac{1}{R} \sum\limits_{s \in S} \Pi(s) \lambda_s\]
\[ \beta R \operatorname{Ex}_1 \bracket{u_c(c_2(S))} = \sum\limits_{s \in S} \Pi(s) \lambda_s = u_c(c_1)\]

So the Euler equation is exactly as expected, but in expectation in period 1.


### Example

Let \( u(c_t) = \alpha c_t - \frac{1}{2} \gamma c_t^2 \) then set \( \beta R = 1 \) to simplify \( u_c(c_t) = \alpha - \gamma c_t \).
Then the Euler equation \( \alpha - \gamma c_1 = \operatorname{Ex}_1 \bracket{\alpha - \gamma c_2(s)} \) simplifies to \( \operatorname{Ex}_1 \bracket{c_2(s)} = c_1 \).
Optimal consumption smoothing under uncertainty is make consumption choice so that expected consumption in period 2 is equal to consumption in period 1.
This generalizes deterministic consumption smoothing.

### Stochastic models

Consider the \( AR(1) \) stochastic process \( X_{t+1} = \rho X_t + \eps_{t+1} \) for \( \rho \leq 1 \) and \( \forall t, \eps_t \sim \mathcal{N}(0, \sigma) \).
This process has mean reversion since \( \bar{x}_{t+1} - \mu = \rho \bar{x}_t - \mu \) in expectation when \( \rho < 1 \).
When \( \rho = 1 \) this is a random walk.

In the general case, consumption is a random walk.
