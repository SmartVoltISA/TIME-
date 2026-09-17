# Ω-TIME-046 — Orientation does not determine feedback sign

**Status:** STRUCTURAL PASS / SIGN DERIVATION FAIL / FUNDAMENTAL DERIVATION OPEN

## Question

Can the sign of feedback be derived from the orientation of a relation alone?

Target chain:

`difference → directed relation → orientation → feedback sign`

The test asks whether orientation itself selects positive reinforcement rather than restoring response.

## Minimal two-channel model

Let

`u_dot = a v`

`v_dot = b u`

with

`A = [[0,a],[b,0]]`.

The eigenvalues satisfy

`lambda^2 = ab`.

Therefore:

- `ab > 0` → real opposite-sign characteristics `±sqrt(ab)`;
- `ab = 0` → degenerate zero spectrum;
- `ab < 0` → imaginary pair `±i sqrt(-ab)`.

Orientation specifies which channel is written as source/target, but it does not by itself constrain the signs of `a` and `b`.

## Orientation reversal control

Reverse the bookkeeping orientation of an incidence edge:

`b_edge → -b_edge`.

If the transfer variable is simultaneously reoriented,

`J → -J`,

the physical state change

`Δr = b_edge J`

is unchanged.

Thus orientation reversal is a representation change, not a mechanism that changes the physical response sign.

## Numerical control

Representative coefficient sweep:

| a | b | ab | spectrum | interpretation |
|---:|---:|---:|---|---|
| 1 | 1 | +1 | ±1 | hyperbolic / reinforcing-compatible |
| 1 | -1 | -1 | ±i | elliptic-type / non-hyperbolic |
| -1 | -1 | +1 | ±1 | hyperbolic / opposite orientation convention |
| -1 | 1 | -1 | ±i | non-hyperbolic |
| 2 | 0.5 | +1 | ±1 | same propagation scale |
| 2 | -0.5 | -1 | ±i√1 | sign changed by constitutive response, not orientation |

The cases show that the same two-node relational topology admits both signs of `ab`.

## Negative control: orientation-only derivation

Assume only:

1. two distinct states;
2. one directed relation;
3. an orientation label;
4. local coupling.

These assumptions do not impose either

`a b > 0`

or

`a b < 0`.

Both remain admissible.

Therefore:

**orientation alone does not derive the sign of feedback.**

## Important distinction

A directed arrow answers:

> which variable is allowed to influence which variable?

It does not answer:

> does the receiving variable change in the same direction or in the opposite direction?

That second question is the sign of the constitutive response.

A feedback-loop sign is determined by the combined signs of the interactions around the loop, not merely by the existence or orientation of arrows. This is standard in dynamical-systems and causal-network representations. External sources distinguish positive/reinforcing and negative/stabilizing feedback by the signs of the component interactions around the loop. 

## Relation to Ω-TIME-042…045

- Ω-TIME-042: difference alone does not choose positive feedback.
- Ω-TIME-043: changing coupling sign changes amplification/restoration but the sign is an added rule.
- Ω-TIME-044: memory can accumulate an interaction trace but does not determine the sign of response.
- Ω-TIME-045: positive relational/resource valuation does not force positive feedback; ordinary gradient response is restoring.
- Ω-TIME-046: orientation also fails to determine the sign.

The candidate fundamental chain therefore loses another possible shortcut:

`relation → orientation → positive feedback`

is not established.

## Strong negative result

The following implication is **not derived**:

`directed relation ⇒ positive feedback`.

Likewise,

`directed relation ⇒ negative feedback`

is not derived.

The sign belongs to an additional constitutive rule or deeper structural constraint.

## Current fundamental boundary

The unresolved node is now sharply localized:

`relation + direction + memory + positive valuation → ??? → sign of constitutive response`.

To close this gap, Ω must derive a rule that determines whether a change causes the next change to continue in the same direction or oppose it.

Possible deeper candidates to test, without assuming their result:

1. reciprocity and conservation;
2. competition between alternative transitions;
3. saturation/finite capacity;
4. delayed response;
5. curvature or second-order change;
6. selection of the transition that preserves admissibility;
7. coupling between change and its own accumulated trace.

Each must be tested with positive and negative controls.

## Decision

**PASS:** orientation is a legitimate structural component and determines causal bookkeeping.

**FAIL:** orientation alone does not determine positive feedback.

**FAIL:** topology alone does not determine the sign of the constitutive response.

**OPEN:** fundamental source of the sign.

## Working chain

`difference → relation → orientation → constitutive response → sign → feedback regime → polarity/stability`

The first three nodes are structurally representable. The fourth remains the current fundamental bottleneck.
