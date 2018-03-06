---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Euler Equation
Consider the household problem in endowment economy, \( \max\limits_{c_1, c_2} u(c_1) + \beta u(c_2) \) such that \( c_1 + \frac{c_2}{1 + r_2} = y_1 + \frac{y_2}{1 + r_2} \).

Then we have the MRS \( \frac{u_c(c_1)}{u_c(c_2)} = \beta ( 1 + r) \), which is the Euler equation (the intertemporal first order condition).

To get a closed form, consider some utility functions:

### Constant Elasticity of Substitution
CS utility is \( u(c) = \frac{c^{1-\gamma} - 1}{1 - \gamma} \) for \( \gamma \in [0, \infty) \) coefficient of relative risk aversion.

Note \( \gamma = 0 \) is linear utility, \( \gamma = 1 \) is log utility, and \( \gamma \to \infty \) is Leontief utiilty \( \min \paren{c_1, c_2} \).

The elasticity of intertemporal substitution is then \( \frac{1}{\gamma} \).
These two constants are not directly related in every utility function, and their simple relation with CS is why we are using it here.

Since \( u_c = c^{-\gamma} \), then the Euler equation is \( \frac{c_2}{c_1} = \paren{\beta(1+r)}^{\frac{1}{\gamma}} \)

Then the intertemporal allocation of consumption is controlled by three forces: patience / discounting \( \beta \) (low expedites consumption), return on savings \( r \) (high postpones consumption), and willingness to substitute across time \( \frac{1}{\gamma} \) (high amplifies \( \beta(1+r) \) ).

\( \log c_2 - \log c_1 = \frac{1}{\gamma} \paren{\log(1 + r) + \log(\beta)} \)

For small \( x \), \( \log (1 + x) \approx x \), and let \( \beta = \frac{1}{1 + \rho} \) for discount rate \( \rho \in [0, \infty) \), so \( \Delta \log c_t \approx \frac{r - \rho}{\gamma} \)

\newpage
## Imperfections in the Model

### Borrowing Limits

In the setup for the endowment economy --- \( \max\limits_{c_1, c_2} u(c_1) + \beta u(c_2) \) such that \( c_1 + s = y_1 \) and \( c_2 = y_2 + (1 + r) s \) --- we assume we can borrow any amount of money.
However, there are some borrowing limits.

The simplest is the ad-hoc limit \( s \geq -b \).

The Inada conditions on utility, \( U(0) = -\infty \), tell us we cannot borrow more than we can pay back, leading to the natural borrowing limit \( s \geq \frac{-y_2}{1+r} \).
This cannot be a binding constraint due to Inada conditions.

Suppose your house has value \( H \) then we can use the house as collateral \( s \geq - \phi H \) where \( \phi \) represents the rate at which the bank discounts the value of the house comapred to equivalent dollar value due to illiquidity.


1. Solve the relaxed problem without hte borrowing limit.
2. Check that the borrowing constraint is not binding.
3. If it is, solve the optimization problem with the constraint as an equality constraint.

### Borrowing Asymmetry
Suppose there is a wedge between the borrowing rate and the saving rate \( r^b > r^s \).

Then you get \( c_2 = y_2 + (1 + r^s) s \) when \( s \geq 0 \).

But you only get \( c_2 = y_2 + (1 + r^b) s \) when \( s < 0 \).

1. Intermediation Cost:
For the bank \( \Pi(s) = -r^s s + (r^b - k) s \).
In perfect competition \( r^b = r^s + k \).

2. Compensation for Risk of Default:
\( \pi(S) = -r^s s + q r^b s \) then \( r^b = \frac{r^s}{q} \geq r^s \)

There is a kink in the budget constraint at the zero-savings point between the constraint for borrowing and the constraint for saving.

1. Guess \( s > 0 \) and solve with \( r = r^s \).
Solve and verify \( \widetilde{c_1} < y_1 \).
If so, \( c_1^* = \widetilde{c_1} \) (stop).
2. Guess \( s < 0 \) and solve with \( r = r^b \).
Solve and verify \( \widetilde{c_1} > y_1 \).
If so, \( c_1^* = \widetilde{c_1} \) (stop).
3. Otherwise, \( c_1^* = y_1 \) and \( c_2^* = y_2 \).
