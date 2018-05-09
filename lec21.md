---
header-includes: |
    \usepackage{pset}
    \usepackage[margin=1in]{geometry}
    \usepackage{mathrsfs}
    \usepackage{stmaryrd}
    \usepackage{mathpartir}
---

### I missed lecture today to go to Dimitris Tsementzis's talk on Finite Inverse Categories.

\[\begin{array}{c|c}
    \mathrm{fic} & \mathrm{context} \\
    \hline
    X & (X : \mathrm{Type}) \\
    X \to Y & (Y : \mathrm{Type}) (X : Y \to \mathrm{Type} ) \\
    I {\to}_{i} A {\rightrightarrows}_{c, d} O \mathrm{\ with\ } \mathcal{C}(I, O) = \curly{ci = di}
        & \paren{O : \mathrm{Type}} \paren{A : O \to O \to \mathrm{Type}} \) \( \paren{I : \prod\limits_{x : O} A(x,x) \to \mathrm{Type}} \\
    I {\to}_{i} A {\rightrightarrows}_{c, d} O \mathrm{\ with\ } \mathcal{C}(I, O) = \curly{ci \neq di}
        & \paren{O : \mathrm{Type}} \paren{A : O \to O \to \mathrm{Type}} \) \( \paren{I : \prod\limits_{x, y : O} A(x,y) \to \mathrm{Type}} \\
    I {\to}_{i} A {\rightrightarrows}_{c, d} O \mathrm{\ with\ } \mathcal{C}(I, O) = \curly{ci = di \neq e}
        & \paren{O : \mathrm{Type}} \paren{A : O \to O \to \mathrm{Type}} \) \( \paren{I : \prod\limits_{x : O} A(x,x) \to O \to \mathrm{Type}}
\end{array}\]

## Syntax: \( \mathbb{T}_{\mathrm{fic}} \)

\[
\inferrule{\ }{\bullet \vdash},
\inferrule{\Psi \vdash \Gamma}{\Psi, A : \Gamma \vdash},
\inferrule{\Psi \vdash }{\Psi \vdash \bullet},
\inferrule
    {\Psi, A : \Delta, \Psi' : L, \Psi, A : \Delta, \Psi' : \sigma : \Gamma \Rightarrow \Delta}
    {\Psi, A, \Psi' \vdash \Gamma, X : A \sigma},
\inferrule
    {\Psi \vdash \Gamma}
    {
        \Psi \vdash \eps_r : \Gamma \Rightarrow \bullet,
        \Psi \vdash \mathrm{id}_r : \Gamma \Rightarrow \Gamma,
        \mathrm{etc\ldots},
        \equiv
    }
\]

such that \( \mathrm{id}_r \circ \sigma \equiv \sigma \equiv \sigma \circ \mathrm{id}_r \), etc\ldots

## Theorem: There exists an interpretation of \( \mathbb{T}_{\mathrm{fic}} \) such that Soundness:
* \( \llbracket \Psi \vdash \rrbracket \Leftrightarrow \llbracket \Psi \rrbracket \) is a fic
* \( \llbracket \Psi \vdash \Gamma \rrbracket \Leftrightarrow \llbracket \Gamma \rrbracket : \llbracket \Psi \rrbracket \to \mathrm{Set} \subset {\mathrm{Shape}}_0\) (functor)
* \( \llbracket \Psi \vdash \sigma : \Gamma \Rightarrow \Delta \rrbracket \Leftrightarrow \llbracket \sigma \rrbracket : \llbracket \Gamma \rrbracket \Rightarrow \llbracket \Delta \rrbracket\) (natural transformation)

* Analogous to Lindenbaum-Tarski algebras
* Where was the train going?

## Theorem: Every [semantic] fic is derivable in this system: \( \forall \mathrm{fic\ } \mathcal{L}, \exists \Psi \vdash, \mathcal{L} \cong \llbracket \Psi \rrbracket \)

## Interpretation of \( \mathbb{T}_{\mathrm{fic}} \) in Coq
* \( I(X) = \mathrm{unit} : \mathrm{Type} \)
* \( I(\Psi, A : \Gamma) = \sum\limits_{X : I(\Psi)} I(\Psi, \Gamma)(X) \to \mathrm{Type} \)
* etc\ldots
* \( \mathrm{FIC} \simeq \Phi \big| \mathbb{T}_{\mathrm{fic}} \vDash \Phi = \mathrm{Sig} \rightarrow_I\) Coq, Agda, CHTT, HoTT, etc\ldots (but not Isabel)

Need

* \( \Sigma \) types
* non-dependent functors
* non-dependent types
* unit types
* associative constructors?

### The metamathematics of mathematics formalized by type theory is the mathematics of fics

So, you can do type theory in any programming language!
You can even actually store structured data like JSON files as elements, with a hierarchy naturally provided by nestedness.
Elements of fics are dags, etc\ldots
