# Ω-TIME-036 — Reciprocity from a shared relation: is conservation forced by one boundary crossing?

## Status
**STRUCTURAL PASS / FUNDAMENTAL DERIVATION OPEN.**

## Question
Ω-TIME-035 reduced the resource problem to a quadratic valuation class under explicit composition and equivalence assumptions. The remaining bridge is reciprocity:

`relation/boundary → opposite balance signs → conservation`.

The test asks exactly what is forced by representing an interaction as one shared relation and what still has to be assumed.

## Check 1 — Incidence representation of one shared relation

For two nodes connected by one oriented relation, use incidence vector

`b = (-1,+1)ᵀ`.

Let `J` be one scalar transfer carried by that relation. The node balance is

`Δr = b J = (-J,+J)ᵀ`.

Therefore

`1ᵀΔr = 1ᵀb J = 0`.

### Result
**PASS.**

Once one relation carries one shared transfer variable, opposite balance signs and conservation of the summed quantity follow algebraically from incidence structure.

## Check 2 — General graph

For an oriented graph with incidence matrix `B` and edge-flow vector `j`,

`Δr = B j`.

Every column of `B` contains one `+1` and one `-1`, so

`1ᵀB=0`.

Hence

`1ᵀΔr=0`

for arbitrary edge flows `j`.

### Result
**PASS.**

Graph incidence gives a general structural conservation identity for the additive node quantity represented by `r`.

This is stronger than a two-node special case.

## Check 3 — Weighted conserved quantity

Let the conserved quantity be

`R = wᵀr`.

Then

`ΔR = wᵀB j`.

This vanishes for arbitrary `j` only when

`wᵀB=0`.

For a connected graph, this requires equal weights across each connected component (up to a component-wise constant).

### Result
**PASS with a condition.**

Incidence automatically conserves an unweighted additive total, but conservation of an arbitrary weighted resource requires a compatibility condition between the resource weights and the exchange structure.

This is important: reciprocity alone does not conserve every possible scalar valuation.

## Check 4 — Numerical random-graph control

Generate random connected graphs with arbitrary real edge flows. Construct `B` from oriented edges and compute

`Δr=Bj`.

The residual

`|Σ_i Δr_i|`

should remain at floating-point roundoff.

### Result
**PASS expected algebraically; numerical residual is implementation-level only.**

The identity is exact because every edge contributes `+J` at one endpoint and `-J` at the other.

## Check 5 — Negative control: two independent directed transfers

Replace one shared transfer by two independent processes:

`Δr₁=-J₁+J₂`.

Equivalently, allow independent transfer variables in opposite directions rather than one shared edge variable.

Then

`Δ(r₁+r₂)`

need not vanish unless a new condition is imposed, such as

`J₁=J₂`.

### Result
**FAIL for automatic conservation.**

A boundary relation does not force reciprocity if the model allows independent directed channels.

## Check 6 — Negative control: creation/destruction term

Extend the balance law to

`Δr = B j + s`.

Here `s` is a source/sink term.

Then

`1ᵀΔr = 1ᵀs`.

Unless

`1ᵀs=0`,

the total is not conserved.

### Result
**FAIL for automatic conservation.**

Conservation requires exclusion or balancing of net source/sink terms.

## Check 7 — Boundary crossing interpretation

A single shared relation can be represented as a boundary crossing carrying one transfer variable. The two sides see the same event with opposite incidence signs:

`side A: -J`

`side B: +J`.

This is not an additional numerical law; it is the algebraic meaning of one shared oriented edge.

### Result
**PASS as a structural mechanism.**

Reciprocity is derivable from the representation of interaction as one shared exchange relation.

## Check 8 — Does distinction alone force a shared edge variable?

No.

A distinction only establishes that two states/regions are different. It does not prohibit the model from assigning two independent processes across the distinction.

Therefore

`difference → shared J`

is not established.

### Result
**FAIL.**

The missing premise is not conservation itself but **shared-event/reciprocal coupling**.

## Check 9 — Interaction symmetry versus reciprocity

A symmetric coupling matrix

`S=Sᵀ`

is a different statement from conservation of node totals.

- symmetry concerns compatibility between channels;
- reciprocity concerns the same transfer appearing with opposite balance signs;
- conservation concerns an invariant sum/valuation.

These concepts can coincide but must not be silently identified.

### Result
**PASS for conceptual separation.**

## Check 10 — Link to Ω-TIME-031

If a positive metric `G>0` is present and the interaction operator satisfies

`GA=S`, `S=Sᵀ`,

then the two-channel coefficients have the same sign:

`a=s/g₁`, `b=s/g₂`,

so

`ab=s²/(g₁g₂)>0`.

Ω-TIME-036 shows a separate route to conservation: shared incidence `Bj` gives opposite node balances.

The two structures therefore answer different questions:

`shared edge → reciprocity/conservation`,

`positive metric + symmetric compatibility → ab>0`.

### Result
**PASS.**

The mechanisms are complementary rather than interchangeable.

## Check 11 — Can reciprocity survive coarse-graining?

Suppose several microscopic edges are grouped into one macroscopic relation. If coarse-grained flow is defined as the sum of constituent flows,

`J_macro = Σ_k J_k`,

then the boundary balance remains

`Δr_A=-J_macro`,
`Δr_B=+J_macro`.

Thus incidence conservation survives positive aggregation of internal exchanges.

### Result
**PASS under explicit aggregation rule.**

Coarse-graining preserves reciprocity when the coarse variable is defined from the same shared flows.

Without that aggregation rule, conservation cannot be assumed.

## Check 12 — Does reciprocity determine the amount of transfer?

No.

The relation fixes the balance pattern

`(-J,+J)`

but does not determine `J`.

`J` may depend on state difference, metric, constitutive law, memory, constraints, or another dynamical rule.

### Result
**FAIL for magnitude determination.**

Reciprocity determines accounting structure, not transfer magnitude.

## Synthesis
The strongest chain now becomes:

`comparison`
`→ difference`
`→ relation/boundary`
`→ shared interaction event`
`→ one exchange variable J`
`→ opposite incidence signs`
`→ conservation of the represented additive total`

in parallel with

`difference`
`→ scalarization principles`
`→ positive quadratic metric class`
`→ completeness`
`→ G>0`
`→ symmetric compatibility`
`→ ab>0`
`→ real ± characteristics.

These branches meet at a dynamical system in which the same relational structure supplies both exchange accounting and compatible two-channel propagation.

## Decision
**PASS:** one shared edge/transfer variable produces opposite balance signs.

**PASS:** graph incidence gives exact conservation of the represented unweighted additive total.

**PASS:** weighted conservation follows when the valuation weights are compatible with the incidence nullspace.

**PASS:** reciprocity survives coarse-graining when coarse flows are explicitly aggregated from shared microscopic flows.

**FAIL:** difference alone forces reciprocal exchange.

**FAIL:** a boundary alone forbids independent directed channels.

**FAIL:** reciprocity determines transfer magnitude.

**FAIL:** incidence conservation applies automatically to arbitrary weighted resources.

**FAIL:** conservation excludes source/sink terms without an additional closure condition.

**OPEN:** why fundamental interactions should be representable as shared events/edges rather than independent directed processes.

**OPEN:** why physical resource should belong to the conserved incidence nullspace.

**OPEN:** why source/sink terms should be absent or balanced at the fundamental level.

## Main result
A useful reduction has been achieved:

> **Reciprocity is not the same thing as conservation; it is a representation of one shared transfer event. Conservation follows when that event is encoded by incidence, while the resource being conserved must itself be compatible with the incidence structure.**

This removes another hidden identification from the Ω chain.

The remaining foundational question is now more precise:

`Ω-foundation → why interaction is a shared event`

rather than simply assuming reciprocity because two directions exist.

## Next decisive target
Attack the shared-event premise itself. Compare:

1. independent directed relations;
2. one shared reciprocal relation;
3. shared relation plus source/sink;
4. shared relation with memory-dependent constitutive law.

Determine which minimal assumptions are sufficient for a stable conserved positive resource and whether the shared-event representation emerges from boundary/closure rather than being inserted.

## Rule
FACT → CHECK → RESULT → DECISION → FIXATION.
PASS, FAIL and OPEN remain separate.
