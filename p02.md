---
title: Precept --- week 2
header-includes: |
    \usepackage[margin=0.5in]{geometry}
    \usepackage{mathrsfs}
---

 Total differential: \( df(x, y) = \frac{\partial f(x, y)}{\partial x} dx + \frac{\partial f(x, y)}{\partial y} dy \)

In part 1(a), derive an implicit equation of the form \( f(h, t, \tau) = 0 \).

Then explore how a change in \(t\) or \(\tau\) affects \(f\).
\( 0 = \frac{\partial f}{\partial h}dh + \frac{\partial f}{\partial t} dt + \frac{\partial f}{\partial \tau} d\tau\)

But WLOG we hold \(\tau\) constant and solve for \(\frac{dh}{dt} = \frac{-\frac{\partial f}{\partial t}}{\frac{\partial f}{\partial h}}\) and evaulate.
Can also use implicit function theorem.
