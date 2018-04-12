---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Investment
* Addition to capital stock
* _Firm_
* Intertemporal tradeoff: can decide to invest more today (reduces profits today) in order to increase production (and thus also profits) in the future
* Infinite planning horizon
* Maximize discounted present value of profits  with production function having \( f_k > 0 \) and \( f_{k,k} < 0 \) and \( k_{t+1} = (1-\delta) k_t + I_t \) and discounted exactly at the interest rate \( 1 + r \):
\[ \max V_t = \max \sum\limits_{j=0}^{\infty} \pfrac{1}{1+r}^j \Pi_{t+j} = \max\limits_{\curly{I_{t+j}}_{j=0}^{\infty}}\sum\limits_{j=0}^{\infty} \pfrac{1}{1+r}^j  \paren{z_{t+j} f(k_{t+j}) - p_{t+j}I_{t+j}} \]
* Substitute motion for capital into capital in objective function and maximize over \( k_{t+j+1} \)
\[ \max V_t = \max\limits_{\curly{k_{t+j+1}}_{j=0}^{\infty}}\sum\limits_{j=0}^{\infty} \pfrac{1}{1+r}^j  \paren{z_{t+j} f(k_{t+j}) - p_{t+j} \paren{k_{t+j+1} - (1-\delta) k_{t+j}}} \]
\[ \operatorname{FOC}(k_{t+1}) : \pfrac{1}{1+r}\paren{z_{t+1} f_k(k_{t+1}) + p_{t+1}(1-\delta)} = p_t \]
* Marginal cost is equal to anti-depreciated marginal value, where marginal value is marginal product of capital plus resale of the excess capital.
Note that the resale value change calculates obsolescence (technological progress) whereas \( \delta \) captures physical depreciation (decay).
* \( f(k_t) = \frac{1}{\alpha} k_t^{\alpha} \) so \( f_k = k_t^{\alpha - 1} \) then we have \( (1+r) p_t - (1-\delta) p_{t+1} = z_{t+1} k_{t+1}^{\alpha - 1} \).
\[ k_{t+1}^* = f^{-1}\pfrac{z_{t+1}}{(1+r) p_t - (1-\delta) p_{t+1}}= \pfrac{z_{t+1}}{(1+r) p_t - (1-\delta) p_{t+1}}^{\frac{1}{1-\alpha}} \]
* Firm invests more when: \( z_{t+1} \) rises; \( p_t \) fall; \( r \) falls, \( \delta \) falls, \( p_{t+1} \) rises.
* This prices capital at \( p_t = \frac{z_{t+1}k_{t+1}^{\alpha - 1}}{1+r} + \pfrac{1-\delta}{1+r} p_{t+1} \) corresponds to the asset pricing equation \( p_t = y_t + \beta p_{t+1} \) where the dividend is the revenues provided and the discounting is the depreciation and the interest.
* Substituting the recurrence yields \( p_t = \pfrac{1}{1+r} \sum\limits_{j=0}^{\infty} \pfrac{1-\delta}{1+r}^j z_{t+j+1} k_{t+j+1}^{\alpha - 1} \) which is exactly discounted present value of dividends (noting that capital is productive starting next period) and is the fundamental value of capital.
Bubble can be included just as in last lecture.

### Adjustment costs: Tobin's q Theory of Investment

Adjustment costs \( c(I_t, k_t) = \frac{\phi}{1+\eps} \paren{\frac{I_t}{k_t} - \delta}^{1+\eps}k_t \) correctly hold \( c(\delta k_t, k_t ) = 0 \)

\[ \mathcal{L} = \sum\limits_{j=0}^\infty \pfrac{1}{1+r}^j \paren{z_t+j f(k_{t+j}) - p_{t+j} I_{t+j} - c(I_{t+j}, k_{t+j}) + q_{t+j} \paren{(1+\delta)k_{t+j} + I_{t+j} - k_{t+j+1}}} \]
\[ \operatorname{FOC}(I_t): p_t + c_I(I_t, k_t) = q_t \]
Marginal value equals marginal cost.

Given \( \eps > 0 \) and \( c \) and \( f \) having constant returns to scale then \( \phi\paren{\frac{I_t}{k_t} - \delta}^{\eps} = q_t - p_t \).
Then log of investment rate in excess of replacement is affine in log of \( q_t - p_t \).
So investment should go up when the shadow value is above the investment cost.
Assertion: \( q_t = \frac{V_t}{k_t} \) is both the marginal value and the average value of capital.
Also the stockholder value divided by value of assets.
