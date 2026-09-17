# Ω-TIME-050 — Can boundary geometry force the sign of transition-cost change?

**Status:** STRUCTURAL NEGATIVE RESULT / SIGN ORIGIN OPEN / FUNDAMENTAL DERIVATION OPEN

## 1. Target

After Ω-TIME-048/049 the remaining hole is localized to the sign of the change in the cost of repeating a relation.

Target:

`difference → relation → boundary/closure → transition geometry → cost change → feedback sign`

Question: can boundary/closure alone force a completed transition to make continuation of the same relation cheaper?

## 2. Minimal transition coordinate

Let `d` denote relational asymmetry and let `C(d)` be a local transition cost for continuing the same relational direction.

A completed event changes the state by `Δd` and therefore changes the marginal continuation cost by

`ΔC ≈ C'(d) Δd`.

Positive feedback requires the continuation cost to decrease in the direction already taken:

`ΔC_same < 0`.

Restoring feedback requires

`ΔC_same > 0`.

Neutral response has `ΔC_same = 0`.

## 3. Symmetric boundary-compatible counterexample

Take the bounded state `d ∈ [-1,1]` and two costs

`C_+(d)=C0-ad`

and

`C_-(d)=C0+ad`, with `a>0`.

Both can be made nonnegative on the same bounded domain by choosing `C0>a`.

Under exchange `d→-d`, the two descriptions are mapped into each other. Neither violates positivity, locality, boundedness, or the existence of the same boundary states.

For motion toward positive `d`:

`C_+'(d)=-a` gives decreasing continuation cost;

`C_-'(d)=+a` gives increasing continuation cost.

Thus the same boundary geometry permits both reinforcement and restoration.

## 4. Geometric metric control

A possible stronger premise is that cost is path length in a positive metric:

`C[γ]=∫ sqrt(g_ij(q) dq^i dq^j)`.

But positivity of `g` fixes nonnegative length, not whether a particular state change lowers or raises the cost of future motion.

Two positive metrics can have opposite state dependence along the same coordinate. Therefore metric positivity alone does not determine `∂C/∂d`.

This is consistent with the earlier Ω result that a positive graph Laplacian gives a positive structural form but does not by itself select Lorentzian sign or causal orientation.

## 5. Boundary-distance control

Suppose continuation cost is distance to a boundary:

`C_1(d)=1-d`,

for the positive boundary, while cost measured from the opposite boundary is

`C_2(d)=1+d`.

Both are legitimate distances on the same interval. Choosing which boundary is the target is additional information.

Therefore `boundary exists` does not imply `motion toward this boundary becomes cheaper`.

## 6. Closure control

Closure says that an elementary event is internally represented and has no unresolved external incidence. It constrains admissible transitions but does not supply an ordering of costs among admissible transitions.

Formally, if `A(q)` is the admissible transition set and `C:A(q)→R_+` is a cost valuation, closure constrains `A(q)` but does not uniquely determine `C`.

Hence:

`closure → admissibility`

but not, without an extra principle,

`closure → decreasing continuation cost`.

## 7. Stronger candidate: shortest continuation principle

If one postulates that realized transitions minimize future continuation cost, then reinforcement can emerge: repeated motion can follow a locally shortened path.

But this is a new variational/optimization principle. It cannot be counted as derived from difference or closure unless an independent derivation of that minimization principle is found.

This is a relocation of the hole, not a closure of it.

## 8. Adaptive-topology control

Adaptive networks are known to exhibit state↔topology feedback and self-organization through local update rules. The existence of this feedback loop does not by itself fix the sign of the topological response; the update rule supplies the direction. This is established in the adaptive-network literature and is used here only as an external control, not as evidence for the Ω derivation.

## 9. Negative-control theorem within the tested class

Assume only:

1. bounded relational state;
2. boundary/closure;
3. positive finite transition cost;
4. exchange symmetry;
5. locality;
6. smoothness.

Then both a locally decreasing continuation cost and a locally increasing continuation cost can be constructed while preserving all six assumptions.

Therefore no theorem using only these assumptions can derive positive feedback.

## 10. What remains genuinely missing

The missing principle is now narrower:

`Ω-foundation → why does a realized relation alter the future valuation of that relation in one preferred direction?`

Candidate sources:

- path minimization;
- accessibility maximization;
- geometric shortening;
- resource accumulation;
- irreversible state-space deformation;
- causally preferred continuation;
- a deeper variational principle;
- a monotonicity law connecting realized transition and future accessibility.

Each must be tested with its opposite-sign control.

## 11. Decision

**PASS:** boundary/closure can constrain the admissible transition space.

**FAIL:** boundary/closure alone do not determine transition-cost ordering.

**FAIL:** positive metric/cost alone does not determine the sign of marginal cost change.

**OPEN:** derive a monotonic relation between realized transition and future continuation cost from a deeper Ω principle without inserting optimization, preference, or positive feedback under another name.

## 12. Updated frontier

`difference → relation → boundary → closure → admissible transitions → cost valuation → marginal cost change → ??? → feedback sign → polarity`

The hole is now localized at the arrow:

`realized transition → preferred change of future transition valuation`.

This is the next fundamental target.
