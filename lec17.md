---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
---

## Fiscal Policy

Ricardian Neutrality of Fiscal Policy by David Ricard with later work by Antonio de Viti de Marco and Robert Barro:
Government debt has to be repaid with taxes at some point in the future

### Ricardian Proposition

Given government expenditures \( \curly{g_t}_{t=0}^{\infty}\), it is irrelevant for households whether those expenditures are figured by current taxes on current debt and future taxes: the path of taxes does not matter.

This "neutrality" or "equivalence" holds under very strict assumptions.

### Two-Period Endowment Economy

Given times \( t \in \mathcal{T} = \curly{1, 2} \), interest rate \(r\), and government expenditures \( \curly{g_t}_{t \in \mathcal{T}} \).

Assume taxes are lump-sum in period 1 or period 2. Then consider \( \forall t \in \mathcal{T}, \tau_t = g_t \) using taxes to finance expenditures in every period.
Then the government budget constraint is \( g_1 + \frac{g_2}{1+r} = \tau_1 + \frac{\tau_2}{1+r} \).
Then given optimal consumption choices \( \curly{c^*_t}_{t \in \mathcal{T}} \) such that \( c_1^* + a = y_1 - \tau_1 \) and \( c_2^* = (1+r)a+y_2 - \tau_2 \) we have the budget constraint \( c_1 + \frac{c_2}{1+r} = y_1 + \frac{y_2}{1+r} - \paren{\tau_1 + \frac{\tau_2}{1+r}} = y_1 + \frac{y_2}{1+r} - \paren{g_1 + \frac{g_2}{1+r}} \).

Similarly, when \( g_1 = \hat{b} + \hat{\tau}_1 \) and \( g_2 + (1+r) \hat{b} = \hat{\tau}_2 \) note the government budget constraint is \( g_1 + \frac{g_2}{1+r} = \hat{\tau}_1 + \frac{\hat{\tau}_2}{1+r} \) as before.
Still, \( c_1 + \frac{c_2}{1+r} = y_1 + \frac{y_2}{1+r} - \paren{\tau_1 + \frac{\tau_2}{1+r}} = y_1 + \frac{y_2}{1+r} - \paren{g_1 - \hat{b} + \frac{g_2 + (1+r) \hat{b}}{1+r}} = y_1 + \frac{y_2}{1+r} - \paren{g_1 + \frac{g_2}{1+r}} \).

All we must show is \( \forall t \in \mathcal{T}, c_t^* = \hat{c}_t \).
Note from the Euler equation \( u(c_2) = \beta u((1+r)c_1) \) so for most sane \( u \) we can substitute for \( c_2 \).

### Assumptions

1. We assume the debt is repaid within the lifetime of the individual.
2. Only holds for lump-sum taxes because they are non-distortionary.
3. No Redistribution from Fiscal Policy
4. No Credit Constraints on Households

## Social Security

