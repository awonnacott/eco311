---
header-includes: |
    \usepackage[margin=1in]{geometry}
---

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
2. Agents
3. Commodity set - Two goods:
    * Input: labor services \( h \)
    * Output - Final good - Consumption:
        * Private \(c\)
        * Public \(g\)
4. Markets
    1. Final good market
    2. Labor market
5. Time constraint \(h+l=1\)
    * Time allocated to work \(=\frac{8\cdot 5\cdot 50}{16\cdot 365}=\frac{1}{3}\)
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
    * In dollar terms, with price \(p\), quantity \(c\), nominal wage \(w\), dividend \(d\), lump sum tax \(t\):

        \( pc \leq w^N h + d^N - t^N \) where \(N\) tags as nominal.
    * In real terms, with numeraire of economy \(c$, then other variables in terms of \(c\):
    \( c \leq wh + d - t \)
    where \(h = 1-l\)
    * Shown with budget constraint as non-axis boundary of budget set, and wage is the price of leisure, illustrated by
    \( c + wl \leq w + d - t \)
6. Production Technology
    * Total factor productivity \( z \), labor \( m \), capital \( k \): \( y = zf(k, m) \)
    * Propreties of \(f\)
        1. Monotonicity: marginal product of labor \(f_m > 0\), marginal product of capital \(f_k > 0 \)
        2. Concavity: decreasing marginal returns
            * Two inputs are complementary if \( f_{mk} \geq 0 \)
        3. Linearity: constant returns to scale
            * Increasing returns to scale is \(f(\alpha k, \alpha m) > \alpha f(k, m)\)

    * Common \(f\):
        * Cobb-Douglas: \( y = zk^\alpha m^{1-\alpha} \) for \( \alpha \in (0, 1) \)
        * Constant Elasticity of Substitution subsumes Cobb-Douglas when \(\gamma = 0 \):

            \( y = z\left[\alpha k^\gamma (1-\alpha)m^\gamma\right]^{\frac{1}{\gamma}}\) for \( \gamma \in (-\infty, 1), \alpha \in (0, 1) \)
7. Government
   * Government budget constraint \( g = t \) where spending \(g\) is a parameter.
