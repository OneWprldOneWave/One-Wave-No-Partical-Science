Here’s the full Oscillation node, with the Green proof and Yellow audit state combined cleanly, so it can sit in Appendix A without pretending the crossing inequality is already solved. Tiny mercy from the math goblin.

Function Node

Function: Oscillation

Status: 🟢 Green
Yellow Audit: Open

---

Purpose

Oscillation describes repeated motion about a shared ground.

It occurs when bounded motion and inertial memory combine so that a mode repeatedly crosses the ground rather than simply returning to it.

---

Definition

Let displacement from ground be

[
x=\psi-\psi_0.
]

Let the restoring response be

[
F_{OW}=-\mathcal{A}(x).
]

Let inertial memory be carried by

[
(1-\gamma)\Delta\psi_n.
]

An oscillation is repeated crossing of the shared ground produced by the interaction of bounded motion, restoring response, and inertial memory.

---

Mathematics

Bounded Motion confines the mode to a finite region around ground.

Restoring Response points toward ground.

Inertial Memory carries the previous state change into the next update.

At the ground,

[
x=0,
]

the restoring response momentarily vanishes because there is no displacement from ground.

Whether the mode crosses the ground therefore depends on the motion carried into the crossing by Inertial Memory:

[
(1-\gamma)\Delta\psi_n.
]

If this carried motion remains sufficient at the ground, the mode crosses into the opposite side of the restoring field.

Once the mode crosses ground, displacement changes sign.

The restoring response then reverses relative to the new displacement and points back toward ground again.

Repeated ground crossing produces oscillation.

---

Proof

Assume:

- Bounded Motion has been established.
- Restoring Response points toward ground.
- Inertial Memory carries previous motion through

[
(1-\gamma)\Delta\psi_n.
]

If the carried motion remains sufficient for the mode to cross the shared ground, then the mode overshoots ground.

After crossing, displacement changes sign.

The restoring response acts toward ground from the opposite side.

This creates repeated ground crossing.

Therefore,

[
\boxed{
\text{Bounded Motion}
+
\text{Inertial Memory}
+
\text{Ground Crossing}
\Rightarrow
\text{Oscillation}.
}
]

---

Alternative Outcome

If inertial memory decays before the mode crosses ground, the mode returns toward equilibrium without overshooting.

This produces non-oscillatory return rather than oscillation.

Therefore,

[
\boxed{
\text{Bounded Motion}
+
\text{Inertial Memory}
\not\Rightarrow
\text{Oscillation}
}
]

unless ground crossing occurs.

---

Crossing Condition

The Green node identifies ground crossing as the boundary between oscillation and non-oscillatory return.

The relevant carried-motion term is

[
(1-\gamma)\Delta\psi_n.
]

If this term remains strong enough to carry the mode through

[
x=0,
]

then oscillation occurs.

If this term decays before crossing, return-to-ground occurs without oscillation.

The exact crossing inequality has not yet been derived.

---

Multi-Component Extension

This node treats

[
\psi
]

as a scalar field.

Future Yellow audit must determine whether the crossing condition should instead be evaluated on the complete state

[
\psi_{3D}=(E,C,F,B,U,D).
]

Different components may carry different inertial-memory behavior or response-channel behavior.

Whether oscillation commutes with projection remains open and is inherited from Projection / Blocker 0.

---

Assumptions

- Ground / Zero exists.
- Bounded Motion has been established.
- Restoring Response points toward ground.
- Inertial Memory carries previous motion.
- Oscillation requires ground crossing.
- This Green node treats \psi as scalar.
- Multi-component oscillation and projection consistency remain open for Yellow audit.

---

Candidate Experiment

Objective

Determine the conditions required for repeated ground crossing.

Procedure

1. Generate bounded motion.

2. Vary the inertial-memory parameter

[
\gamma.
]

3. Measure whether the mode:

- returns without crossing,
- crosses once,
- oscillates repeatedly,
- decays,
- or becomes unstable.

4. Measure:

- first ground crossing,
- overshoot,
- oscillation amplitude,
- decay rate.

5. Identify the boundary separating:

- monotonic return,
- damped oscillation,
- sustained oscillation,
- unstable growth.

6. Repeat the test for scalar and multi-component states if \psi_{3D} is available.

---

Dependencies

Core Functions

- Ground / Zero
- Bounded Motion
- Inertial Memory

Supporting Functions

- Restoring Response
- Projection
- Prediction

---

Green Audit Result

This node establishes that oscillation is not implied by bounded motion alone.

Oscillation requires successful ground crossing produced by the interaction of bounded motion and inertial memory.

The exact mathematical crossing condition remains open for Yellow audit.

---

Yellow Audit Target

Derive the inequality governing successful ground crossing.

The target is to determine when

[
(1-\gamma)\Delta\psi_n
]

is sufficient to carry the mode through

[
x=0.
]

This should produce the One-Wave-native boundary between:

[
\text{Oscillation}
]

and

[
\text{Return to Ground}.
]

---

Final Green Lock

[
\boxed{
\text{Bounded Motion}
+
\text{Inertial Memory}
+
\text{Ground Crossing}
\Rightarrow
\text{Oscillation}.
}
]

[
\boxed{
\text{No Ground Crossing}
\Rightarrow
\text{Non-Oscillatory Return}.
}
]

[
\boxed{
(1-\gamma)\Delta\psi_n
\text{ controls the crossing mechanism.}
}
]
