Appendix Function Node

Function: Gradient

Status: 🟡 Yellow

Purpose

A gradient describes how the One-Wave field changes across space. It compares the projected field state between neighboring positions.

---

Definition

Let the One-Wave field be

[
\psi(x)
]

where \psi represents the local field state.

A spatial differential exists whenever neighboring field states differ:

[
\boxed{\psi(x_1)\neq\psi(x_2)}
]

A gradient is the spatial rate of change of that field state.

---

Mathematics

The gradient operator is

[
\boxed{\nabla\psi}
]

If

[
\psi(x_1)\neq\psi(x_2),
]

then

[
\boxed{\nabla\psi\neq0}
]

If the field is spatially uniform,

[
\psi(x_1)=\psi(x_2),
]

then

[
\boxed{\nabla\psi=0}
]

---

Proof 2: Differential Creates Gradient

Assume a spatial differential exists:

[
\psi(x_1)\neq\psi(x_2)
]

By definition, a gradient measures spatial change in the field.

Therefore,

[
\nabla\psi\neq0
]

Hence,

[
\boxed{\text{Differential}\Rightarrow\text{Gradient}}
]

---

Geometry Rule

The underlying field state is singular.

[
\psi
]

The observed state depends on the active geometry.

Compressed projection:

[
\psi_{2D}=P_{2D}(\psi)
]

Expressed projection:

[
\psi_{3D}
]

The 2D projection preserves only the compressed components of the field state.

The 3D projection preserves the complete expressed state.

Both are projections of the same underlying field rather than separate field variables.

---

Projection Warning

Projection removes observable information.

The hidden components are not zero and not absent.

They remain part of the underlying field but are not represented in the compressed projection.

Therefore,

[
P_{2D}(\nabla\psi_{3D})
\neq
\nabla(P_{2D}\psi_{3D})
]

unless demonstrated otherwise.

A 2D gradient is therefore a compressed approximation of the projected field rather than automatically equivalent to the full 3D gradient.

---

Hungry Gremlin Rule

The 2D Gradient Gremlin predicts the next projected field state using only the compressed projection.

If the predicted recursive update differs from the observed recursive update beyond the accepted tolerance, the Gremlin becomes Hungry.

A Hungry Gremlin requests evaluation using the full 3D projection.

Prediction failure is therefore the experimental trigger for escalation from 2D analysis to 3D analysis.

---

Assumptions

- The field possesses spatial coordinates.
- Neighboring field states are comparable.
- A projection operator exists.
- Projection may remove observable information without removing the underlying field state.

---

Candidate Experiment

1. Compute the projected 2D gradient.
2. Predict the next recursive field state.
3. Compute the full 3D gradient.
4. Compare both predictions with the observed recursive outcome.
5. Measure the divergence.

If the divergence exceeds the accepted tolerance, the Hungry Gremlin condition has been satisfied.

---

Dependencies

- Function: Displacement
- Function: Differential
- Appendix G: Projection Rule (geometry and projection definitions)

---

Yellow Audit Result

The Gradient function is mathematically defined.

The relationship

[
\boxed{\text{Differential}\Rightarrow\text{Gradient}}
]

is established.

Projection effects have been explicitly identified rather than assumed away.

The remaining work belongs to the Projection Rule node, not the Gradient node itself.
