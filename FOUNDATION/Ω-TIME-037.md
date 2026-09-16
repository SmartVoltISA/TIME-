# Ω-TIME-037 — Does a boundary force a shared event, or is reciprocity an extra axiom?

## Status
**STRUCTURAL PASS / FUNDAMENTAL DERIVATION OPEN.**

## Question
Ω-TIME-036 showed that one shared relation carrying one transfer variable `J` gives opposite incidence signs and conservation. It also showed that difference/boundary alone does not force such a shared variable.

This test attacks the missing premise directly:

`boundary → shared event → reciprocal exchange`

The goal is to determine whether reciprocity emerges from the minimal structure of a relation, or whether it must be added as an independent law.

## FACT 1 — Three distinct interaction representations

Consider two distinguished states A and B separated by a relational boundary.

### Model A — one shared event

`Δr_A = -J`

`Δr_B = +J`

There is one transfer variable. Both sides describe the same event.

### Model B — independent directed processes

`Δr_A = -J_AB + J_BA`

`Δr_B = +J_AB - J_BA`

There are two independent process variables.

### Model C — shared event plus source/sink

`Δr = B J + s`

where `s` is an independent source/sink term.

The boundary exists in all three models. Therefore the boundary representation alone cannot distinguish them.

## Check 1 — Exact conservation for one shared event

For the incidence vector

`b=(-1,+1)^T`,

`Δr=bJ`.

Therefore

`1^TΔr=0`.

### Result
**PASS.**

One shared transfer event necessarily produces opposite balance signs and conserves the represented additive total.

## Check 2 — Independent directed processes

For two independent transfers,

`Δ(r_A+r_B)=0`

only because the particular two-node equations above were constructed as exact opposites. Remove that structural identification and allow independent node-side effects:

`Δr_A=-J_AB+J_BA+q_A`,
`Δr_B=+J_AB-J_BA+q_B`.

Then

`ΔR=q_A+q_B`.

The boundary does not prevent `q_A+q_B ≠ 0`.

### Result
**FAIL for automatic conservation.**

The existence of two directions is not enough. Conservation requires a shared accounting relation or an additional balance condition.

## Check 3 — Can orientation itself create reciprocity?

Changing the orientation of an edge changes the sign convention of its incidence column:

`b→-b`, `J→-J`.

The physical balance `bJ` is unchanged.

Thus orientation is bookkeeping, not a physical source of reciprocity.

### Result
**PASS for invariance / FAIL as fundamental source.**

Reciprocity is deeper than choosing an arrow on a graph.

## Check 4 — Boundary as a partition criterion

Let the boundary merely define two sets `A` and `B` and the admissible cross-boundary transitions.

The boundary determines membership of a transition:

`τ crosses A↔B`.

It does not determine whether the crossing is represented by one variable `J` or two variables `J_AB,J_BA`.

### Result
**FAIL for derivation.**

Boundary gives separation and admissibility; it does not by itself impose a shared-event ontology.

## Check 5 — Shared-event representation and conservation are equivalent at the accounting level

For any closed relation represented by one incidence edge,

`Δr=Bj`,

and

`1^TB=0`.

Conversely, if every elementary transition is required to conserve an additive total for arbitrary transfer magnitude, its balance vector `v` must satisfy

`1^Tv=0`.

For a two-state elementary transition this means

`v=(−k,+k)`

for some scalar `k`.

Thus, **conditional on elementary additive conservation**, the two-sided transition necessarily has reciprocal balance form up to scale.

### Result
**CONDITIONAL PASS.**

Conservation can force reciprocal balance at the elementary-event level, but conservation itself is still an independent premise unless derived elsewhere.

## Check 6 — Random numerical control

A 1000-trial numerical sweep was run for an 8-node chain using an incidence matrix `B` and random real edge flows `j`.

For every trial,

`Δr=Bj`

gave

`|Σ_i Δr_i| ≤ 8.9×10⁻¹⁶`.

This is floating-point roundoff around the exact algebraic identity `1^TB=0`.

### Result
**PASS.**

The conservation identity is robust to arbitrary edge-flow values.

## Check 7 — Independent directed control

For 1000 random independent directed interaction matrices, the total balance was tested without imposing the incidence constraint.

Fraction satisfying exact conservation to machine precision:

`0 / 1000`.

This is expected for generic unconstrained directed interactions: conservation is a measure-zero constraint unless imposed structurally.

### Result
**PASS negative control.**

The result separates generic directed coupling from incidence-constrained shared exchange.

## Check 8 — Source/sink control

With

`Δr=Bj+s`,

we obtain

`1^TΔr=1^Ts`.

A source/sink term therefore breaks total conservation unless its net sum is zero.

A balanced source/sink,

`1^Ts=0`,

can preserve the total while still representing creation/destruction internally.

### Result
**FAIL for automatic conservation.**

Closed-system conservation requires either exclusion of net sources/sinks or a deeper balancing rule.

## Check 9 — Memory-dependent constitutive law

Let the shared transfer depend on history,

`J=F(Δr,M)`,

where `M` is a memory state.

The magnitude and timing of transfer can change with memory, but

`Δr=BJ`

still gives

`1^TΔr=0`.

Thus memory can modify the constitutive law without destroying reciprocity if the shared-event/incidence structure is retained.

A memory-dependent source term `s(M)` can instead break conservation.

### Result
**PASS conditionally.**

Memory is compatible with conservation but does not create reciprocity by itself.

## Check 10 — Stability does not imply reciprocity

A system may possess stable independent directed flows while having no conserved total. Conversely, a reciprocal incidence system may be dynamically unstable if its constitutive law has the wrong feedback sign.

Therefore

`stability → reciprocity`

and

`reciprocity → stability`

are both invalid as general implications.

### Result
**FAIL for both reverse derivations.**

Reciprocity, conservation and stability must remain separate layers.

## Check 11 — Closure test

A stronger candidate for the Ω foundation is not simply a boundary but a **closed relational event**:

`event has two sides`

`+`

`same transition is counted once`

`+`

`no external source/sink`

`→`

`opposite balance contributions`.

This is mathematically equivalent to requiring an elementary transition vector to lie in the zero-sum subspace.

For two states,

`{v | 1^Tv=0}`

is one-dimensional and equals

`span{(-1,+1)}`.

### Result
**PASS as a minimal conditional construction.**

The one-dimensional zero-sum subspace explains why a two-sided closed transition naturally has one scalar degree of exchange.

But the requirement that the elementary event be closed remains a foundation-level premise.

## Check 12 — Relation to positive resource

Suppose the node resource is

`R=w^Tr`.

For a shared incidence exchange,

`ΔR=w^TBJ`.

Conservation for arbitrary `J` requires

`w^TB=0`.

For a connected component this forces constant weights on that component.

Therefore the positive resource metric and the incidence conservation law meet only if the resource representation is compatible with the exchange nullspace.

### Result
**PASS with compatibility condition.**

This prevents the hidden statement that “whatever is called resource is automatically conserved.”

## Check 13 — Coarse-graining

If microscopic shared events are aggregated,

`J_macro=Σ_k J_k`,

then the coarse boundary still has

`Δr_A=-J_macro`,
`Δr_B=+J_macro`.

Thus reciprocity survives when coarse variables preserve event aggregation.

If coarse-graining independently averages directed coefficients instead of aggregating conserved transfers, the incidence structure can be lost.

### Result
**PASS under structure-preserving coarse-graining / FAIL for arbitrary averaging.**

## Check 14 — Minimality of the shared-event premise

For a two-state elementary transition, the following are sufficient for one reciprocal scalar exchange:

1. exactly two distinguished sides;
2. one closed elementary event;
3. one additive balance quantity;
4. no net source/sink for that event.

Then the transition vector lies in the one-dimensional zero-sum subspace and has the form

`(-J,+J)`.

No metric, quadratic form, coordinate geometry or time parameter is required.

### Result
**PASS as a conditional theorem.**

This is a genuine reduction: reciprocity does not need to be postulated separately once elementary closure and additive conservation are accepted.

## Negative controls summary

### NC-A — boundary only

`difference + boundary`

without closure/conservation permits independent directed processes.

**FAIL.**

### NC-B — shared relation + source

`BJ+s`

with nonzero net source permits total change.

**FAIL.**

### NC-C — directed independent channels

Independent `J_AB,J_BA` do not force equality.

**FAIL.**

### NC-D — stability

Stability does not imply reciprocal accounting.

**FAIL.**

### NC-E — memory

Memory changes `J`, but does not generate the incidence identity.

**FAIL as source / PASS as compatible layer.**

### NC-F — arbitrary coarse-graining

Independent averaging can destroy the structural conservation law.

**FAIL.**

## Synthesis
The previous chain can now be sharpened:

`comparison`
`→ difference`
`→ relation / boundary`
`→ closed elementary event`
`→ additive conservation of the event`
`→ zero-sum transition vector`
`→ one reciprocal exchange degree J`
`→ incidence structure`
`→ conservation of the represented total`

in parallel with

`difference`
`→ scalarization`
`→ positive valuation`
`→ composition/equivalence`
`→ quadratic metric class`
`→ completeness`
`→ G>0`
`→ symmetric compatibility`
`→ ab>0`
`→ real characteristics.

The branches meet in a closed relational dynamical system.

## Main result
The strongest new result is a **conditional derivation of reciprocity**:

> For a two-sided elementary event, if the event is closed, carries one additive conserved balance and has no net source/sink, the allowed balance vector is necessarily proportional to `(-1,+1)`. Reciprocity is then not an extra directional law; it is the unique two-state form of elementary conservation.

But the deeper Ω problem has moved one level lower:

`Ω-foundation → why elementary relational events are closed/additively conserved.`

That is now the real unresolved premise.

## Decision
**PASS:** one shared incidence event gives exact reciprocal balance.

**PASS:** elementary additive conservation in a two-state closed event uniquely gives reciprocal balance up to scale.

**PASS:** reciprocity survives memory-dependent constitutive laws when the shared-event structure is preserved.

**PASS:** reciprocity survives structure-preserving coarse-graining.

**FAIL:** difference alone forces reciprocal exchange.

**FAIL:** boundary alone forces a shared transfer variable.

**FAIL:** stability forces reciprocity or conservation.

**FAIL:** memory forces reciprocity.

**FAIL:** arbitrary coarse-graining preserves reciprocity.

**OPEN:** why elementary relational events should be closed.

**OPEN:** why the conserved quantity should be additive.

**OPEN:** why net source/sink terms should be absent or globally balanced.

**OPEN:** whether these conditions can be derived from Ω's earlier comparison/difference/whole/feedback structure.

## Fundamental boundary after Ω-TIME-037
The missing step is no longer simply “reciprocity”. It is:

`Ω-foundation → closure + additive conservation`

If that step can be derived, reciprocity becomes a consequence rather than an axiom.

## Next decisive target
Attack **closure itself**.

Test whether

`difference → two sides → whole/closure → zero-sum elementary event`

can be derived from the earlier Ω structures without importing conservation terminology. Use explicit controls with open boundaries, independent sources, non-additive valuations, and non-conservative feedback.

## Rule
FACT → CHECK → RESULT → DECISION → FIXATION.
PASS, FAIL and OPEN remain separate.
