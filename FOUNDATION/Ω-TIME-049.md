# Ω-TIME-049 — Can transition-cost change derive the sign of feedback?

**Status:** STRUCTURAL NEGATIVE RESULT / COST-SIGN OPEN / FUNDAMENTAL DERIVATION OPEN

## 1. Question

After Ω-TIME-048 the remaining hole was narrowed to the effect of a state change on the accessibility/cost of future transitions.

Target:

`event → state change → future transition cost → response sign → feedback → polarity`

Question: **can the sign of the feedback be derived if transition rates are determined by a state-dependent cost, without inserting the sign into the constitutive law?**

## 2. Minimal two-alternative model

Let

`x₁+x₂=1`, `d=x₁-x₂`, `d∈[-1,1]`.

Let `r₁(d), r₂(d) ≥ 0` be transition rates into the two alternatives. The conservative dynamics is

`ẋ₁ = x₂ r₁ - x₁ r₂`,

`ẋ₂ = -ẋ₁`.

Therefore

`ḋ = (1-d)/2 · r₁(d) - (1+d)/2 · r₂(d)`.

Exchange symmetry requires

`r₂(d)=r₁(-d)`.

No sign of the transverse mode is fixed by this symmetry alone.

## 3. Cost-to-rate mapping

Introduce transition costs `C₁(d), C₂(d)` and a standard monotone rate mapping

`rᵢ(d)=r₀ exp[-Cᵢ(d)]`, `r₀>0`.

Symmetry requires

`C₂(d)=C₁(-d)`.

Consider the symmetric local family

`C₁(d)=C₀-a d`,

`C₂(d)=C₀+a d`.

Then

`r₁=r₀e^{a d}e^{-C₀}`,

`r₂=r₀e^{-a d}e^{-C₀}`.

Linearizing at `d=0` gives

`ḋ = r₀e^{-C₀}(a-1)d + O(d²)`.

Thus there is a threshold:

- `a>1` → amplification;
- `a<1` → restoration;
- `a=1` → neutral linear mode.

The occupancy factor itself contributes a restoring term. A sufficiently strong cost reduction can overcome it, but the required magnitude/sign is not derived by symmetry or conservation.

## 4. Direct numerical control

For `r₀e^{-C₀}=1` and small `d=10⁻⁶`:

- `a=-2` gives `ḋ/d ≈ -3`;
- `a=-1` gives `ḋ/d ≈ -2`;
- `a=+1` gives `ḋ/d ≈ 0`;
- `a=+2` gives `ḋ/d ≈ +1`.

The same state domain, conservation, positivity, exchange symmetry and monotone cost-to-rate mapping therefore support both restoration and amplification.

## 5. Stronger candidate: cost generated from relational resource

A natural Ω-compatible positive quantity is

`U(d)=1/2 d²`.

Its gradient is

`U'(d)=d`.

If transition cost follows the positive resource gradient, the induced response is restorative: moving farther from the symmetric state costs more.

This reproduces the earlier Ω-TIME-045 result: positive quadratic resource plus ordinary descent does not create positive feedback.

To obtain amplification, the effective cost must instead decrease along the already selected direction, requiring a local concavity/complementarity mechanism or an equivalent constitutive assumption.

Therefore **positive resource does not imply decreasing future cost**.

## 6. Complementarity control

Suppose the cost contains an occupancy-dependent term

`C₁=C₀-a x₁`, `C₂=C₀-a x₂`.

Increasing occupancy then reduces the cost of repeating the same transition. This produces reinforcement for sufficiently large `a`.

But the opposite law

`C₁=C₀+a x₁`, `C₂=C₀+a x₂`

is equally compatible with positivity and exchange symmetry and produces restoration.

Therefore the missing ingredient is not merely state-dependent cost; it is the **sign of the state-to-cost derivative**:

`∂C_same/∂x_same < 0` for reinforcement,

versus

`∂C_same/∂x_same > 0` for restoration.

That derivative is exactly the old feedback-sign problem expressed geometrically.

## 7. Important result

We have now separated three layers:

1. **State constraint:** which states are admissible.
2. **Transition cost:** how difficult an admissible transition is.
3. **Cost response:** how an event changes the cost of repeating/avoiding a relation.

Ω-TIME-034 already showed that accessibility does not automatically scalarize into a capacity/cost. Ω-TIME-048 showed that conservation/positivity/symmetry do not select the feedback sign.

Ω-TIME-049 shows that even after introducing a monotone cost-to-rate mapping, the sign is still located in the constitutive derivative `∂C/∂x`.

## 8. Negative theorem within the tested class

Let a two-state model satisfy:

- additive conservation;
- nonnegative states;
- exchange symmetry;
- local smooth transition rates;
- rates monotone decreasing with their own transition cost;
- symmetric cost functions.

Then these assumptions do **not** determine whether the symmetric state is stable or unstable.

Proof by construction: the two symmetric families

`C₁=C₀-a d`, `C₂=C₀+a d`

with `a>1`, and

`C₁=C₀+a d`, `C₂=C₀-a d`

with the same magnitude `a>1`, satisfy the same structural assumptions but give opposite signs of the transverse mode.

Therefore a derivation of positive feedback must supply an additional principle that fixes the sign of the state-to-cost response.

## 9. New frontier

The hole is now localized even more sharply:

`difference → relation → event → state change → transition geometry/cost → ??? → sign(∂C/∂state) → feedback`

The next attack is therefore not “find another feedback law”. It is:

> **Can the direction of change of transition cost be derived from boundary/closure and the geometry of admissible states?**

Candidate routes:

- path shortening caused by completed relation;
- removal of constraints after a successful transition;
- geometric contraction of the admissible transition region;
- compositional closure making repetition cheaper;
- variational principle where successful continuation reduces action/cost;
- resource redistribution that necessarily lowers the marginal cost of the same relation.

Each must survive the opposite-sign control.

## 10. Decision

**PASS:** state-dependent transition cost provides a precise representation of accessibility.

**PASS:** monotone cost-to-rate mapping can convert cost changes into feedback.

**FAIL:** state dependence, conservation, positivity, symmetry and monotone rate mapping do not determine the sign.

**FAIL:** positive relational resource with ordinary gradient descent gives restoration rather than amplification.

**OPEN:** derive the sign of the marginal transition-cost change from deeper Ω structure.

## 11. Updated chain

`difference → relation → alternatives → boundary → closure → conservation → admissible state space → transition cost → marginal cost response → feedback sign → polarity`

The remaining hole is now concentrated in one quantity:

`sign(∂C_same / ∂x_same)`.

If Ω can derive that sign without inserting an equivalent assumption, the positive-feedback gap is closed. Otherwise the gap is a genuine additional constitutive law.
