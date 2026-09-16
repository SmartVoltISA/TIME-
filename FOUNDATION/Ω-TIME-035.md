# Ω-TIME-035 — What forces a quadratic resource valuation?

## Status
**STRUCTURAL PASS / CONDITIONAL DERIVATION PASS / FUNDAMENTAL DERIVATION OPEN.**

## Question
Ω-TIME-034 isolated scalarization as an additional layer. The next question is sharper:

> Can a quadratic valuation be forced from minimal composition principles, rather than assumed?

Candidate principles:

1. `R(0)=0`;
2. `R(x)≥0`;
3. continuity;
4. additivity for independent components;
5. invariance under relabeling/equivalent orthogonal coordinates;
6. consistent composition of independent subsystems.

The test separates what follows from weak assumptions from what requires the stronger symmetry axiom.

## Check 1 — Weak additivity permits many valuations

For componentwise independent coordinates, define

`R_p(x)=Σ_i |x_i|^p`, `p>0`.

Then

`R_p(x,y)=R_p(x)+R_p(y)`

for independent coordinate blocks, and `R_p≥0` with `R_p(0)=0`.

Thus positivity + continuity + independent additivity alone do not select `p=2`.

### Result
**FAIL for uniqueness under weak axioms.**

Examples `p=1,2,3,4` all survive these requirements.

## Check 2 — Relabeling invariance is too weak

A permutation of coordinates leaves every `R_p` unchanged:

`R_p(Px)=R_p(x)`.

Therefore invariance under pure relabeling does not select the quadratic form.

### Result
**FAIL for uniqueness.**

A stronger equivalence principle is required.

## Check 3 — Orthogonal invariance distinguishes the quadratic case

Require invariance not only under permutations but under every orthogonal change of equivalent coordinates:

`R(Qx)=R(x)`, with `QᵀQ=I`.

For the Euclidean norm,

`R_2(x)=||x||²`,

this holds exactly because

`||Qx||²=xᵀQᵀQx=xᵀx`.

For `p≠2`, generic rotations change the value.

### Numerical control
Use

`x=(1,0)`

and rotate by `45°`:

`Qx=(1/√2,1/√2)`.

Then

`R_p(x)=1`,

while

`R_p(Qx)=2(1/√2)^p=2^(1-p/2)`.

Therefore:

- `p=2` → `R=1` exactly;
- `p=1` → `R=√2`;
- `p=3` → `R≈0.7071`;
- `p=4` → `R=0.5`.

### Result
**PASS.**

Full orthogonal invariance eliminates the generic `p≠2` alternatives.

## Check 4 — Additivity + rotational equivalence gives quadratic structure

Assume the resource decomposes over orthogonal independent directions:

`R(x)=Σ_i φ(x_i)`

with a common function `φ` for equivalent directions.

Rotational invariance in any two-dimensional subspace requires

`φ(x²)+φ(y²)`

to depend only on

`x²+y²`.

Define

`F(s)=φ(s)` for `s≥0`.

Then the composition condition implies, for independent orthogonal components,

`F(a)+F(b)=F(a+b)`

under the corresponding representation.

With continuity, the additive Cauchy equation has the regular solution

`F(s)=c s`.

Hence

`R(x)=c Σ_i x_i² = c ||x||²`,

with `c≥0` from nonnegativity and `c>0` for nontrivial valuation.

### Result
**CONDITIONAL DERIVATION PASS.**

Quadratic valuation follows if the orthogonal-composition assumptions are accepted.

This is stronger than the result of Ω-TIME-033: the quadratic form is no longer merely a convenient choice, but a consequence of a specified symmetry/composition package.

## Check 5 — Matrix form and anisotropic generalization

If equivalent-coordinate rotational invariance is weakened, the natural continuous quadratic form is

`R(x)=xᵀGx`,

with `G=Gᵀ≥0`.

If all coordinate directions are physically equivalent, symmetry reduces this to

`G=cI`.

If equivalence is broken, different positive coefficients are allowed.

### Result
**PASS.**

The foundation may determine a quadratic class without necessarily determining isotropy.

## Check 6 — Strict positivity again requires complete distinction

For

`R(x)=xᵀGx`,

nonnegative semidefinite `G` permits null directions.

Strict positivity,

`R(x)>0` for all nonzero relevant `x`,

requires

`ker(G) ∩ V_relevant = {0}`.

This reproduces the completeness condition found in Ω-TIME-032/033.

### Result
**PASS.**

The distinction between `G≥0` and `G>0` is not removed by deriving the quadratic form.

## Check 7 — Overall scale remains free

If

`R(x)=c||x||²`,

then every `c>0` satisfies the same structural axioms.

Therefore the axioms can determine the shape of the valuation but not its absolute numerical unit.

### Result
**OPEN for absolute scale.**

An independent calibration/reference is required.

This is consistent with the unresolved absolute temporal scale and universal `c` in the earlier TIME anchors.

## Check 8 — Negative control: remove orthogonal equivalence

Without full orthogonal invariance, `R_1`, `R_2`, `R_3`, `R_4` all satisfy positivity, continuity and independent additivity.

### Result
**FAIL for uniqueness.**

Therefore the quadratic result is conditional on a genuine equivalence/symmetry principle, not on positivity alone.

## Check 9 — Negative control: remove additivity

Even with rotational invariance, functions such as

`R(x)=f(||x||²)`

remain rotationally invariant for many monotone continuous `f`.

Examples:

`R=||x||²`,
`R=||x||⁴`,
`R=exp(||x||²)-1`.

### Result
**FAIL for uniqueness.**

Composition/additivity is essential to reduce the family to a linear function of `||x||²`.

## Check 10 — Negative control: allow indefinite valuation

If `c<0`, the same algebraic rotational invariance and additivity remain, but the valuation is nonpositive rather than resource-like.

More generally, an indefinite `G` permits positive and negative directions.

### Result
**FAIL for positive resource.**

Nonnegativity is a genuine structural input.

## Check 11 — Connection to Ω-TIME-031/032

Ω-TIME-031 established that

`G>0 + GA symmetric → ab>0`.

Ω-TIME-032 established a route from complete distinction toward

`G=DᵀD≥0`

and then strict positivity under completeness.

The present anchor adds a different result:

`composition + equivalence + continuity → quadratic valuation class`.

Thus the route can be written more precisely as:

`difference/distinction`
`→ admissible transition structure`
`→ scalarization principles`
`→ nonnegative valuation`
`→ [composition + equivalence + continuity]`
`→ quadratic metric class`
`→ completeness`
`→ G>0`
`→ reciprocal exchange + compatibility`
`→ ab>0`
`→ hyperbolic propagation.

## Decision
**PASS:** positivity + continuity + independent additivity alone do not uniquely force quadratic form.

**PASS:** relabeling invariance alone does not force quadratic form.

**PASS:** full orthogonal equivalence removes generic `p≠2` norm alternatives.

**PASS:** with independent additivity, orthogonal equivalence and continuity, the regular scalar valuation is quadratic up to scale.

**PASS:** anisotropic quadratic forms remain possible when directional equivalence is not assumed.

**PASS:** strict positivity still requires completeness/no blind directions.

**FAIL:** difference alone forces a quadratic resource.

**FAIL:** positivity alone forces a quadratic resource.

**FAIL:** conservation alone forces a quadratic resource.

**OPEN:** why the relevant degrees of freedom should obey the required equivalence principle.

**OPEN:** why resource composition should be additive.

**OPEN:** why the valuation scale is fixed physically.

**OPEN:** why reciprocal exchange and common coupling follow from the same foundation.

## Main result
A significant part of the previous "resource" mystery can now be decomposed:

- **shape** of the scalar valuation can be conditionally derived from symmetry + composition + regularity;
- **positivity** is an independent requirement;
- **strict positivity** requires complete distinction;
- **absolute scale** remains free;
- **reciprocity/conservation** remains a separate structural problem.

This prevents the statement "difference implies energy" while allowing a stronger, testable statement:

> If equivalent independent distinctions compose additively and the valuation is invariant under changes of equivalent coordinates, continuity forces a quadratic metric form up to scale.

That is a conditional theorem of the model class, not yet a universal physical law.

## Next decisive target
Attack the remaining reciprocity step:

`distinction + positive metric + composition → reciprocal exchange?`

Test whether a single shared boundary relation mathematically forces opposite balance signs, or whether reciprocity is another independent axiom.

## Rule
FACT → CHECK → RESULT → DECISION → FIXATION.
PASS, FAIL and OPEN remain separate.
