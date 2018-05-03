---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Growth Models
\vspace{-2ex}
Growth correlates with investment and accumulation of capital, including both physical and human capital.
\vspace{-2ex}

### Solow Growth Model

Consider the intermediary between integer discrete time and continuous time, where the time intervals are spaced by \(\Delta\) instead of by \(1\).

Growth is now \( \lim\limits_{\Delta \to 0} \frac{y(t+\Delta) - y(t)}{\Delta} = \dot{y}(t)\) instead of \( \frac{y_{t+1} - y_t}{1} \).

1. Aggregate production function \( Y(t) = AF(K(t), N(t)) \) where \( A \) is total factor productivity
   a. \( F \) is CRS
   b. \( F_K > 0 \) and \( F_N > 0 \)
   c. \( F_{K,K} < 0 \) and \( F_{N,N} < 0 \)
   d. Inada conditions

2. Law of Motion for Capital
   * Discrete time: \( K_{t+1} = (1-\delta) K_t + I_t \)
   * Continuous time: \( K(t+\Delta) = (1-\delta \Delta)K(t) + I(t)\Delta \) or in the limit case \( \dot{K}(t) = I(t) - \delta K(t) \)

3. Savings function (closed economy) \( I(t) = S(t) = s Y(t) \) where \( s \) is average propensity to save.
   * For a more complicated model (with more realistic savings function based on PIH, etc\ldots) see the Ramsey-Cass-Koopmans model with a household dynamic optimization problem here instead.

We can just use Cobb-Douglas \( Y(t) = A {K(t)}^\alpha {N(t)}^{1-\alpha} \).
This is \( y(t) = A {k(t)}^\alpha \) per worker.
The derivative of the log of that is \( \frac{\dot{y}(t)}{y(t)} = \alpha\frac{\dot{k}(t)}{k(t)} \).
Then by substitution into the law of motion for capital, we have \( \dot{K}(t) = s A {K(t)}^\alpha {N(t)}^{1-\alpha} - \delta K(t) \).
Per worker, this is \( \frac{\dot{K}(t)}{N(t)} = s A {k(t)}^\alpha - \delta k(t) \).
Substitute by:
\[ \dot{k}(t) = \frac{\partial}{\partial t} \pfrac{K(t)}{N(t)} = \frac{\dot{K}(t)}{N(t)} - \pfrac{\dot{N}(t)}{N(t)} \pfrac{K(t)}{N(t)} = \frac{\dot{K}(t)}{N(t)} - n k(t) \]
and the result is the Solow Growth Equation \( \dot{k}(t) = sA{k(t)}^\alpha - (\delta + n)k(t) \).

The steady-state capital stock where savings is equal to depreciation is when \( \dot{k}(t) + nk(t) = sA {k(t)}^\alpha - \delta k(t) \) is at equilibrium, then \( sA{k^*}^\alpha = (\delta + n) k^* \), which has equilibrium \( k^* = \pfrac{sA}{\delta + n}^{\frac{1}{1-\alpha}} \).

Increased savings or technology level increases equilibrium capital stock.
Effective depreciation decreases the equilibrium capital stock.
It is also increasing in \( \alpha \), which determines the concavity.

The model gives conditional convergence but not absolute convergence.

### Golden Rule of Capital Accumulation
What steady-state capital \( k^G \) maximizes consumption?
When \( sA{k^*}^\alpha = (\delta + n) k^* \) adjusted savings equal depreciation.
Then we have the conditions \( c^* = y^* - i^* \) from \( Y = C + I + G + NX \), and \( s^* = i^* \), so \(c^* + s^* = y^* \) and \( s^* = y^* - c^* \).
Then from the above \( c^*(k^*) = A{k^*}^\alpha - (\delta + n)k^* \) is maximized when \( \delta + n = \frac{\alpha A}{{k^*}^{1-\alpha}} \).
This is the golden rule of accounting: \( k^* = \pfrac{\alpha A}{\delta + n}^{\frac{1}{1-\alpha}} \).

### Dynamic Inefficiency
If \( s > \alpha \) there is "oversaving" and the economy is dynamically inefficient, because the economy moves from \( k^* \) to \( k^G \) by increasing consumption monotonically.
China presently, Japan in the miracle, and Italy in the 1970s experienced this.
If \( s < \alpha \) then the economy is inefficient \( k^* \neq k^G \) but not dynamically: the transition to the optimal has loss before gains.
Let's consider the labor share as \( \alpha \) increases, then the labor share \( \frac{wn}{y} = 1 - \alpha \) goes down.

## Growth Models with exogenous technical change

Consider when \( \dot{k}(t) = s A(t) {k(t)}^\alpha - (\delta + n) k(t) \).
Perhaps \( A(t) = A_0 e^{\gamma t} \) then \( \frac{\dot{A}(t)}{A(t)} = \gamma \).

### AK model

Limit case of Solow Model as \( \alpha \to 1 \):
\( \dot{k}(t) = s A k(t) - (\delta + n) k(t) \)

When \( sA > \delta + n\) then from \( \frac{\dot{k}(t)}{k(t)} = sA - \delta - n \) there is perpetual endogenous growth.
This assumes no decreasing marginal returns in capital accumulation, which seems unrealistic
However, if human capital appreciation is modeled in capital then the production function is linear in this aggregate capital concept, then this model describes endogenous growth due to continuously linearly increasing capital productivity.

* What is the reproducible factor of production?

  Physical capital \( k \), through investment

* Are there decreasing marginal returns in the production of this factor?

  Yes when \( \alpha < 1 \). No when \( \alpha = 1 \).
  If no, then there is endogenous growth.

### Endogenous growth with human capital

\( Y(t) = A {H(t)}^\alpha \paren{N(t) u(t)}^{1 - \alpha} \) where \( u(t) : [0, 1] \) is the fraction of time devoted to work (and the rest to learning), and \( \dot{h}(t) = b(1-u(t)) h(t) \) is the stock of human capital, and \( b \) is quality of schooling.
Then express per-capita \( y(t) = A{h(t)}^\alpha {u(t)}^{1-\alpha} \)
Take log and derivative then \( \frac{\dot{y}(t)}{y(t)} = \alpha \frac{\dot{h}(t)}{h(t)} + (1 - \alpha) \frac{\dot{u}(t)}{u(t)} \).
Balanced growth, or constant \( g_y \), is not possible when \( \alpha < 1 \), since \( u \) is bounded and thus cannot grow at a nonzero constant rate.

* What is the reproducible factor of production?

  Human capital

* Are there decreasing marginal returns in the production of this factor?

  No, since \( \dot{h}(t) = \alpha b (1 - u^*) h(t) \sim h(t) \), so there is endogenous growth.

This model confirms highly productive education and high rates of education participation are correlated with perpetual growth, as is the relevance of human capital, as e.g.\ innovation or research, not as physical labor.
