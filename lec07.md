---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

# Dynamic Production Economy

1. Time: \( t \in \curly{1, 2} \)
3. Commodity set:
   * Final good (consumption and investment)
   * Labor services
   * Capital services:
       * supply \( a_t \) units of capital (wealth)
       * firm demand for capital \( k_t \)
       * \(( 1-\delta) a_t \) undepreceiated capital returned where \( \delta \) is the depreciation rate
       * Net rental rate \( r_t \) then rented capital \( ( r_t + \delta) a_t \); note \( r_t + \delta \) is the gross rental rate
       * Hoseholds then get back \( (1 + r_t )a_t\)
   * Households have an endowment \( \bar{a}_1 \) of wealth
4. All markets competitive
5. Preferences:
   * Households live for 2 periods, so \( U(c_1, c_2, l_1, l_2) = u(c_1, l_1) + \beta u(c_2, l_2) \) where \(\beta \in [0, 1] \) is the discount factor
6. Technology
   * \( y_t = z_t f(k_t, n_t) \) as before
   * Constraint: \( f \) has constant retunrs to scale
   * \( k_{t+1} = (1-\delta) k_t + i_t \) where \( i_t \) is gross investment
   * Net investment is gross investment less depreciation \( k_{t+1} - k_t \)
7. Government
   * Taxes labor income at net \( \tau_t \) and transfers lump-sum to households the tax revenuse \( b_t \)

\newpage
## Household Problem

* Labor income is \( (1-\tau_1)w_1(1-l_1) \)
* Capital income is \( r_1 a_1 + d_1 \) interest and dividends

\( \max\limits_{a_2, \curly{c_t, l_t}_{t=1}^t} u(c_1, l_2) + \beta u(c_2, l_2) \) such that:

* the first budget constraint \( c_1 + a_2 = (1-\tau_1)w_1(1-l_1) + (1+r_1) \bar{a}_1 + d_1 + b_1 \)
* the second budget constraint \( c_2 = (1-\tau_2)w_2(1-l_2) + (1+r_2) a_2 + d_2 + b_2 \)
* usual bound on \( c_t \) and \( l_t \) ignored due to Inada assumptions

Savings: \( s_1 = y_1^D - c_1 = (1-\tau_1)w_1(1-l_1) + (1+r_1) \bar{a}_1 + d_1 + b_1 - c_1 \) are exactly \( a_2 - a_1 \)

* Lifetime budget constraint: substitute into \( a_2 \) in the first budget constraint the second budget constraint solved for \( a_2 \)
\[ c_1 + \frac{c_2}{1 + r_2}
    = (1-\tau_1)w_1(1-l_1) + \frac{(1-\tau_2)w_2(1-l_2)}{1 + r_2}
    + (1+r_1) \bar{a}_1 + d_1 + \frac{d_2}{1 + r_2}
    + b_1 + \frac{b_2}{1 + r_2} \]
The relevant Lagrangian is:

\begin{multline*} \mathcal{L}(c_1, c_2, l_1, l_2, \lambda) = u(c_1, l_2) + \beta u(c_2, l_2) \\
+ \lambda\paren{
(1-\tau_1)w_1(1-l_1) + \frac{(1-\tau_2)w_2(1-l_2)}{1 + r_2}
    + (1+r_1) \bar{a}_1 + d_1 + \frac{d_2}{1 + r_2}
    + b_1 + \frac{b_2}{1 + r_2}
    - c_1 - \frac{c_2}{1 + r_2}
}
\end{multline*}

From consumption FOCs
\[ \mathcal{L}_{c_1} = 0 \Leftrightarrow u_c(c_1^*, l_1^*) = \lambda \]
\[ \mathcal{L}_{c_2} = 0 \Leftrightarrow \beta u_c(c_2^*, l_2^*) = \frac{\lambda}{1 + r_2} \]
then we find the **Euler equation**:
\[\frac{ u_c(c_1^*, l_1^*) }{ u_c(c_2^*, l_2^*) } = \beta (1 + r_2)\]
which is a general result which holds in multi-period economies: the intertemporal consumption allocation is determined by the discount factor and the interest rate.

From leisure FOCs
\[ \mathcal{L}_{l_1} = 0 \Leftrightarrow u_l(l_1^*, l_1^*) = \lambda (1 - \tau_1) w_1\]
\[ \mathcal{L}_{l_2} = 0 \Leftrightarrow \beta u_l(l_2^*, l_2^*) = \frac{\lambda(1 - \tau-2) w_2}{1 + r_2} \]
then we find the intratemporal MRS:
\[\frac{ u_l(c_1^*, l_1^*) }{ u_c(c_2^*, l_2^*) } = (1 - \tau_t) w_t\]
Note the distortionary taxes ensure a non-Pareto-optimal competitive equilibrium.

And as above the intertemporal time allocation is determined by the dicount factor, interest rate, wage, and taxes.
\[\frac{ u_l(c_1^*, l_1^*) }{ u_l(c_2^*, l_2^*) } = \frac{(1 - \tau_1) w_1}{(1 - \tau_2) w_2} \beta (1 + r_2)\]

\newpage
## Firm Problem

\[ d_t = \Pi_t = \max\limits_{\curly{n_t, k_t}_{t=1}^2} z_tf(k-t, n_t) - w(t n_t - (r_t + \delta) k_t \]

Marginal product of labor \( z_t f_n (n_t, k-t) = w_t \)

Marginal product of capital \( z_t f_k(k-t, n_t) = r_t + \delta \)

With constant returns to scale this only constrains the ratio.

### Theorem: If \( f(x, y)\) is CRS, then \( f(x, y) = f_x(x) + f_y(y) \)

Proof: CRS means \( f(\theta x, \theta y) = \theta f(x, y) \forall \theta > 0 \)

Differentiate by \( \theta \), then set \(\theta = 1\):
\[\frac{\partial f(\theta x, \theta y)}{\partial \theta} \mid_{\theta = 1} = f_x(x, y) x + f_y(x, y) y\]
\[\frac{\partial \theta f( x, y)}{\partial \theta} \mid_{\theta = 1} = f(x, y) \]

\[\Pi_t = z_t f(k_t, n_t) - z_t f_k k_t - z_t f_n N-t = z_t \paren{f(k_t, n-t) - f_n(n_t) - f_k k_t} = 0 \]
Then with CRS, \( \Pi_t = 0 \) always!

## Government

\( \tau_t w_t (1 - l_t) = b_t \) at each \(t\)
