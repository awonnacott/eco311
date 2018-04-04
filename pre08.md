---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Uncertainty

Normal two period problem with next income period stochastic \( y_2(s) : y_2(\bar{s}_N) > \ldots > y_2(\bar{s}_1) \)

Household \( \max\limits_{c_1, a_2, c_2} u(c_1) + \beta \sum\limits{s \in \mathcal{S}} \pi(s) u(c_2(s)) \) such that \( c_1 + a_2 = y_1 \) and w.p.\ \( \pi(s) \), \( c_2(s) = y_2(s) + Ra_2 \).

Combine the \( N+1 \) budget constraints into \( N \) budget constraints: \( c_1 + \frac{c_2(s)}{R} \leq y_1 + \frac{y_2(s)}{R} \)

\[ \mathcal{L} = u(c_1) + \sum\limits_{s \in \mathcal{S}} \pi(s) \paren{ \beta u(c_2(s)) + \lambda_s \paren{y_1 + \frac{y_2(s)}{R} - c_1 - \frac{c_2(s)}{R}}} \]


\[u'(c_1) = \sum\limits_{s \in \mathcal{S}} \pi(s) \lambda_s = \Ex{\lambda_s}\] \[\pi(s) \beta u'(c_2(s)) = \frac{\pi(s) \lambda_s}{R}\]

Add up the FOCs:
\[\beta \sum\limits_{s \in \mathcal{S}} \pi(s) u'(c_2(s)) = \frac{1}{R} \sum\limits_{s \in \mathcal{S}} \pi(s) \lambda_s \Rightarrow \beta \Ex{u'(c_2(s))} = \frac{1}{R} \Ex{\lambda_s}\]
Euler equation:
\[u'(c_1) = \beta R \Ex{u'(c_2(s))} \]

## Risk Aversion

How can we measure the amount of risk aversion of a specific utility function?
Take a lottery with payoff \( z \) with \( \Ex{z} = 0 \) with variance \( \sigma^2 \).
What at premium \( \pi \) to avoid the lottery would you be indifferent about playing the lottery.

* Absolute risk aversion: how many dollars \( \pi \) (or absolute goods) are you willing to pay?

  \( u(c - \pi) = \Ex{u(c+z)} \Rightarrow \pi = \frac{-vu''(c)}{2u'(c)} \)
* Relative risk aversion: what fraction \( \pi \) of your consumption are you willing to pay?

  \( u(c(1-\pi)) = \Ex{u(c(1+z))} \Rightarrow \pi = \frac{-cvu''(c)}{2u'(c)} \)

With a concave function then the player is risk averse.

Intuition:

* Portfolios contain risky assets and safe assets.
* Increasing absolute risk aversion implies that as individuals get richer, they invest fewer dollars in stocks.
* Increasing relative risk aversion implies that as individuals get richer, they invest a smaller proportion of their wealth in stocks.
* Increasing absolute risk aversion is inconsistent with real world behavior.

## Precautionary Savings

* If there is uncertainty about future income, agents save in order to be able to consume in the future even in the case of an undesirable income shock.
* Any \( u \) with prudence, i.e.\ \( u''' > 0 \), features this savings motive.
* To see this, note that when \( u''' > 0 \) then \( a_1 \) are increasing in the variance of \( y_2 \) by lecture.

## Conclusion:
* What are uncertainty, random variable, probability distribution
* Write down and solve a model that includes uncertainty and solve for the Euler Equation
* What are risk aversion, precautionary saving as properties of utility functions and why are we interested, i.e.\ to narrow down what is a sensible functional form to describe utility functions

## Permanent Income Hypothesis: Deterministic and Stochastic

a. We want to show \( c_t = \operatorname{Ex}_t\bracket{c_t+1} \) since we know \( \beta R = 1 \) in order to show \( c_t \) is a Martingale.

    Introduce history notation \( s^t - \paren{s_i}_{i=0}^t \) so then \( c_t(s^t) = c_t(s_0, s_1, \ldots s_t) \).
    The household problem is:
    \[ \max\limits_{c_t(s_t), a_{t+1}(s_t)} \sum\limits_{t=0}^\infty \sum\limits_{s^t} \pi(s^t) \beta^t \paren{b_1 c_t(s^t) - \frac{1}{2} b_2 {c_t(s_t)}^2} \Big| \forall t, \forall s^t, c_t(s^t) + a_{t+1}(s^t) \leq Ra_t(s^{t-1}) + y_t(s^t)\]
    \[ \mathcal{L} = \sum\limits_{t=0}^\infty \sum\limits_{s^t} \pi(s^t) \beta^t \paren{b_1 c_t(s^t) - \frac{1}{2} b_2 {c_t(s_t)}^2} - \sum\limits_{t=0}^\infty \sum\limits_{s^t} \pi(s^t) \lambda_t(s^t) \paren{c_t(s^t) + a_{t+1}(s^t) - Ra_t(s^{t-1}) - y_t(s^t)} \]
    \[ \frac{\partial \mathcal{L}}{\partial c_t(s^t)} = 0 \Rightarrow \pi(s^t) \beta^t \paren{b_1 - b_2 c_t(s^t)} = \lambda_t (s^t) \pi(s^t)\]
    \[ \frac{\partial \mathcal{L}}{\partial a_{t+1}(s^t)} = 0 \Rightarrow \sum\limits_{s^{t+1}} \lambda_{t+1} (s^{t+1}) \pi(s^{t+1}) R = \lambda_t(s^t) \pi(s^t) \]
    There is a term \( \sum\limits_{s^{t+1}} Ra_{t+1}(s^t) \pi(s^{t+1}) \lambda_{t+1}(s^{t+1}) \) hence the \( t+1 \) term above.
    Then:
    \[b_1 - b_2 c_t(s^t) = \beta R \sum\limits_{s^{t+1}} \frac{\pi(s^{t+1})}{\pi(s^t)} \paren{b_1 - b_2 c_{t+1}(s^{t+1})}\]
    This simplifies since \( \pi(s^{t+1}) = \pi(s^t \land s_{t+1}) \):
    \[b_1 - b_2 c_t(s^t) = \beta R \sum\limits_{s^{t+1}} \pi\paren{s_{t+1} \middle| s^t} \paren{b_1 - b_2 c_{t+1}(s^{t+1})} = \beta R \operatorname{Ex}_t\bracket{b_1 - b_2 c_{t+1} (s^{t+1})}\]
    This is exactly the Martingale statement above since \( \beta R = 1 \).
b. 

