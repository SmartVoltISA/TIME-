# Ω-TIME-047 — Competition: does mutual exclusion derive the sign of feedback?

**Status:** STRUCTURAL PASS / SIGN DERIVATION OPEN / FUNDAMENTAL DERIVATION OPEN

## Question

Can the chain

`difference → alternatives → mutual exclusion/competition`

by itself derive the positive feedback required for spontaneous polarity, or does competition require an additional constitutive law?

## Minimal controls

Consider two nonnegative alternatives with normalized total resource

`x1 + x2 = 1`.

### Control A — symmetric exchange

`dx1/dt = g(x2-x1)`
`dx2/dt = g(x1-x2)`

For `d=x1-x2`:

`dd/dt = -2gd`.

The difference decays and the symmetric state `x1=x2` is selected.

**Result:** competition-like coupling does not automatically imply amplification.

### Control B — replicative competition

Use the normalized growth law

`dx_i/dt = x_i(f_i - f̄)`

with `f_i=x_i`.

Then

`dx1/dt = x1(x1-f̄)`
`dx2/dt = x2(x2-f̄)`.

For unequal initial conditions, the larger component grows and the smaller declines. Numerical integration from `(0.51,0.49)` gives approximately `(0.999999,0.000001)` after the tested interval.

The symmetric state is unstable to an antisymmetric perturbation.

**Result:** mutual exclusion plus a multiplicative self-reinforcing fitness law produces polarity.

## Critical control

Replace the fitness law by a common value `f1=f2=c`.

Then

`dx_i/dt = x_i(c-c)=0`.

Normalization and mutual exclusion remain, but there is no amplification and no selection.

Therefore conservation/normalization + alternatives + competition are insufficient to derive the sign.

## Sign decomposition

The replicative model contains two distinct ingredients:

1. a competition/normalization constraint;
2. a constitutive ordering `f_i=x_i`, which makes the currently larger state receive the larger growth rate.

The second ingredient is precisely a positive-feedback assumption in another representation.

Thus the positive eigenvalue near the symmetric state is not obtained from mutual exclusion alone.

## Symmetry control

With exactly symmetric initial condition `(1/2,1/2)`, the deterministic system remains exactly symmetric. Polarity requires a perturbation, noise, or another symmetry-breaking condition.

For small perturbation `x1=1/2+ε`, `x2=1/2-ε`, the replicative law amplifies `ε`, whereas symmetric exchange suppresses it.

## Relation to known competition models

Winner-take-all models commonly obtain selection through explicit combinations of positive and negative feedback, lateral inhibition, or other constitutive interaction rules. This supports the distinction between the existence of competition and the particular feedback sign; it does not supply an Ω derivation of that sign.

## Decision

**PASS:** competition can convert an existing asymmetry into selection/polarity when an explicit reinforcing response is present.

**FAIL:** difference + alternatives + mutual exclusion/normalization alone does not force positive feedback.

**OPEN:** derive the reinforcing constitutive law from deeper Ω structure without inserting `f_i∝x_i`, a gain sign, an optimization objective, or an equivalent hidden premise.

## Updated frontier

`difference → relation → alternatives → boundary/mutual exclusion → ??? → feedback sign → polarity`

The unresolved node is now narrower: **what structural rule makes the response to an existing deviation reinforce that deviation?**

## Reproducibility notes

Numerical control uses deterministic Euler integration with fixed initial state and step. The qualitative conclusions are analytic and do not depend on the numerical endpoint.

No claim is made that the replicative model is fundamental physics. It is a positive control showing that polarity follows once the missing reinforcing constitutive rule is explicitly supplied.
