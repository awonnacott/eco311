---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---


## Social Security

Two systems:

* Fully funded
* Pay-as-you-go

Given endowment economy \( y_1 = y \) with work at \( t = 1 \) and retirement at \( t = 2 \).

Preferences \( U(c_t^y, c_{t+1}^o) = 2\sqrt{c_t^y} + \beta 2 \sqrt{c_{t+1}^o} \) with \( \beta = 1\)

Assume population growth \( N_{t+1} = (1+n)N_t \) and output growth \(y_{t+1} = (1+g)y_t \).

Under the fully funded system, the budget constraints are \( c_t^y + a = y-\tau_y \) and \( c_{t+1}^o = (1+r)(a + \tau_y) \).
The utility-maximizing \( a = \paren{\frac{1+r}{2+r} - \tau} y \), showing mandated savings \( \tau_y \) crowding out individual savings at rate of return \( 1 + r \).

Under the pay-as-you-go system, \( B_t = \tau y_t N_t \) so \( \frac{B_t}{N_{t-1}} = \tau y_t \frac{N_t}{N_{t-1}} = \tau y_t(1+n) = \tau y_{t-1} (1+g)(1+n) \) so the payoff is better when \( (1 + g)(1 + n) > (1 + r) \), e.g.\ approximately when \( g + n > r \).

## Optimal Taxation

* Government makes choices subject to constraints
    * Benevolent: maximizes welfare of citizens
    * Political economics: simple model: median voter
* Optimal labor income tax
* 2-period income model
* \( g \) in the first period with \( \curly{\tau_i}_{t=1}^2 \)
* Preferences are quasilinear: \( U(c_1, c_2, h_1, h_2) = c_1 - \frac{1}{2}h_1^2 + \beta\paren{c_2-\frac{1}{2}h_2^2} \)
* Indifferent about consumption when \( \beta(1+r) = 1 \) and otherwise consume at a corner solution
* \( y = Ah \Rightarrow w = A = 1 \) we can normalize the wage to 1
* Budget constraint: \( c_1 + \frac{c_2}{1+r} = (1-\tau-1)w_1h_1 + \frac{(1-\tau_2)w_2h_2}{1+r} \) tells us \( c_1 + \beta c_2 = (1-\tau_1)h_1 + \beta(1-\tau_2)h_2 \)
* Household problem is \( \max\limits_{h_1, h_2}  (1-\tau_1)h_1 + \beta(1-\tau_2)h_2 - \frac{1}{2}h_1^2 - \beta\frac{1}{2}h_2^2 \)
* How should the government set taxes given the FOCs of the above: \( h_1^* = (1-\tau_1) \) and \( h_2^* = (1-\tau_2) \).
* Government problem \( \max_{\tau_1, \tau_2} (1-\tau_1)h_1 + \beta(1-\tau_2)h_2 - \frac{1}{2}h_1^2 - \beta\frac{1}{2}h_2^2 \) such that \( g = \tau_1 h_1 + \beta \tau_2 h_2 \) and given that the household problem FOCs above are met
* A Ramsey equilibrium is a C.E.\ with endogenous taxes, i.e.\ tax levels and household choices such that:
    1. Given taxes, households and firms optimize
    2. Markets clear
    3. Intertemporal budget budget constraint is balanced
    4. Government optimizes the government problem subject to the household reaction function
* \( \mathcal{L} = \frac{1}{2} (1-\tau_1)^2 + \beta \frac{1}{2} (1-\tau_2)^2 + \lambda\paren{\tau_1(1-\tau_1) + \beta\tau_2(1-\tau_2) - g} \) then \( \tau_1^* = \tau_2^* = \frac{\lambda - 1}{2\lambda - 1} \).
* This result is called tax smoothing: taxes should be the same in both periods.
