# Ω-TIME-044 — Memory of interaction: does repetition derive the sign of reinforcement?

**Status:** STRUCTURAL PASS / SIGN DERIVATION FAIL / FUNDAMENTAL DERIVATION OPEN

## Question

Can the positive feedback required for polarization emerge from repeated interaction and memory, without inserting the sign of plasticity as an additional rule?

The previous Ω-TIME-042/043 controls showed that a relational difference does not determine whether feedback is restoring or amplifying. Here the next candidate is memory: repeated interaction changes the strength of the relation.

## 1. Minimal relational system

Let

\[
d=a-b
\]

and let `w` be a memory variable representing accumulated interaction history.

For an ordinary reciprocal exchange,

\[
\dot a=w(b-a),\qquad
\dot b=w(a-b),
\]

so

\[
\dot d=-2wd.
\]

If `w>0`, stronger remembered coupling makes the difference decay faster.

Therefore **memory amplification of a coupling is not equivalent to positive feedback of the difference**.

## 2. Memory update

A minimal activity-dependent reinforcement rule is

\[
\dot w=\eta F(d)-\gamma w.
\]

For an unsigned repetition measure such as

\[
F(d)=d^2\ge0,
\]

memory grows when the relation is repeatedly active and decays otherwise.

But the state equation remains

\[
\dot d=-2wd.
\]

Thus increasing memory strengthens the restoring response rather than changing its sign.

This is a decisive control: **positive memory of interaction does not by itself produce positive feedback of the relational difference.**

## 3. What would produce amplification?

To obtain

\[
\dot d=+2wd,
\]

the state coupling must instead be

\[
\dot a=w(a-b),\qquad
\dot b=w(b-a).
\]

The sign has now been changed explicitly. Memory can amplify the magnitude of an already anti-restoring coupling, but it did not derive that coupling sign.

Likewise, a nonlinear polarity model

\[
\dot d=\lambda(w)d-\mu d^3
\]

requires a condition such as `\lambda(w)>0`. The memory variable can modulate the gain, but the positive sign remains an additional constitutive assumption unless derived elsewhere.

## 4. Numerical control

A direct discrete integration was run for the two-node system with

- `a(0)=1`, `b(0)=-1`;
- `w(0)=0`;
- memory reinforcement `\dot w=0.05d^2-0.01w`;
- reciprocal exchange `\dot d=-2wd`;
- explicit Euler step `Δt=0.01`.

The relational difference decreased from approximately `|d|=2` to `|d|≈0.0068`, while the memory variable increased to approximately `w≈0.5035`.

The observed behavior is therefore:

\[
\text{repetition} \rightarrow \text{stronger memory} \rightarrow \text{stronger restoration},
\]

not

\[
\text{repetition} \rightarrow \text{positive feedback}.
\]

## 5. Negative controls

### Control A — no memory

With fixed positive `w`, the reciprocal system still gives

\[
\dot d=-2wd.
\]

Memory is not required for restoration.

### Control B — positive memory + reversed coupling

With the same memory rule but `\dot d=+2wd`, the difference grows. However, the sign reversal is explicitly inserted, so this does not constitute a derivation.

### Control C — signed memory update

Rules based directly on the sign of `d` can preserve or reverse polarity, but that introduces an orientation-dependent constitutive rule. Again, the required sign is supplied by the update law.

## 6. Relation to known plasticity

Activity-dependent synaptic plasticity is an established mechanism associated with learning and memory, but biological plasticity contains both potentiating and stabilizing mechanisms. Reviews explicitly distinguish Hebbian positive feedback from homeostatic negative feedback and emphasize that additional rules can be required for stability. This supports using plasticity as a control model, not as a fundamental derivation of the feedback sign.

## 7. Decision

**PASS:** memory can be represented as a state variable whose strength depends on repeated interaction.

**PASS:** repeated interaction can strengthen a coupling without violating reciprocal balance when the incidence structure is preserved.

**FAIL:** memory/repetition alone does not derive the sign required for amplifying feedback.

**FAIL:** stronger positive coupling does not imply positive feedback of the difference; for reciprocal exchange it strengthens restoration.

**OPEN:** whether the sign of the constitutive response can be derived from a deeper Ω structure such as admissibility, resource redistribution, competition, or a relation between change and its own induced constraint.

## 8. Updated fundamental boundary

The chain is now more sharply localized:

\[
\text{difference}
\rightarrow
\text{relation}
\rightarrow
\text{repeated interaction}
\rightarrow
\text{memory}
\not\Rightarrow
\text{positive feedback}.
\]

To obtain polarity we still need a principled source of the sign:

\[
\text{memory}
\rightarrow
\boxed{\text{constitutive sign}}
\rightarrow
\text{amplification}
\rightarrow
\text{polarity}.
\]

The next fundamental attack should therefore test whether **constraint/competition generated by the change itself** can force the sign, without importing a positive-gain coefficient.

## 9. Reproducibility note

This anchor intentionally records a negative result. No earlier Ω-TIME file is modified. The historical chain remains immutable.
