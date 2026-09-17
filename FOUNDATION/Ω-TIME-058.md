# Ω-TIME-058 — Reachability invariant attack

**Status:** STRONG NEGATIVE RESULT / CONDITIONAL THEOREM / FUNDAMENTAL INVARIANT OPEN

## 1. Question

Ω-TIME-057 showed that composition does not itself preserve old capabilities. The missing object can be represented as reachability.

Let `Reach(x)` be the set of states reachable from state x under admissible operations.

Question:

> Does difference, relation, boundary, whole, closure, conservation, reciprocity, persistence and composition force reachability to be monotone after realization?

Target:

`Reach(x) ⊆ Reach(x')`.

## 2. Neutral control

If a realization changes only an internal label while leaving transition structure unchanged,

`Reach(x') = Reach(x)`.

All conservation and closure constraints can remain valid.

Thus realization need not expand reachability.

## 3. Destructive control

Take a transition graph with two routes:

`x → a → y`

and

`x → b → y`.

Suppose realization consumes or locks the edge through a while conserving total resource elsewhere.

Then the post-state can have only

`x → b → y`.

Therefore

`Reach(x') ⊂ Reach(x)`

is compatible with conservation and closure.

No algebraic contradiction appears.

## 4. Constructive control

If realization adds an edge without deleting existing edges,

`E ⊆ E'`,

then every old path remains available and

`Reach(x) ⊆ Reach(x')`.

This is a direct sufficient condition for reachability monotonicity.

But edge preservation is itself an extra condition.

## 5. Graph-theoretic decomposition

For a transition graph G=(V,E), define

`Reach_G(v)`.

A graph update `G→G'` satisfies reachability monotonicity if

`Reach_G(v) ⊆ Reach_G'(v)`

for the relevant v.

A sufficient condition is

`E ⊆ E'`.

A destructive update can instead have

`E' = E \ {e}`

for an essential edge e, causing reachability loss.

Therefore the sign of capability change is fundamentally a property of the update map on the transition graph.

## 6. Conservation attack

Let each edge carry a conserved allocation q_e with

`Σ_e q_e = Q_total`.

Moving allocation from e₁ to e₂ preserves Q_total but can remove e₁ from the feasible graph.

Thus:

`conservation → quantity invariant`

but not

`conservation → reachability invariant`.

A reachability invariant needs a separate non-rivality or redundancy condition.

## 7. Boundary attack

A fixed boundary can enclose either a graph whose edges are preserved or one in which an internal edge is consumed.

Boundary therefore defines the domain of the system but does not determine the direction of graph inclusion:

`E'⊇E`, `E'=E`, and `E'⊂E`

are all compatible with the same boundary.

## 8. Composition attack

Path composition gives

`(e₁∘e₂)∘e₃ = e₁∘(e₂∘e₃)`

where defined.

This ensures consistency of composing surviving transitions. It does not ensure that an update preserves all previous edges.

Therefore composition is downstream of reachability preservation, not its source.

## 9. Persistence attack

A persistent trace may remain forever while the corresponding transition is unavailable:

`trace(e)=1`,

but

`e∉E'`.

Hence

`memory of transition ≠ availability of transition`.

Persistence therefore cannot supply reachability monotonicity by itself.

## 10. Conditional reachability theorem

If an update satisfies

`E ⊆ E'`,

then every old path remains a path in G'. Therefore

`Reach_G(v) ⊆ Reach_G'(v)`.

Consequently, for any nonnegative path resource functional,

`MC'(e) ≤ MC(e)`

provided the resource cost of retained paths is unchanged.

This gives the chain:

`edge preservation → reachability preservation → capability inclusion → non-increasing marginal cost`.

## 11. Strict reinforcement

Strict decrease still requires a genuinely cheaper newly reachable path:

`∃γ_new∈Reach_G'(v) : R(γ_new)<MC_G(e)`.

Thus reachability monotonicity alone produces at most non-increase.

Strict reinforcement remains a second condition.

## 12. Fundamental attack

The existing Ω package can derive:

- distinctions;
- relations;
- selected boundaries/wholes;
- closure conditions;
- conserved totals under closed exchange;
- reciprocal balance under shared events;
- persistent traces;
- compositional path descriptions.

It cannot derive

`E ⊆ E'`

because conservation permits redistribution and redistribution can remove an essential edge.

Therefore reachability monotonicity is not yet fundamental.

## 13. Candidate invariant

The missing principle can now be stated as a graph invariant:

> **Non-destructive Reachability:** realization of a relation does not remove any previously reachable transition unless an explicitly stated resource conflict or boundary rule requires it.

Minimal mathematical form:

`Reach_G(v) ⊆ Reach_{G'}(v)`.

Stronger local form:

`E ⊆ E'`.

The local edge form is sufficient but may be stronger than necessary; reachability inclusion is the more general requirement.

## 14. Decision

**PASS — graph reformulation:** capability evolution can be reduced to reachability evolution.

**PASS — conditional theorem:** preserved transition structure guarantees non-decreasing reachability and therefore non-increasing optimal marginal cost.

**FAIL — fundamental derivation:** conservation, closure, composition, persistence and boundary do not force reachability preservation.

**OPEN:** find a deeper invariant that forbids destructive loss of reachability.

## 15. Updated frontier

`difference → relation → boundary → whole → closure → conservation → composition → graph → reachability → ??? → non-destructive reachability → MC ↓ → reinforcement → polarity`

The question is now extremely sharp:

> **Why should realization preserve the set of possibilities already reachable by the system?**

If no deeper invariant forces this, monotone capability and positive feedback must enter as an independent constitutive law.
