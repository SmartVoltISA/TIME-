# Ω-TIME-056 — Capability preservation attack

**Status:** STRONG NEGATIVE RESULT / CONDITIONAL THEOREM / FUNDAMENTAL DERIVATION OPEN

## 1. Question

Ω-TIME-055 replaced hidden scalar resource creation with a sharper object: the feasible capability set

`F_e(x) = {all admissible implementations of relation e from state x}`.

The conditional theorem was:

`F_e(x) ⊆ F_e(x')  ⇒  MC_e(x') ≤ MC_e(x)`.

The next question is whether this monotone inclusion can itself be derived from the existing Ω primitives.

Target:

`realization → preservation of old capability + addition of reusable capability`.

## 2. Minimal event model

Let a system state be

`x = (Q,S)`

where Q is the conserved allocation and S is structural organization.

A relation realization is a state transition

`x → x' = T_e(x)`.

Closure and conservation impose constraints such as

`Q_total(x') = Q_total(x)`.

They do not directly constrain the feasible implementation set F_e.

The key test is therefore whether every admissible T_e necessarily satisfies

`F_e(x) ⊆ F_e(x')`.

## 3. Neutral return control

Take a reversible or cyclic realization that returns the structural state to the same configuration:

`x' = x`.

Then

`F_e(x') = F_e(x)`.

Capability is preserved, but nothing is added.

Therefore realization alone does not imply capability extension.

This is a strict neutral control: all original capabilities survive and the marginal cost is unchanged.

## 4. Destructive rearrangement control

Construct a closed system with two alternative routes for the same relation:

`F_e(x) = {γ₁, γ₂}`.

A realization can consume or lock the structural element supporting γ₁ while preserving total Q:

`F_e(x') = {γ₂}`.

Thus

`F_e(x') ⊂ F_e(x)`

is compatible with conservation and closure.

If γ₁ was cheaper than γ₂,

`MC_e(x') > MC_e(x)`.

Therefore conservation does not imply capability preservation.

## 5. Constructive extension control

A different admissible transformation may preserve both old routes and create a new route:

`F_e(x') = {γ₁, γ₂, γ₃}`.

Then

`F_e(x) ⊂ F_e(x')`.

The minimum resource requirement obeys

`MC_e(x') ≤ MC_e(x)`.

If

`R(γ₃) < min(R(γ₁),R(γ₂))`,

then

`MC_e(x') < MC_e(x)`.

This is genuine marginal learning, but the strict cheaper-route condition is additional.

## 6. Three-way structural fork

The same high-level primitives admit three branches:

### Branch A — neutral

`F' = F`

`MC' = MC`.

### Branch B — destructive

`F' ⊂ F`

`MC' ≥ MC`, with strict increase possible.

### Branch C — monotone extension

`F ⊂ F'`

`MC' ≤ MC`, with strict decrease possible.

Difference, relation, boundary, closure and conservation do not select among A/B/C.

## 7. Why boundary does not solve the problem

A boundary specifies what is internal and external to the selected whole. It can constrain admissible fluxes or transitions across the boundary.

But the same boundary can enclose:

- a preserved route;
- a consumed route;
- a newly constructed route;
- or a rearrangement that exchanges one route for another.

Therefore boundary determines admissibility of the whole but does not determine monotonicity of its capability set.

## 8. Why positivity does not solve it

Let every resource cost satisfy

`R(γ) > 0`.

Positivity prevents negative costs, but all three branches remain possible.

Thus

`positivity ≠ capability preservation`.

## 9. Why symmetry does not solve it

Symmetric interaction can guarantee reciprocal relations or balanced exchange under suitable conditions. It does not imply that a realized relation leaves all prior implementation paths available.

A symmetric system can undergo either:

`F → F`,

`F → F' ⊂ F`,

or

`F → F' ⊃ F`.

Hence symmetry does not fix the sign of capability change.

## 10. Capability inclusion as a distinct mathematical principle

The condition

`F_e(x) ⊆ F_e(T_e(x))`

is not a statement about quantity conservation. It is a statement about **order preservation in capability space**.

Define a partial order

`x ⪯_e y  iff  F_e(x) ⊆ F_e(y)`.

Then monotone capability extension is simply

`x ⪯_e T_e(x)`.

The missing fundamental law can therefore be restated as:

> **Does realization generate a monotone trajectory in capability space?**

Nothing in the current primitive package forces this order relation.

## 11. Stronger requirement: non-destructive composition

A possible route to derive monotonicity is to require that adding a realized relation composes with existing implementations without invalidating them.

For every old implementation γ,

`γ ∈ F_e(x)  ⇒  γ ∈ F_e(x')`.

This is equivalent to capability preservation.

But this requirement is itself a compositional axiom. It cannot be silently assumed as a consequence of closure.

## 12. Resource conservation attack on composition

Suppose an implementation γ requires resource allocation q_γ.

A new realization may use the same conserved pool Q and reserve some amount q_new.

If allocations are rival,

`q_γ + q_new ≤ Q`

may fail for some old γ.

Therefore conservation can create competition between capabilities rather than preserve them.

For monotone extension, the new structure must be non-rival with respect to the old implementation, or the system must possess compensating capacity.

Both are additional assumptions.

## 13. Non-rivality control

If the newly added structure can be used without consuming the resources required by every previously feasible implementation, then capability preservation becomes plausible.

Formally, if for every old γ there exists a realization γ' with equivalent old performance after the update, then old capability survives.

But the existence of such non-rival structure is not implied by conservation.

Thus:

`non-rival reusable capacity → capability preservation`

is conditional, not fundamental.

## 14. Strict learning requires more than monotonicity

Even if

`F ⊆ F'`,

we only know

`MC' ≤ MC`.

Strict learning requires

`min_{γ∈F'}R(γ) < min_{γ∈F}R(γ)`.

Therefore the complete decomposition is:

`realization`

`→ capability preservation`

`→ capability extension`

`→ strictly cheaper new implementation`

`→ marginal cost reduction`.

Every arrow after the first requires a specific structural condition.

## 15. Negative control: same event label, opposite capability effect

The same relation type e can be embedded in different structural contexts.

Context 1:

`F={γ₁}` and realization adds γ₂ without removing γ₁.

Context 2:

`F={γ₁}` and realization replaces γ₁ by γ₂.

The event label, closure and conservation can be identical at the coarse level.

Yet:

`F₁' ⊃ F₁`

in the first case and

`F₂' ≈ F₂`

or even

`F₂' ⊂ F₂`

in the second.

Thus the coarse Ω primitives do not encode the missing compositional information.

## 16. Decision

**PASS — neutral control:** realization can preserve capability without extending it.

**PASS — destructive control:** conservation and closure permit loss of capability.

**PASS — constructive control:** capability extension yields non-increasing marginal cost conditionally.

**FAIL — fundamental derivation:** the current Ω primitives do not force capability preservation or extension.

**OPEN:** determine whether a deeper primitive below capability space can generate the order

`F_old ⊆ F_new`.

## 17. Updated frontier

`difference → relation → boundary → whole → closure → conservation → trace → persistence → capability set → capability order → ??? → monotone extension → marginal cost ↓ → reinforcement → polarity`

The unresolved object is now an **order law in capability space**, not merely a resource law.

> **A realized relation does not necessarily make the system richer in possibilities. It must first be shown that realization cannot destroy what was already possible.**
