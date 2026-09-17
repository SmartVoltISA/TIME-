# Ω-TIME-062 — Locality attack on capability preservation

**Status:** STRONG NEGATIVE RESULT / CONDITIONAL THEOREM / LOCALITY INSUFFICIENT

## 1. Question

Ω-TIME-061 showed that independence is not derived from dimensionality, boundary, conservation, positivity or symmetry.

The next candidate is locality:

> If new realization acts only locally, must sufficiently distant old capabilities remain unchanged?

Target:

`support(T_r) ∩ support(F_old) = ∅`

or, more generally,

`F_old ⊆ F_new`.

## 2. Strictly disjoint local support

If an update acts on a component A and an old capability e is supported entirely on a disconnected component B, then the update cannot alter e under a strictly factorized dynamics.

This gives a valid conditional theorem:

`disjoint support + no-mediated constraint`

`⇒ preservation of e`.

## 3. Locality does not imply disjointness

Take a chain

`A-B-C`.

An update at A is local, but B couples A to C.

A local change can therefore propagate through successive local interactions and alter a capability at C.

Thus:

`local update ≠ isolated update`.

## 4. Finite propagation control

Suppose influence travels at finite speed v.

Then an event at A cannot affect C before a finite propagation time

`τ ≥ d(A,C)/v`.

This constrains the time of influence, not its eventual existence.

Therefore finite propagation gives a causal delay but does not by itself guarantee capability preservation.

## 5. Screening control

If interactions decay or are screened beyond a scale ξ, influence can become small:

`|δC| ~ exp(-d/ξ)`.

But nonzero influence still permits capability modification in principle.

Approximate independence is not exact non-rivality.

## 6. Zero-coupling control

If the coupling across a cut is exactly zero,

`H = H_A ⊕ H_B`,

then A and B are dynamically independent under the specified model.

This works, but zero cross-coupling is an explicit structural condition.

It is not implied by merely having a boundary between the selected whole and environment.

## 7. Graph-cut attack

Let G contain a cut separating A and B.

If there is at least one active cross-edge, local changes can transmit influence across the cut.

If all cross-edges vanish, the graph decomposes.

Therefore the relevant invariant is not “there is a boundary”, but “the boundary is dynamically impermeable for the considered channel”.

That is an additional property.

## 8. Conservation attack

A globally conserved quantity can be transported through local edges.

Locality therefore does not prevent redistribution.

A local update can consume capacity near A while compensating elsewhere through a chain of local exchanges.

Hence:

`locality + conservation ≠ local non-rivality`.

## 9. Symmetry attack

A translation-symmetric local system can still possess collective modes spanning the entire system.

Symmetry therefore does not imply localization of capability.

Conversely, a localized defect can break a capability globally if the relevant path is structurally essential.

## 10. Conditional locality theorem

Let G be partitioned into A and B with no active transition edge from A to B or B to A for the relevant operation class.

Then

`Reach_A` and `Reach_B`

are independent under that operation class.

An update supported in A preserves every B-only capability.

This is a strong sufficient condition, but again it inserts impermeability.

## 11. Fundamental attack

The current Ω package can construct:

- local coupled systems;
- local screened systems;
- locally disconnected systems.

All can satisfy difference, relation, boundary, whole, closure, conservation and positivity.

Therefore locality itself does not select exact independence.

## 12. Important refinement

The missing principle has now become more precise:

`boundary`

is merely geometric/structural selection,

while

`impermeable boundary for a resource channel`

is a dynamical constraint.

The latter can protect old capability.

The former cannot.

## 13. Decision

**PASS — finite-speed control:** locality can delay influence without preventing it.

**PASS — graph-cut control:** exact capability separation requires vanishing relevant cross-coupling.

**PASS — conditional theorem:** impermeable dynamic cut preserves remote capabilities.

**FAIL — fundamental derivation:** locality alone does not force non-destructive capability preservation.

**OPEN:** whether impermeability/sector conservation can itself be derived from a deeper invariant.

## 14. Updated frontier

`difference → relation → boundary → whole → closure → conservation → composition → graph → reachability → redundancy → capacity rivalry → factorization → independence → locality → impermeability/sector conservation → ??? → protected capability → MC ↓ → reinforcement → polarity`

The next decisive cut is sector conservation:

> **Can a boundary-defined sector possess its own conserved quantity without introducing an additional conservation law?**
