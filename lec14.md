---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Savings Models

1. Intentional Saving: \( \beta R > 1 \)
2. Consumption Smoothing: Concavity of \( u \) when \( \beta R = 1 \)
3. Precautionary Saving: \( u''' > 0 \)
4. Life-Cycle Motive (Retirement): Consumption smoothing given expectation of retirement
5. Bequest Motive: Want to leave money to your children

Wealth calculation: \( a_t + \sum\limits_{\tau = t}{T} R^{-(\tau - t)} y_{\tau} = \sum\limits_{\tau = t}^{T} R^{-(\tau - t)} c_{\tau} \)

## Asset Pricing

### Real estate

### Bonds

Safe asset returns a roughly constant \( R^b \approx 1\% \)

### Stocks

Risky asset returns \( R^e \approx 6\% \) with much higher variance

### Equity Premium

Compensation for risk \( R^e - R^b \approx 5\% \)

\newpage
## 2-period Endowment Economy with Uncertainty

\( s \in \mathcal{S} = \curly{s^L, s^H} \) with \( \pi \) a distribution over these outcome states and \( y_2(s^L) < y_2(s^H) \)

### Bonds
\( \max\limits_{c_1, c_2(s)} \frac{{c_1}^{1-\gamma}}{1-\gamma} + \beta \sum\limits_{s \in \mathcal{S}} \pi(s) \frac{{c_2(s)}^{1-\gamma}}{1-\gamma} \) such that \( \forall s, c_1 + \frac{c_2(s)}{R^b} = y_1 + \frac{y_2(s)}{R^b} \)

\[ \mathcal{L} = \frac{{c_1}^{1-\gamma}}{1-\gamma} + \sum\limits_{s \in \mathcal{S}} \pi(s) \paren{ \beta \frac{{c_2(s)}^{1-\gamma}}{1-\gamma} + \lambda_s \paren{ y_1 + \frac{y_2(s)}{R^b} - c_1 - \frac{c_2(s)}{R^b} } } \]
\[ \frac{\partial \mathcal{L}}{\partial c_1} = 0 \Rightarrow c_1^{-\gamma} = \Ex{\lambda_s} \]
\[ \frac{\partial \mathcal{L}}{\partial c_2(s)} = 0 \Rightarrow \pi(s) \beta c_2(s)^{-\gamma}  = \pi(s) \frac{\lambda_s}{R^b} \]
\[ R^b \sum\limits_{s \in \mathcal{S}} \pi(s) \beta c_2(s)^{-\gamma} = \Ex{\lambda_s} =  c_1^{-\gamma} \]
\[ R^b \sum\limits_{s \in \mathcal{S}} \pi(s) \pfrac{\beta {c_2(s)}^{-\gamma}}{c_1^{-\gamma}} = 1 \]
Note that the summand is just the marginal rate of substitution, so \( R^b \Ex{\operatorname{MRS}(s)} = 1 \).
So the decision about bond investment can be made only on the expectation of the future and not on the actual outcome.

### Stocks
\( \max\limits_{c_1, c_2(s)} \frac{{c_1}^{1-\gamma}}{1-\gamma} + \beta \sum\limits_{s \in \mathcal{S}} \pi(s) \frac{{c_2(s)}^{1-\gamma}}{1-\gamma} \) such that \( \forall s, c_1 + \frac{c_2(s)}{R^e(s)} = y_1 + \frac{y_2(s)}{R^e(s)} \)

\[ \mathcal{L} = \frac{{c_1}^{1-\gamma}}{1-\gamma} + \sum\limits_{s \in \mathcal{S}} \pi(s) \paren{ \beta \frac{{c_2(s)}^{1-\gamma}}{1-\gamma} + \lambda_s \paren{ y_1 + \frac{y_2(s)}{R^e(s)} - c_1 - \frac{c_2(s)}{R^e(s)} } } \]
\[ \frac{\partial \mathcal{L}}{\partial c_1} = 0 \Rightarrow c_1^{-\gamma} = \Ex{\lambda_s} \]
\[ \frac{\partial \mathcal{L}}{\partial c_2(s)} = 0 \Rightarrow \pi(s) \beta c_2(s)^{-\gamma}  = \pi(s) \frac{\lambda_s}{R^e(s)} \]
\[ \sum\limits_{s \in \mathcal{S}} \pi(s) R^e(s)  \beta c_2(s)^{-\gamma} = \Ex{\lambda_s} =  c_1^{-\gamma} \]
\[\sum\limits_{s \in \mathcal{S}} \pi(s)  R^e(s) \pfrac{\beta {c_2(s)}^{-\gamma}}{c_1^{-\gamma}} = 1 \]
Note that unlike before we cannot take the return rate out of the sum, so we get \( \Ex{R^e(s) \operatorname{MRS}(s)} = 1 \).

## Equity Premium
Then by using covariance we have \( \Ex{R^e(s)}\Ex{ \operatorname{MRS}(s)} = 1 - \operatorname{cov}\paren{R^e(s), \operatorname{MRS}(s)} \).

Substituting by the above we get \( \frac{\Ex{R^e(s)} - R^b}{R^b} = -\operatorname{cov}\paren{R^e(s), \operatorname{MRS}(s)} \) is the excess return on equity investment and contains the compensation for taking risk.
