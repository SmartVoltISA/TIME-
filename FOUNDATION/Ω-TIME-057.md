# Ω-TIME-057 — Compositional capability attack

**Status:** STRONG NEGATIVE RESULT / CONDITIONAL THEOREM / NEW CANDIDATE OPEN

## 1. Question

Ω-TIME-056 isolated the unresolved condition as capability inclusion:

`F_old ⊆ F_new`.

The next attack asks whether ordinary composition of relations forces that inclusion.

Question:

> If a new relation is composed with an existing system, must every previously feasible implementation remain feasible?

The answer is tested with neutral, destructive and monotone composition controls.

## 2. Capability as reachable implementation

Let a system be represented by states and admissible transitions.

For a target relation e from state s, define

`F_e(s) = {admissible paths γ implementing e}`.

This is equivalent to viewing capability as a reachable-set object: monotone-system and reachability theory explicitly treats preservation of order/reachability as an additional structural property rather than an automatic consequence of having a transition system. citeturn0search0turn0search13

The Ω question is stronger: whether adding/composing a relation automatically preserves the old feasible paths.

## 3. Composition alone is insufficient

Let an old system contain two implementations of e:

`F_e(s) = {γ₁, γ₂}`.

Now compose a new relation r.

There are at least three admissible outcomes:

### Neutral composition

`F'_e(s) = {γ₁, γ₂}`.

No capability change.

### Destructive composition

`F'_e(s) = {γ₂}`.

The composition invalidates γ₁.

### Monotone composition

`F'_e(s) = {γ₁, γ₂, γ₃}`.

The old paths survive and a new path appears.

The operation "compose another relation" does not by itself choose among these cases.

## 4. Minimal graph counterexample

Take states `{A,B,C}`.

Before the new relation:

`E_old = {(A,B),(A,C)}`.

Both edges implement the same abstract relation e from A.

After a reconfiguration:

`E_new = {(A,C),(B,C)}`.

The total number of edges is unchanged. The state set is unchanged. The operation can be embedded in a closed system with conserved total structural budget.

But for relation e from A:

`F_old = {(A,B),(A,C)}`

while

`F_new = {(A,C)}`.

Therefore

`F_new ⊂ F_old`.

A composition/reconfiguration can preserve coarse quantities while destroying a capability.

This is a direct negative control against deriving capability monotonicity from composition alone.

## 5. Neutral composition control

If r acts on a disjoint component and leaves every old path untouched,

`F'_e = F_e`.

Composition has occurred, but no learning follows.

Thus composition does not even imply capability extension.

## 6. Constructive composition control

If r introduces a genuinely independent path γ₃ while retaining γ₁ and γ₂,

`F_e ⊂ F'_e`.

Then for a nonnegative implementation cost R,

`MC'_e = inf_{γ∈F'_e}R(γ) ≤ inf_{γ∈F_e}R(γ)=MC_e`.

This recovers the conditional theorem from Ω-TIME-055.

If additionally

`R(γ₃)<MC_e`,

then

`MC'_e<MC_e`.

Strict learning therefore requires a strictly cheaper compositional path.

## 7. Associativity is not monotonicity

A composition law may satisfy associativity:

`(A∘B)∘C = A∘(B∘C)`.

It may even be invariant to composition order in an abstract system algebra. Such composition-order invariance is a recognized structural property of system algebras. citeturn0search1

But associativity says how compositions are grouped; it does not say that composing a new component preserves every old implementation.

Therefore:

`associativity ≠ capability inclusion`.

## 8. Closure is not capability preservation

Closure says that the selected whole remains a valid system under the specified operation.

It does not say that the internal transition relation only grows.

A closed transformation may:

`add + remove`,

`replace`,

`re-route`,

or

`preserve + add`.

Hence:

`closure ≠ monotone extension`.

## 9. Conservation is not non-rival composition

Suppose old implementation γ requires resource allocation qγ and new relation r requires qr.

Conservation gives only

`Q_total = const`.

If qγ and qr are rival uses,

`qγ + qr ≤ Q_total`

may become restrictive.

Adding r can therefore make γ infeasible.

To guarantee preservation, the composition must have some form of non-rivality, compensation, or redundant capacity.

That is an additional constitutive property.

## 10. Composition with monotone order

The mathematical candidate can now be stated cleanly.

Define capability order:

`x ⪯_e y  iff  F_e(x) ⊆ F_e(y)`.

A transition operator T_r is capability-monotone if

`x ⪯_e y  ⇒  T_r(x) ⪯_e T_r(y)`.

But this property concerns preservation of an order under an operator. Standard monotone-systems theory likewise treats monotonicity as a special property of dynamics/update maps, not as a generic consequence of composition. citeturn0search0turn0search13

Thus even if we introduce the capability order, we still need a law making the realization operator order-preserving.

## 11. Stronger resource-theoretic correspondence

Abstract resource theories commonly use preorders and monotones: resource conversions define an order, and a monotone is a quantity that respects that order. Set inclusion is one standard route to constructing such monotones. citeturn0search3turn0search14

This independently supports the mathematical structure used here:

`capability inclusion → monotone quantity`.

But the existence of an order/monotone framework does not supply the physical law that makes Ω realizations move monotonically in that order.

That remains the unresolved step.

## 12. The decisive distinction: composability vs preservability

A relation can be composable without being preservative.

### Composability

A new operation can be connected to an existing system.

### Preservability

Every old implementation remains valid after the connection.

The second is strictly stronger.

Therefore:

`composition → connection`

but not necessarily

`composition → preservation`.

## 13. Candidate fundamental principle

The missing law can now be named:

> **Non-destructive compositionality:** realization of a new relation may add a compatible implementation without invalidating any previously feasible implementation.

Formal form:

`F_e(x) ⊆ F_e(T_r(x))`.

If this law holds, then marginal cost is non-increasing.

If a newly added implementation is strictly cheaper, marginal cost decreases.

## 14. Attack on derivation from Ω primitives

Current package:

`difference + relation + boundary + whole + closure + conservation + positivity + symmetry + trace + persistence + composition`

still permits:

`F' = F`,

`F' ⊂ F`,

and

`F' ⊃ F`.

Therefore the candidate law is **not derived** by the current package.

It must either:

1. be derived from a deeper primitive not yet isolated; or
2. be accepted as an independent constitutive principle; or
3. be rejected if a deeper negative theorem shows that no such universal law is possible.

## 15. Decision

**PASS — composition control:** composition can preserve, destroy, or extend capability.

**PASS — graph counterexample:** fixed coarse resource/budget does not prevent capability loss.

**PASS — conditional theorem:** non-destructive capability extension implies non-increasing marginal cost.

**FAIL — fundamental derivation:** composition, closure and conservation do not force capability preservation.

**OPEN:** identify a deeper invariant that makes composition non-destructive.

## 16. Updated frontier

`difference → relation → boundary → whole → closure → conservation → composition → capability set → capability order → non-destructive composition → ??? → marginal cost ↓ → reinforcement → polarity`

The key unresolved question is now:

> **What invariant, if any, prevents the realization of a new relation from destroying an old possibility?**

This is the next decisive cut.