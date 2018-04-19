---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---


## Tax Smoothing

Due to the disutility of working being concave up, note \( v(h_1) + v(h_2) \geq v_1\pfrac{h_1 + h_2}{2} \) when \( v \) is given.

This tells us \( \tau_1^* = \tau_2^* \) (minimization of distortions).

## Labor Markets

\( P_t \) working age (16-65) population can be partitioned into participating (labor force) \( L_t \) and nonparticipating (early retirees, students, disabled, discouraged workers) \(N_t \), and labor force can be further partitioned into employed \( E_t \) and unemployed (actively searching) \( U_t \).

Unemployment rate \( u_t = \frac{U_t}{L_t} \) (currently around \( 4.1 \%\)).

## Search Model

Employed worker at wage \( w \) discounts future income at \( b \) with probability \( \sigma \) of separation has value \( V_e(w) = w + \beta\paren{\sigma V_u + (1 - \sigma) V_e(w)}  = \frac{w + \beta \sigma V_u}{1 - \beta(1 - \sigma)} \) then when \( \sigma = 0 \), \( V_e(w) = \frac{w}{1-\beta} \).

Unemployed worker samples a job every period from distribution with C.D.F.\ \( G(w) \) models an optimal stopping problem: \(V_u = b + \beta \int\limits_{0}^{\bar{w}} \max(V_e(w), V_u) dG(w) \)

Given the reservation wage \(w^*\) such that \( V_e(w^*) = V_u \), then \( V_u = V_e(w^*) = \frac{w^*}{1-\beta} \).

\[V_u = b + \beta \int\limits_{0}^{\bar{w}} \max\paren{ V_e(w), V_u} dG(w) \]
\[V_u - \beta V_u = b + \beta \paren{ \int\limits_{0}^{\bar{w}} \max\paren{ \frac{w + \beta \sigma V_u}{1 - \beta(1 - \sigma)} , V_u} dG(w)  -  V_u} \]
\[V_u(1 - \beta) = b + \beta  \int\limits_{0}^{\bar{w}} \max\paren{ \frac{w + \beta \sigma V_u}{1 - \beta(1 - \sigma)} - V_u, 0} dG(w) \]
\[ w^* = b + \beta  \int\limits_{0}^{\bar{w}} \max\paren{ \frac{w - w^*}{1 - \beta(1 - \sigma)}, 0} dG(w) \]
\[ w^* = b + \pfrac{\beta}{1-\beta(1-\sigma)} \int\limits_{0}^{\bar{w}} \max\paren{ w - w^*, 0} dG(w) \]
\[ w^* = b + \pfrac{\beta}{1-\beta(1-\sigma)} \int\limits_{w^*}^{\bar{w}}  w - w^* dG(w) \]
\[ w^* = b + \pfrac{\beta}{1-\beta(1-\sigma)} \Ex{w - w^* \middle| w > w^*} \]
