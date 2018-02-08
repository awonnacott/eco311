# Primitives of an Economy
1. Time
    * Static
    * Dynamic
    * Continuous: \(t\in [0, T]\)
    * Discrete: \(t\in\mathbb{Z}\)
2. Agents:
    * Households
    * Firms
    * Government
    * Fiscal authority
    * Monetary authority
3. Commodity set
    * Inputs and outputs: Commonly restricted to \(\mathbb{R}^+\)
4. Market structure
5. Preferences
5. Budget constraint
5. Time constraint
6. Production technology
7. Government budget constraint

\newpage
# Static Economy
1. Time: static
3. Commodity set - Two goods:
    * Input: $h =$ labor services
    * Output - Final good - Consumption:
        * Private = c
        * Public = g
4. Markets
    1. Final good market
    2. Labor market
5. Time constraint \(h+l=1\)
    * Time allocated to work \(=\frac{8*5*50}{16*365}=\frac{1}{3}\)
5. Preferences
    * Utility function \(u(c,l,g)=U(c,l)+V(g)\) meets the following properties:
        1. Monotonicity: First derivative is positive
        2. Concavity: Second derivative is negative (decreasing marginal utility)
        * Preferences only defined on the monotonically increasing range and are concave down on that region.
    * Indifference curves
    * Marginal rate of substitution = slope of indifference curve
    * MRS higher on the indifference curve is higher (slope of indifference curve is is negative convex up)
    * Preferences are convex
    * Preference for variety: a convex combination of two points on an indifference curve is strictly preferred to those points.
    * Inada Conditions: avoid corner cases / ensure global optimum is always a local optimum
        * \( \lim\limits_{c \to 0} U_c = \infty \)
        * \( \lim\limits_{l \to \infty} U_l = \infty \)
5. Budget constraint
    * In dollar terms, with price $p$, quantity $c$, nominal wage $w$, dividend $d$, lump sum tax $t$:
    \( pc \leq w^N h + d^N - t^N \) where $N$ tags as nominal.
    * In real terms, with numeraire of economy $c$, then other variables in terms of $c$:
    \( c \leq wh + d - t \)
    where $h = 1-l$
    * Shown with budget constraint as non-axis boundary of budget set, and wage is the price of leisure, illustrated by
    \( c + wl \leq w + d - t \)
