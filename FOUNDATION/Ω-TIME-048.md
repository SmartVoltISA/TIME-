# Ω-TIME-048 — Can conservation + positivity + symmetry force the sign of feedback?

**Status:** STRUCTURAL NEGATIVE RESULT / SIGN DERIVATION OPEN / FUNDAMENTAL DERIVATION OPEN

## 1. Question

After Ω-TIME-047 the remaining hole is:

`difference → relation → alternatives → boundary/mutual exclusion → ??? → feedback sign → polarity`

The direct attack is to add the strongest constraints already obtained:

- two alternatives;
- additive conservation `x₁+x₂=1`;
- nonnegative state `xᵢ≥0`;
- exchange symmetry `1↔2`;
- locality/state-only response;
- smooth bounded dynamics;
- no external source/sink.

Question: **do these constraints force the symmetric state to be unstable and therefore force positive feedback?**

## 2. General reduction

Let

`d = x₁ - x₂`,  `x₁=(1+d)/2`,  `x₂=(1-d)/2`,  `d∈[-1,1]`.

Exact conservation gives

`ẋ₂ = -ẋ₁`.

Exchange symmetry requires the difference dynamics to be odd:

`ḋ = F(d)`,  `F(-d)=-F(d)`.

Positivity can be preserved by making the boundary states `d=±1` invariant, i.e. `F(±1)=0`.

A broad admissible family is therefore

`F(d)=k d (1-d²)(1+a d²)` with `a≥0`.

Every member is:

- smooth;
- odd under exchange;
- exactly conservative;
- bounded on `[-1,1]`;
- boundary-preserving;
- local/state-only;
- compatible with the same two-alternative structure.

But the linearization at the symmetric state is

`F'(0)=k`.

Therefore the sign of `k` alone determines the feedback sign.

## 3. Positive-feedback branch

For `k>0`:

`ḋ≈k d` near `d=0`.

A small asymmetry grows. The symmetric state is unstable and the boundary polarities `d=±1` are attracting for the tested family.

Example numerical integration, `d₀=±10⁻³`, `k=1`, `a=0`, `dt=10⁻³`, `T=20`:

- `d₀=+10⁻³ → d≈+1.000000`;
- `d₀=-10⁻³ → d≈-1.000000`.

This is polarity/selection.

## 4. Negative-feedback branch

For `k<0`:

`ḋ≈k d` near `d=0`.

A small asymmetry decays and the symmetric state is restored.

Example, same numerical conditions with `k=-1`:

- `d₀=+10⁻³ → d≈+2.04×10⁻¹²`;
- `d₀=-10⁻³ → d≈-2.04×10⁻¹²`.

Thus the **same structural constraints** permit restoration or amplification.

## 5. Numerical structural sweep

For

`k∈{-2,-0.5,+0.5,+2}` and `a∈{0,1,5}`

we evaluated the vector field on 10,001 points across `d∈[-1,1]`.

Observed for every tested parameter pair:

- exact conservation residual `max|ẋ₁+ẋ₂| = 0` in floating-point evaluation;
- state interval remains bounded by the invariant endpoints;
- exchange symmetry is exact;
- the sign of the transverse linear mode is exactly the sign of `k`.

So neither positivity nor conservation nor symmetry removes the sign ambiguity.

## 6. Stronger control: multiplicative participation

A possible escape is to demand that each state's change be proportional to its current amount:

`ẋᵢ = xᵢ(rᵢ-r̄)`.

This is the standard route to replicator dynamics; normalizing absolute growth rates produces the familiar replicator form. The derivation is well established in evolutionary dynamics. citeturn0search1turn0search4

But proportional participation still does not determine the sign of selection. The sign enters through the constitutive difference `r₁-r₂`.

If `r₁-r₂ = c(x₁-x₂)`, then:

`ḋ = c(1-d²)d/2`.

- `c>0` gives reinforcement;
- `c<0` gives restoration;
- `c=0` gives neutral dynamics.

Thus the replicator form moves the unexplained quantity from the overall conservation law into the **response/fitness law**. It does not close the Ω hole by itself.

## 7. Important separation

We now have four distinct ingredients:

1. **Conservation** — fixes the allowed direction of motion in state space.
2. **Positivity** — restricts the admissible state domain.
3. **Symmetry** — requires opposite behavior under exchange.
4. **Feedback sign** — determines whether a deviation grows or decays.

The first three do **not** mathematically determine the fourth.

Equivalently, conservation supplies a tangent space, but not an orientation of the flow inside that tangent space.

## 8. Negative control against hidden assumptions

The two systems

`ḋ = +d(1-d²)`

and

`ḋ = -d(1-d²)`

have the same:

- variables;
- conservation law;
- state domain;
- exchange symmetry;
- locality;
- smoothness;
- boundary invariance;
- absence of external source/sink.

They differ only in the sign of the response.

Therefore **no proof using only those premises can derive positive feedback**. Any such proof would have silently inserted an additional premise equivalent to `F'(0)>0`.

## 9. What would actually close the hole?

A genuine derivation must explain why a deviation changes the future transition rate in the same direction:

`d > 0  ⇒  response favors further d > 0`.

Possible candidate mechanisms must be attacked separately rather than assumed:

- self-reinforcing resource access;
- memory-dependent accessibility;
- multiplicative participation;
- geometric/structural advantage of an already occupied relation;
- path shortening / reduced transition cost;
- accumulation of successful transitions;
- instability generated by a deeper variational or conservation principle.

The critical requirement is that the mechanism must derive the **sign** rather than rename it.

## 10. Connection with known dynamics

Standard replicator dynamics indeed amplifies a type when its fitness exceeds the mean, but that statement already contains the constitutive ordering rule. citeturn0search3turn0search25

Likewise, symmetry-breaking models show that positive linear feedback can destabilize the symmetric branch and produce paired states, but the feedback coefficient/sign remains part of the dynamical model. citeturn0search0turn0search7

These are controls and literature anchors, not evidence that Ω has derived the sign.

## 11. Decision

**PASS:** conservation + positivity + exchange symmetry define a strong admissible structural class.

**FAIL:** these constraints do not force positive feedback.

**FAIL:** replicator normalization alone does not close the sign problem.

**OPEN:** derive the constitutive response sign from a deeper Ω principle without importing an equivalent positive-feedback assumption.

## 12. Updated frontier

`difference → relation → alternatives → boundary/mutual exclusion → closure/conservation → admissible state space → ??? → response sign → positive feedback → polarity`

The hole has therefore become smaller and more precise:

> **What structural fact makes an already-used/occupied relation more likely to be used again, rather than merely conserving or restoring the previous state?**

That is the next target.
