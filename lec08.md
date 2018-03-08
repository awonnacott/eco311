---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Competetive Equilibrium for Dynamic Production Economy

Given \( \bar{a}_1\), \(\curly{\tau_t}_t\), a competitive equilibrium is:

* a set of allocations (10, skip \(d\)): \( \curly{c_t, l_t, n_t, k_t}_t \), \(\curly{a_t}_t\), \(\curly{d_t}_t\)
* a set of prices (4): \(\curly{w_t, r_t}_t \)
* a government policy (2): \(\curly{b_t}_t\)

such that:

1. Household Optimal (4): Given prices, taxes, and transfers, \( \curly{c_t, l_t}_t, a_t \) solve the Household Problem
   * FOC for labor at each time
   * Euler equation
   * Lifetime budget constraint
2. Firm Optimal (4, skip CRS condition): Given prices, \( \curly{n_t, k_t}\) solve the Firm problem
   * FOC for labor and capital at each time
   * \(\forall t, d_t = 0\) by CRS
3. Labor Market Clears (4): \( \forall t, n_t = 1 - l_t \) and \( \forall t, w_t = sf_n(n_t, k_t) \)
4. Capital Market Clears (4): \( \forall t, a_t = k_t \) and \( \forall t, r_t + \delta = z_t f_k(n_t, k_t) \)
5. Goods Market Clears (2, but skip due to Walras):
   * \( c_1 + i_1 = z_1 f(n_1, k_1) \)
   * \( c_2 = z_2 f(n_2, k_2) + (1-\delta) k_2 \)

    where investment \( s_1 = i_1 = k_2 - (1-\delta) k_1 \) is what is saved/invested between the time periods.
    As noted before \( i_1 - \delta k_1 = k_2 - k_1\) and \( s_1 = a_2 - \bar{a}_1 \), and we have \( s_1 = i_1 - \delta k_1 \) from national accounts.
6. Government balances budget (2): \( \forall t, b_t = \tau_t w_t n-t \)

## Planner Problem for Dynamic Production Economy

\( \max\limits_{c_1, l_1, c_2, l_2, k_2} u(c_1, l_1) + \beta u(c_2, l_2) \) such that

* First period feasible: \( c_1 + k_2 - (1-\delta) k_1 = z_1 f(1-l_1, k_1) \)
* Second period feasible: \( c_2 = z_2 f(1 - l_2, k_2) + (1-\delta)k_2 \)
\[
    \mathcal{L} = u(c_1, l_1) + \beta u(c_2, l_2)
    + \lambda_1 \paren{z_1 f(1-l_1, k_1) - c_1 - k_2 + (1-\delta) k_1}
    + \lambda_2 \paren{z_2 f(1 - l_2, k_2) + (1-\delta)k_2 - c_2}
\]
* FOC \(c_1\): \(u_c(c_1, l_1) = \lambda_1\)
* FOC \(c_2\): \(\beta u_c(c_2, l_2) = \lambda_2\)
* FOC \(l_1\): \(u_l(c_1, l_1) = \lambda_1 z_1 f_n(1-l_1, k_1)\)
* FOC \(l_2\): \(\beta u_l(c_2, l_2) = \lambda_2 z_2 f_n(1-l_2, k_2)\)
* FOC \(k_2\): \(\lambda_1 = \lambda_2 \paren{z_2 f_k(1-l_2, k_2) + (1-\delta)}\)

This gives us \( \frac{u_l(c_t, l_t)}{u_c(c_t, l_t)} = z_t f_n(1-l_t, k_t) \),
which is not the competitive equilibrium becaues it would have been \( (1-\tau_t) w_t\).
There is a wedge resulting in workers performing less labor.

The Euler equation comes out to \( \frac{u_c(c_1, l_1)}{u_c(c_2, l_2)} = \beta \paren{1 + z_2 f_n(1 - l_2, k_2) - \delta } \),
which is equal to \( \beta (1 + r_2) \) at competitve equilibrum by the firm MPC.

So the wedge is in the intratemporal first order condition due to the income tax.
By contrast, a tax on capital income would show up in the Euler equation (which would be \( \beta \paren{1 + (1 - \tau_k) r_2} \) at equilibrium).

\newpage
## Indifference Curves

Given \( U = u(c_1, l_1) + \beta u(c_2, l_2) \), we have \( 0 = u_c(c_1, l_1) dc_1 + \beta u_c(c_2, l_2) dc_2 \), or \( \frac{dc_2}{dc_1} \mid_{U = \bar{U}} = \frac{-u_c(c_1, l_1)}{\beta u_c(c_2, l_2)} \).

Just as the wage is the slope of the budget constraint in the static economy, \( 1 + r_2 \) is the slope of the budget constraint in the two period economy.

To see this, we look at a simpler model, the **Endowment Economy** , also called **Lucas Tree Economy** because you are 'growing your endowment on a tree'.
The one actor has \( y_1, y_2 \) as endowments, and responds to the storage rate \(1 + r_2 \):
\( \max\limits_{c_1, c_2} u(c_1) + \beta u(c_2) \) such that \( c_1 + a_2 = y_1 \) and \( c_2 = y_2 + (1 + r_2) a_2 \).
The lifetime budget constraint is \( c_1 + \frac{c_2}{1 + r_2} = y_1 + \frac{y_2}{1 + r_2} \).
Here it is clear that the slope is \( -(1 + r_2) \).

In general, just as the wage is a relative price (of leisure) it also seems sensible that the rental rate would be a relative price, namely \( 1 + r_2 = \frac{p_1}{p_2} \).
Real interest rate normalizes across changes in intertemporal purchasing power.
High interest rate means the goods in period 2 are cheaper in nominal prices.
The necessary equations to see this are \( p_1 c_1 + p_1 a_2 = p_1 y_1 \) and \( c_2 = y_2 + \frac{p_1}{p_2} a_2 \).
