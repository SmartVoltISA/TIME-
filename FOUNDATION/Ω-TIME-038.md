# Ω-TIME-038 — Nested wholes: is closure relative to level, and can conservation emerge from that hierarchy?

**Status:** STRUCTURAL PASS / FUNDAMENTAL DERIVATION OPEN  
**Date:** 2026-09-17  
**Branch:** `main`

## 1. Question

Can closure be obtained without inserting conservation as a hidden premise, by treating a system as a **whole at a chosen level** and allowing exchange across nested boundaries?

Target distinction:

- **BOUNDARY** — separates inside from outside at a chosen level;
- **CLOSURE** — all elementary relations considered at that level are internal, with no unresolved boundary flux;
- **CONSERVATION** — an additive quantity has zero net change under those closed internal events.

The test must not identify these concepts by definition.

## 2. Nested structure

Let `W ⊂ W'` be two nested wholes and let `B` be an incidence operator for elementary transfers.

For a closed internal edge `e=(i,j)` the incidence column has one `+1` and one `-1`, therefore

`1ᵀ B_e = 0`.

For a subsystem `W`, split transfers into internal and boundary parts:

`Δr_W = B_int J_int + B_∂ J_∂`.

Then

`1ᵀ Δr_W = 1ᵀ B_∂ J_∂`.

Thus a local source/sink can be a boundary flux relative to `W`, while the same process can be internal to a larger whole `W'`.

This establishes a **level-relative** notion of closure without yet asserting a physical conservation law.

## 3. Control A — same event, different whole

Consider transfer `A ↔ B`.

### Level W₁ = {A,B}

The transfer is internal:

`Δr = (-J,+J)`

and

`ΣΔr = 0`.

### Level W₂ = {A,B,C}

If C is coupled through an additional boundary transfer, the A↔B process remains internal, while A/B↔C can appear as flux at the W₁ boundary.

**Result:** closure depends on the selected system boundary/level. The same physical event can be internal at one level and boundary exchange at another.

**PASS.**

## 4. Control B — open subsystem

Take

`Δr_W = (-J,0)`.

Then

`ΣΔr_W = -J ≠ 0`.

The nonzero balance does not require failure of global conservation; it is compatible with an external transfer through the boundary.

**Result:** an open boundary destroys local zero-sum balance without disproving conservation at a larger closed level.

**PASS.**

## 5. Control C — closure is not conservation

A closed directed cycle can be written as a transfer system whose incidence columns each sum to zero. This gives zero net additive balance for the represented quantity.

However, arbitrary dynamics placed on the cycle can amplify, decay, oscillate, or redistribute internal variables. Topological closure alone does not determine the dynamics or guarantee stability.

**Result:**

`closure → permits an invariant balance`

is defensible under an additive incidence representation, but

`closure → stability`

is false.

**PASS for separation; FAIL for automatic stability.**

## 6. Control D — arbitrary boundary selection

For any graph, changing the chosen subset W changes which edges are classified as internal or boundary edges.

Therefore boundary classification is not an intrinsic property of an isolated edge; it is a relation between the edge and the selected whole.

**Result:** there is no absolute closure without specifying the level/system boundary.

**PASS.**

## 7. Control E — coarse-graining

Let several microscopic nodes be grouped into a macro-node. Internal microscopic transfers cancel in the aggregate if the coarse-graining preserves incidence orientation and the additive balance map.

Boundary transfers remain visible as macro-level flux.

Therefore structure-preserving coarse-graining can preserve the distinction:

`internal cancellation ↔ boundary flux`.

Arbitrary averaging that does not preserve incidence need not preserve it.

**Result:** nested closure is compatible with hierarchical coarse-graining, but only under structure-preserving maps.

**PARTIAL PASS.**

## 8. Control F — memory

Let the transfer magnitude depend on history:

`J = F(state, memory)`.

If the incidence structure remains `(-1,+1)`, then

`Δr = (-J,+J)`

still has zero additive sum.

Memory therefore changes the constitutive law and future accessibility without necessarily breaking conservation.

If memory introduces a source term `s(M)`,

`Δr = BJ+s(M)`,

then conservation can fail at that level.

**Result:** memory and conservation are logically separable.

**PASS.**

## 9. Control G — one level cannot establish universal conservation

Suppose W is closed and an additive scalar is represented by

`R_W = wᵀ r_W`.

Internal incidence gives

`wᵀ B_int J`.

This vanishes for arbitrary internal transfers only if

`wᵀ B_int = 0`.

Thus graph closure supplies an incidence cancellation for the represented balance variables, but it does **not** by itself create the physical scalar valuation `w`.

**Result:**

`closure → conservation of represented incidence balance`

is structural, while

`closure → existence of physical conserved resource`

remains an additional question.

**PASS / OPEN.**

## 10. Control H — relation to Ω-TIME-037

Ω-TIME-037 established that reciprocity is conditional on a closed elementary event plus an additive conserved balance and absence of source/sink.

038 changes the question from:

> Why is the event closed?

to:

> At what level is the event closed?

For nested wholes:

`W₁ ⊂ W₂ ⊂ W₃ ...`

an apparent source/sink at `W₁` can become an internal exchange at `W₂`.

This avoids the circular statement “closed means no exchange” by making closure an explicit boundary classification and treating the boundary flux as an observable term.

## 11. Candidate hierarchy

A more precise structural chain is:

`difference`

`→ distinction / relation`

`→ selected whole W`

`→ internal vs boundary relations`

`→ closure at level W`

`→ incidence cancellation of internal transfers`

`→ conserved additive balance of represented quantities`

`→ reciprocal elementary exchange`

`→ positive-compatible coupling`

`→ ab > 0`

`→ real ± characteristics`

`→ hyperbolic propagation`

`→ causal admissibility`

`→ temporal measure`.

The chain is **conditional**, not a completed fundamental derivation.

## 12. New boundary of the foundation problem

The previous bottleneck “why reciprocity?” moves one level deeper.

The remaining fundamental questions are now:

1. Why does a **whole/system level** exist or become selected from relations?
2. What selects a meaningful boundary rather than an arbitrary subset?
3. Why should elementary internal events admit an additive balance representation?
4. Why does a physical nonnegative scalar valuation exist on that balance?
5. Why should the same compatible coupling govern reciprocal channels?
6. Can these properties be derived from `difference → relation → whole → feedback`, without importing conservation, energy, time, or metric structure?

## 13. Important negative result

A cycle, feedback loop, or graph closure is **not sufficient** to derive:

- physical energy;
- a positive scalar resource;
- stability;
- Lorentzian signature;
- universal propagation speed;
- physical time.

These must remain OPEN until independently derived.

## 14. Decision

### PASS

- Closure is naturally **relative to a selected level/whole**.
- Nested wholes convert local source/sink terms into boundary fluxes of a larger system.
- Incidence-preserving internal events have exact zero-sum balance for the represented additive variables.
- Structure-preserving coarse-graining can retain the internal/boundary distinction.
- Memory can alter transition laws without necessarily violating a conserved incidence balance.

### FAIL

- Boundary alone uniquely selects a whole.
- Closure alone implies stability.
- Closure alone creates a physical energy/resource scalar.
- Graph cycles alone imply conservation of an arbitrary physical quantity.

### OPEN

- Origin/selection of the whole.
- Origin of the boundary criterion.
- Origin of additive valuation.
- Physical meaning and positivity of the conserved scalar.
- Universal reciprocity/common coupling.
- Derivation of Lorentzian geometry and universal `c`.
- Derivation of invariant temporal measure `μ`.

## 15. Current Ω-TIME synthesis

The strongest current working statement is:

> **Time may be reconstructed as a measure of coordinated change along causally admissible trajectories, while causality itself may arise from local reciprocal dynamics inside hierarchically defined wholes.**

This remains a working model, not a fundamental law.

The deepest unresolved bridge is now localized as:

`Ω-foundation → selection of whole + boundary criterion + additive valuation`

rather than directly `Ω-foundation → time`.

---

**Anchor:** Ω-TIME-038  
**Method:** explicit controls, negative controls, level-relative closure, no hidden identification of closure with conservation.  
**Status:** STRUCTURAL PASS / FUNDAMENTAL DERIVATION OPEN
