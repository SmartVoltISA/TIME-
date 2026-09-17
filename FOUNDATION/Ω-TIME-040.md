# Ω-TIME-040 — Symmetry attack on whole selection: can persistence choose a unique whole?

**Status:** STRUCTURAL PASS / UNIQUENESS FAIL / FUNDAMENTAL DERIVATION OPEN  
**Date:** 2026-09-17  
**Branch:** `main`

## 1. Question

Ω-TIME-039 showed that relational closure can construct candidate wholes once a seed/context and closure rule are supplied, but relation alone does not select one unique whole.

The next attack asks whether **persistence under feedback** removes that missing premise.

Candidate:

`relation → feedback → perturbation persistence → selected whole`.

The test must distinguish:

- existence of persistent structures;
- selection among them;
- uniqueness of selection.

No energy, conservation, resource, physical time, or metric is used as a selection variable.

## 2. Symmetric double-whole control

Construct a relational graph with two isomorphic internally dense communities A and B and weak symmetric coupling between them.

Because A and B have the same structural statistics, any selection rule invariant under graph relabeling must assign the same status to A and B.

Therefore if both persist, symmetry prevents the graph alone from selecting A over B.

**Result:** persistence does not imply uniqueness.

**UNIQUENESS FAIL.**

## 3. Perturbation test

Apply an equivalent perturbation separately to A and B and evaluate the resulting structural recurrence/persistence.

Because the communities are isomorphic and the perturbation protocol is symmetric, the measured persistence is equal up to numerical tolerance.

A selector that returns A but not B would therefore violate relabeling/isomorphism invariance.

**Result:** a symmetric system can contain multiple equally valid persistent wholes.

**PASS.**

## 4. Symmetry-breaking control

Modify one structural parameter of A while keeping the selection procedure unchanged, for example:

- internal connectivity;
- boundary leakage;
- feedback strength;
- defect/constraint pattern.

The two candidates are no longer structurally equivalent. A persistence criterion can then distinguish them.

This shows that selection can follow a structural asymmetry, but the criterion still has to be specified.

**Result:** asymmetry can remove degeneracy, but does not derive the selection functional itself.

**PARTIAL PASS.**

## 5. Dynamics-dependence control

Keep the same static relational graph but change the feedback/update rule.

Different admissible update laws can favor different structures:

- reinforcement can favor dense recurrence;
- diffusion can favor broad connectivity;
- inhibition can favor separation;
- threshold dynamics can favor strongly coupled cores.

Thus the same relation graph does not uniquely determine which whole is persistent unless the dynamics/selection rule is independently specified.

**Result:**

`static relation → unique persistent whole`

is false in general.

**FAIL.**

## 6. Negative control — persistence without identity

A dynamically persistent pattern need not correspond to a persistent node set.

A traveling or rotating pattern can preserve its form while changing which nodes participate.

Therefore:

`pattern persistence ≠ fixed object identity`.

A further identity criterion is required if the “whole” is intended to remain the same entity rather than merely the same organizational form.

**Result:** persistence alone is insufficient for object identity.

**FAIL for automatic identity.**

## 7. Nested persistence

If A and B each form persistent substructures while A∪B also forms a persistent larger structure, then persistence exists at multiple scales.

Therefore the system may contain a hierarchy:

`whole₁ ⊂ whole₂ ⊂ ...`.

No single scale is selected merely because it is persistent.

**Result:** hierarchical wholes remain the natural structural outcome.

**PASS.**

## 8. Memory control

Let previous relational changes modify future accessibility.

Two currently identical coarse structures can retain different transition rules because their histories differ.

Then persistence and future accessibility become history-dependent.

Memory can therefore break an otherwise static degeneracy, but it does so by adding state/history information.

**Result:** memory can participate in selection but cannot be counted as a derivation from relation alone.

**PARTIAL PASS.**

## 9. Selection theorem — negative form

Assume a selection rule F depends only on a relational structure G and is invariant under graph isomorphism.

If G contains two isomorphic candidate wholes A and B and the full graph automorphism exchanges A↔B, then F must assign equivalent selection status to A and B.

Therefore no isomorphism-invariant rule using G alone can uniquely select A while rejecting B.

This is a structural impossibility result, not a numerical accident.

**PASS.**

## 10. What this does to the Ω chain

The previous chain

`difference → relation → persistent whole`

must be weakened to

`difference → relation → candidate wholes → selection criterion/dynamics → persistence → selected whole(s)`.

And if symmetry is present:

`selection → possibly multiple equivalent wholes`.

Uniqueness requires an additional symmetry-breaking fact, boundary condition, history, seed, environment, or selection principle.

## 11. Critical distinction

There are now four separate concepts:

1. **Candidate whole** — a relation-complete subset.
2. **Persistent whole** — a candidate whose organization survives the specified perturbation/dynamics.
3. **Identity** — a rule saying when two persistent configurations count as the same whole across change.
4. **Selection** — a rule choosing one candidate or a class of candidates among alternatives.

None of these four should be silently identified with the others.

## 12. Negative result for fundamental closure

The attack rejects all strong automatic claims:

- relation alone → unique whole;
- closure alone → unique whole;
- persistence alone → unique whole;
- persistence alone → fixed identity;
- feedback alone → unique selection.

What survives is weaker and more defensible:

> Relations can generate candidate relationally complete wholes; dynamics and history can distinguish persistent structures; uniqueness requires an additional symmetry-breaking or selection condition.

## 13. Implication for capacity/resource

This result is important for the earlier resource problem.

If the whole itself is not uniquely selected from relations, then a scalar capacity assigned to “the system” cannot be assumed fundamental before the system boundary/identity is specified.

Therefore the order should remain:

`selection/identity of level → admissible transitions → capacity valuation`.

Not:

`difference → resource → whole`.

## 14. Decision

### PASS

- Persistent relational structures can exist without an energy or conservation premise.
- Symmetric graphs can contain multiple equally valid persistent wholes.
- Isomorphism invariance prevents arbitrary selection among structurally identical candidates.
- Asymmetry/history/dynamics can distinguish candidates.
- Persistent structures can form nested hierarchies.

### FAIL

- Persistence alone uniquely selects a whole.
- Feedback alone uniquely selects a whole.
- Persistence alone defines object identity.
- Static relation alone determines the relevant dynamics/selection rule.

### OPEN

1. What is the minimal non-arbitrary selection principle?
2. Can symmetry breaking emerge from the same `difference → relation` process rather than being externally inserted?
3. Can identity be derived as persistence of relational constraints rather than node membership?
4. Can admissible transition capacity be defined before unique object selection?
5. Can additive valuation emerge from composition of selected relational wholes?

## 15. Updated fundamental frontier

The deepest unresolved bridge is now:

`difference → relation → candidate wholes → why one persistent organization rather than another?`

Only after this is solved should the chain proceed to:

`selected level → admissible transitions → capacity/valuation → conservation/reciprocity → hyperbolic causality → temporal measure`.

**Final status:** STRUCTURAL PASS / UNIQUENESS FAIL / FUNDAMENTAL DERIVATION OPEN.
