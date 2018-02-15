---
header-includes: |
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Assumptions:

* Rationality
* Competitive behavior
* Prices as parameters (no adverse selection)

## Firm Problem

Maximize profits \( \max\limits_n \Pi^N(\overline{k}, n) = py - w^Nn \) where \( py \) is total production value and \(n\) is salary.
\( y = zf(\overline{k}, n) \)

Real: \( \max\limits_n \Pi(k, n) = y - wn \).
First order condition: \( zf_n(\overline{k}, n^*) = w\).

Marginal product of labor \( MPL(\overline{k}, n^*) = w \) is monotonically increasing concave down, initially very steep.
Optimal is when slope of MPL is equal to wage.

\( dw = zf_{n, n}(n^*, \overline{k}) dn^* \) so \( \frac{dn^*}{dw} = \frac{1}{zf_{n,n}(n^*, \overline{k})} \leq 0 \)

\( 0 = f_n (n^*, \overline{k}) dz + zf_{n, n}(n^*, \overline{k})dn^* \)
so
\( \frac{dn^*}{dz} = \frac{- f_n (n^*, \overline{k})}{ zf_{n, n}(n^*, \overline{k})} \geq 0 \)

Maximizing profits at \( \Pi^* = zf(n^*, \overline{k}) - wn^* = zf(n^*, \overline{k}) - f_n(n^*, \overline{k})n^* \),
then profits tell us \(d^*\)

## Competitive equilibrium for static economy

* Exogenous variables \( z, \overline{k}, g \)
* Endogenous variables: quantities \( c^*, l^*, n^*, d^*, y^* \), price \(w^*\), govt policty \(t^* \)

We want to find a set of endogenous variables such that:

1. Given \( w^*, d^*, t^* \), the household solution is \(c^*, l^* \)

2. Given \(w^*, z, \overline{k} \), the firm solution is \(n^*, d^*, y^* \)

3. Labor market clearing: \(1 - l^* = n^* \) and the equilibrium wage is \(w^* = zf_{n}(1-l^*, \overline{k}) \)

4. Goods market clearing: \( y^* = c^* + g \) (is a special case of the national accounting identity where \( i = 0 \) because that is the constraint of a static economy)

5. Government budget is balanced: \( g = t^* \) (becomes a much more complicated constraint if expenditures, transfers, taxes, government debt interest, etc\ldots come into play)


Mathematically:

1. Optimizing condition of the worker: \( \frac{U_l(c^*, l^*)}{U_c(c^*, l^*)} = w \)
2. Budget constraint of the worker: \( c^* = w^*(1-l^*) + d^* - t^* \)
3. Optimizing condition of the firm: \(zf_n(n^*, \overline{k}) = w^* \)
4. Budget constraint of the firm: \( y^* = zf(n^*, \overline{k}) \)
5. Output determination of the firm (dividend determination): \( d^* = zf(n^*, \overline{k}) - w^* n^* \)
6. Labor market clearing: \( 1 - l^* = n^* \)
7. Goods market clearing: \( y^* = c^* + g \)
8. Government budget: \( g = t^* \)

We get 8 equations with 7 variables, but one is dependent.

### Walras' Law
In a competitive equilibrium of an economy with \(n\) markets, if \(n-1\) markets clear then the \(n\)--th market is also going to clear.

You can always derive one market clearing condition from all the others.

* Verify starting from equation 2 --- \( c^* = w^*(1-l^*) + d^* - t^* \)
* Substitute by 8 --- \( c^* + g = w^*(1-l^*) + d^*\)
* Substitute by 6 --- \( c^* + g = w^*n^* + d^*\)
* Substitute by 5 --- \( c^* + g = w^*n^* + zf(n^*, \overline{k}) - w^*n^* = zf(n^*, \overline{k}) \)
* Substitute by 4 --- \( c^* + g = y^*\) --- and we have 7

### Production Possibility Frontier (PPF)

From \( c^* + g = zf(1-l^*, \overline{k}) \), the PPF \( \mathcal{C}(l^*) = zf(1-l^*, \overline{k}) - g \)

It is decreasing: \( \mathcal{C}_l = -zf_n(1-l^*, \overline{k}) \leq 0 \) and the slope is the MPL.

It is convex: \( \mathcal{C}_{l,l} = zf_{n,n}(1-l^*, \overline{k}) \leq 0 \)

So where the wage \( -w \) is tangent to \( \mathcal{C} \) is the optimal solution to the firm problem in equilibrium.
We already knew the wege is tangent to the indifference curve at the solution to the household problem.
So equilibrium is there the indifference curve is tangent to the production possibility curve, and the slope at the point of tangency is the wage.
The marginal rate of transformation w.r.t.\ production, of leisure and consumption, i.e.\ if you work less you have to consume less, is \( MRT_{c^*, l^*} = zf_n(1-l^*, \overline{k}) \).
Then, \( MRS_{c^*, l^*} = \frac{U_l}{U_c} = w = zf_n = MRT_{c^*, l^*} \) is the condition of equilibrium.

We say \( \mathcal{C}(l = 1) = -g \) (no robots assumption).


### Comparative Statics on Equilibrium

* What happens when productivity \( z \)  goes up? Increase in prodctivity increases wage. So it is unclear whether leisure goes up or down. However, the total production will always go up. We need to know preferences to figure out change in leisure. But either way welfare must go up.

* Consumption goes up, with \( g\) constant, then \(y\) (output) goes up

* Government expenditure goes up, then taxes go up, and labor goes up because taxes are lump sum (do not affect the price of time) but households are poorer so they work more.
Crowding out effect of government expenditure: \( \Delta y = \Delta c + \Delta g \) but since total production increases the crowding out is partial. Consumption will fall but less than increase in government consumption, and output will go up.

    We know \( \Delta \mathcal{C}(l=0) = -\Delta g\), and \( \Delta \mathcal{C}(l = 0) = - \Delta g \) since \( zf(1, \overline{k}) \) will not change with \(g\).

    Note that unless households derive more utility directly from the government expenditure shock than they are losing due to the consummate decrease in \(c\) and \(l\), they will be worse off after the government expenditure shock.

This means that productivity is the best predictor of welfare, not government expenditure.
