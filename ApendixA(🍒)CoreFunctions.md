Appendix Red A: Core Functions
Introduction
Appendix Red A establishes the foundational functions of the One-Wave framework.
These functions define the mathematical and logical operations upon which later appendices and books are built.
Each function is presented as an independent node containing its purpose, definition, assumptions, dependencies, candidate experiment, and audit status.
The purpose of Appendix Red A is to establish the core functional language before applying it to larger structures developed in later sections of the repository.


---

Function Node

Function: Ground / Zero

Status: 🟢 Green

---

Purpose

Ground / Zero defines the reference state against which all displacement, differential, and motion are measured.

Every subsequent function that computes a difference assumes a reference ground exists. This node establishes that reference explicitly.

---

Definition

Let the field state be

[
\psi
]

Let the reference ground be

[
\psi_0.
]

Displacement from ground is defined as

[
\boxed{x=\psi-\psi_0.}
]

This definition is meaningful only if the reference ground is well-defined.

---

Same-Ground Rule

When comparing two successive field states,

[
\psi_n
\quad\text{and}\quad
\psi_{n-1},
]

both must be measured relative to the same reference ground:

[
\boxed{\psi_{0,n}=\psi_{0,n-1}.}
]

Under this assumption,

[
\Delta x_n

x_n-x_{n-1}

(\psi_n-\psi_0)-(\psi_{n-1}-\psi_0)

\psi_n-\psi_{n-1}

\Delta\psi_n.
]

This establishes that the common ground cancels when successive states share the same reference.

---

No Ground, No Displacement

Without a defined reference ground,

[
x=\psi-\psi_0
]

cannot be evaluated.

Therefore,

[
\boxed{\text{No Ground} \Rightarrow \text{No Displacement}.}
]

---

Open Question 1: Geometry Invariance

Does the reference ground remain the same under compressed and expressed representations?

[
\boxed{\psi_{0,2D}\ ?=\ \psi_{0,3D}.}
]

This question remains open and is inherited by Projection.

---

Open Question 2: Time Invariance

Does the reference ground remain constant through recursive updates?

[
\boxed{\psi_{0,n}=\psi_{0,n-1}}
]

is currently assumed for successive comparisons but has not been proven over arbitrary time.

---

Assumptions

- A reference ground exists.
- Displacement is measured relative to that ground.
- Successive comparisons use the same reference ground.
- Geometry invariance remains unresolved.
- Long-term ground drift remains unresolved.

---

Candidate Experiment

Objective

Determine whether the reference ground changes with time or geometry.

Procedure

1. Establish a baseline reference ground.
2. Measure the apparent ground after repeated recursive updates.
3. Compare compressed (2D) and expressed (3D) representations of the same configuration.
4. Determine whether the reference ground remains invariant within experimental tolerance.

---

Dependencies

Core Functions

None

Downstream Functions

- Displacement
- Differential
- Gradient
- Local Stability
- Bounded Motion
- Inertial Memory
- Projection

---

Green Audit Result

This node establishes the reference structure upon which all displacement-based functions depend.

The mathematical definition is complete under its stated assumptions.

Geometry invariance and long-term ground stability remain open questions for future audit.

---

Final Green Lock

[
\boxed{x=\psi-\psi_0}
]

[
\boxed{\psi_{0,n}=\psi_{0,n-1}\ \text{(assumed for successive comparisons)}}
]

[
\boxed{\psi_{0,2D}\ ?=\ \psi_{0,3D}}
]

[
\boxed{\text{No Ground} \Rightarrow \text{No Displacement}}
]
---

Function Node

Function: Displacement

Status: 🟢 Green

---

Purpose

Displacement is the fundamental departure from equilibrium.

It is the first condition required before any differential, gradient, restoring response, or motion can exist.

---

Definition

Let the One-Wave field be

[
\psi(x,t),
]

where \psi represents the local field state.

Let the reference ground be

[
\psi_0.
]

A displacement is any local field state that differs from the reference ground.

Mathematically,

[
\boxed{\psi(x,t)\neq\psi_0.}
]

---

Differential

Define displacement from ground as

[
\boxed{x=\psi-\psi_0.}
]

Properties:

If

[
\psi=\psi_0,
]

then

[
x=0.
]

If

[
\psi\neq\psi_0,
]

then

[
x\neq0.
]

---

Immediate Logical Consequence

By definition,

[
\psi\neq\psi_0
]

implies

[
x=\psi-\psi_0.
]

Therefore,

[
\boxed{\text{Displacement}\Rightarrow\text{Differential}.}
]

---

Interpretation

Displacement is not motion.

It is the creation of a local imbalance relative to the reference ground.

Without displacement there is no differential.

Without a differential there is no restoring response.

---

Assumptions

- A reference ground exists.
- The field is continuous enough to define a local state.
- Local field values are comparable with the reference ground.
- Displacement is measured relative to Ground / Zero.

---

Candidate Experiment

Objective

Determine whether a measurable local displacement from the reference ground produces the predicted downstream behavior.

Procedure

1. Establish a reference ground.
2. Produce a controlled local displacement.
3. Measure the resulting differential.
4. Verify that downstream functions depend only upon the measured displacement.

---

Dependencies

Core Functions

- Ground / Zero

Downstream Functions

- Differential
- Gradient
- Restoring Response
- Local Stability
- Bounded Motion

---

Green Audit Result

This node establishes displacement as the first measurable departure from the reference ground.

It defines the mathematical quantity upon which all later differential-based functions depend.

---

Final Green Lock

[
\boxed{x=\psi-\psi_0}
]

[
\boxed{\text{Displacement}\Rightarrow\text{Differential}}
]

[
\boxed{\text{No Displacement}\Rightarrow\text{No Differential}}
]
---

Function Node

Function: Differential

Status: 🟢 Green

---

Purpose

Differential measures the local difference produced by displacement.

It is the mathematical quantity that allows comparison between field states and provides the foundation for gradient and all subsequent spatial analysis.

---

Definition

Let the field state be

[
\psi.
]

Let the reference ground be

[
\psi_0.
]

The local differential is defined as

[
\boxed{\Delta\psi=\psi-\psi_0.}
]

Equivalently,

[
\boxed{\Delta\psi=x,}
]

where

[
x=\psi-\psi_0
]

is the displacement from Ground / Zero.

---

Properties

If

[
\psi=\psi_0,
]

then

[
\Delta\psi=0.
]

If

[
\psi\neq\psi_0,
]

then

[
\Delta\psi\neq0.
]

The magnitude of the differential measures the departure from the reference ground.

---

Immediate Logical Consequence

Since

[
\Delta\psi=\psi-\psi_0,
]

every displacement produces a differential.

Therefore,

[
\boxed{\text{Differential}\Rightarrow\text{Gradient}.}
]

---

Interpretation

The differential measures how much a field differs from its reference ground.

By itself, it does not describe direction or motion.

Those properties emerge in later functions.

---

Assumptions

- Ground / Zero has been established.
- Displacement is defined relative to the reference ground.
- Field values are directly comparable.
- The differential is evaluated at a single location.

---

Candidate Experiment

Objective

Determine whether measured field differences correspond to predicted displacement.

Procedure

1. Establish the reference ground.
2. Produce controlled displacements.
3. Measure the resulting differential.
4. Compare measured values with predicted values.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement

Downstream Functions

- Gradient
- Restoring Response
- Pressure Response

---

Green Audit Result

This node establishes the differential as the mathematical measure of displacement from the reference ground.

It provides the quantity from which spatial variation is computed.

---
[
\boxed{\Delta\psi=\psi-\psi_0}
]

Final Green Lock

---

Function Node

Function: Gradient

Status: 🟢 Green

---

Purpose

Gradient describes how the field changes from one location to another.

While Differential measures the amount of local displacement, Gradient measures how that displacement varies across space.

---

Definition

Let the One-Wave field be

[
\psi(x,t).
]

The spatial gradient is defined as

[
\boxed{\nabla\psi.}
]

The gradient measures the spatial rate of change of the field.

---

Mathematics

If

[
\nabla\psi=0,
]

the field is locally uniform.

If

[
\nabla\psi\neq0,
]

the field contains a spatial imbalance.

---

Immediate Logical Consequence

A nonzero gradient represents unresolved spatial imbalance.

Therefore,

[
\boxed{\text{Gradient}\Rightarrow\text{Restoring Response}.}
]

---

Interpretation

The gradient is not a force.

It is a mathematical description of spatial imbalance.

Later functions determine how the field responds to that imbalance.

---

Assumptions

- Ground / Zero has been established.
- Differential is well-defined.
- The field is continuous enough for spatial derivatives to exist.
- Spatial comparisons are made within the same reference frame.

---

Candidate Experiment

Objective

Measure whether spatial field differences produce the predicted restoring response.

Procedure

1. Establish the reference ground.
2. Produce controlled spatial displacement.
3. Measure the spatial gradient.
4. Compare the measured gradient with the resulting field response.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Differential

Downstream Functions

- Restoring Response
- Pressure Response
- Local Stability

---

Green Audit Result

This node establishes Gradient as the mathematical measure of spatial imbalance.

It does not define the field's response to that imbalance; that relationship is established by the Restoring Response function.
[
\boxed{\nabla\psi}
]

[
\boxed{\nabla\psi=0\Rightarrow\text{Local Uniformity}}
]

[
\boxed{\nabla\psi\neq0\Rightarrow\text{Spatial Imbalance}}
]

[
\boxed{\text{Gradient}\Rightarrow\text{Restoring Response}}
]
[
\boxed{\Delta\psi=x}
]

[
\boxed{\text{Differential}\Rightarrow\text{Gradient}}
]
---

Final Green Lock


---

Function Node

Function: Pressure Response

Status: 🟢 Green

---

Purpose

Pressure Response describes how the field responds to spatial curvature.

While Restoring Response reacts to first-order spatial imbalance (Gradient), Pressure Response reacts to second-order spatial imbalance (Curvature).

---

Definition

Let the One-Wave field be

[
\psi.
]

Let the field curvature be

[
\boxed{\nabla^2\psi.}
]

The current One-Wave working postulate defines Pressure Response as

[
\boxed{P_{OW}=-c^2\nabla^2\psi}
]

where

[
c^2>0
]

is the proportional curvature-response coefficient.

---

Mathematics

If

[
\nabla^2\psi=0,
]

then

[
P_{OW}=0.
]

If

[
\nabla^2\psi\neq0,
]

then

[
P_{OW}\neq0
]

according to the current working postulate.

---

Proof

Assume field curvature exists:

[
\nabla^2\psi\neq0.
]

Using the current pressure-response postulate,

[
P_{OW}=-c^2\nabla^2\psi,
]

with

[
c^2>0,
]

therefore

[
P_{OW}\neq0.
]

Hence,

[
\boxed{\text{Curvature}\Rightarrow\text{Pressure Response}.}
]

---

Working Postulate

The negative sign is presently treated as a working postulate because it produces a response opposing unresolved curvature.

Alternative pressure-response laws remain open for future mathematical derivation and experimental testing.

---

Assumptions

- Field curvature is represented by

[
\nabla^2\psi.
]

- Pressure Response exists.
- The response is presently assumed proportional to curvature.
- The proportionality constant satisfies

[
c^2>0.
]

- The negative sign is a working postulate rather than a completed derivation.

---

Candidate Experiment

Objective

Determine whether the measured pressure response is proportional to field curvature.

Procedure

1. Produce controlled field curvature.
2. Measure the resulting pressure response.
3. Compare the measured response with the predicted response.
4. Determine whether the proportional curvature-response model accurately describes the observations.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Differential
- Gradient
- Restoring Response

Downstream Functions

- Local Stability
- Bounded Motion
- Oscillation

---

Green Audit Result

The mathematical relationship has been stated as a working postulate.

The proof is internally consistent under its stated assumptions.

The origin of the pressure-response equation, the behavior of the proportionality constant, and experimental validation remain open for future audit.

---

Final Green Lock

[
\boxed{\text{Curvature}\Rightarrow\text{Pressure Response}}
]

[
\boxed{P_{OW}=-c^2\nabla^2\psi}
]

under the current One-Wave working postulate.
---

Function Node

Function: Local Stability

Status: 🟢 Green

---

Purpose

Local Stability describes the tendency of a displaced field state to return toward its local ground.

It establishes local attraction to equilibrium.

It does not claim global bounded motion.

---

Definition

Let the field state be

[
\psi.
]

Let the reference ground be

[
\psi_0.
]

Define displacement from ground as

[
\boxed{x=\psi-\psi_0.}
]

A state is locally stable when sufficiently small displacements produce a restoring response directed back toward the reference ground.

---

Mathematics

Let the restoring response be

[
F_{OW}=-\mathcal{A}(x).
]

A local restoring condition is

[
xF_{OW}<0.
]

Substituting the restoring response gives

[
x[-\mathcal{A}(x)]<0,
]

or equivalently,

[
\boxed{x\mathcal{A}(x)>0.}
]

This condition guarantees that the restoring response opposes small displacement.

---

Proof

Assume

[
x\neq0.
]

Assume the restoring response

[
F_{OW}=-\mathcal{A}(x).
]

If

[
x\mathcal{A}(x)>0,
]

then

[
xF_{OW}<0.
]

Therefore the restoring response always points toward the local ground.

Hence,

[
\boxed{\text{Restoring Response tied to Ground}\Rightarrow\text{Local Stability}.}
]

---

Ground Rule

Local Stability requires a defined reference ground.

Without

[
\psi_0,
]

displacement

[
x=\psi-\psi_0
]

cannot be defined.

Therefore,

[
\boxed{\text{No Ground}\Rightarrow\text{No Local Stability}.}
]

---

Boundary to Bounded Motion

Local Stability is not equivalent to Bounded Motion.

This node establishes only local attraction toward the reference ground.

Bounded Motion additionally requires the mode to remain confined within a stable region.

Therefore,

[
\boxed{\text{Local Stability}\neq\text{Bounded Motion}.}
]

---

Assumptions

- A Ground / Zero reference state exists.
- Displacement is measured relative to ground.
- Restoring Response opposes displacement.
- The restoring-response operator satisfies the local return condition.
- Local Stability does not imply global boundedness.

---

Candidate Experiment

Objective

Determine whether small displacements return toward the local ground.

Procedure

1. Establish the reference ground.
2. Produce small positive and negative displacements.
3. Measure the restoring response.
4. Verify that

[
xF_{OW}<0.
]

5. Determine whether the response consistently returns toward the reference ground.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Restoring Response

Downstream Functions

- Bounded Motion
- Inertial Memory
- Oscillation

---

Green Audit Result

The mathematical condition for Local Stability has been established:

[
xF_{OW}<0.
]

This node intentionally stops at local attraction and does not claim global bounded motion.

---

Final Green Lock

[
\boxed{\text{Restoring Response tied to Ground}\Rightarrow\text{Local Stability}}
]

[
\boxed{xF_{OW}<0}
]

[
\boxed{\text{No Ground}\Rightarrow\text{No Local Stability}}
]

---

Function Node

Function: Bounded Motion

Status: 🟢 Green

---

Purpose

Bounded Motion describes motion that remains confined around a defined reference ground rather than escaping indefinitely.

It establishes the conditions under which motion remains within a finite region.

It does not, by itself, establish oscillation.

---

Definition

Let displacement from ground be

[
x=\psi-\psi_0.
]

Assume the restoring response

[
F_{OW}=-\mathcal{A}(x),
]

where

[
\mathcal{A}(x)
]

is the restoring-response function.

A mode is bounded if its motion remains confined within a finite stable region surrounding the reference ground.

---

Mathematics

If

[
x\mathcal{A}(x)>0,
]

then

[
xF_{OW}<0,
]

meaning the restoring response always points toward the reference ground.

This establishes Local Stability.

If the restoring response continues to oppose displacement throughout the stable region occupied by the mode, then the motion remains confined within that region.

---

Proof

Assume a displaced mode

[
x\neq0.
]

Assume the restoring response

[
F_{OW}=-\mathcal{A}(x).
]

If

[
x\mathcal{A}(x)>0,
]

then

[
xF_{OW}<0.
]

Therefore the restoring response always acts toward the reference ground.

Provided the restoring response remains effective throughout the stable region occupied by the mode, the motion remains confined.

Hence,

[
\boxed{\text{Restoring Response}\Rightarrow\text{Bounded Motion}}
]

under the stated assumptions.

---

Boundary to Oscillation

Bounded Motion is not equivalent to Oscillation.

This node establishes only that motion remains confined.

Oscillation additionally requires successful ground crossing through Inertial Memory.

Therefore,

[
\boxed{\text{Bounded Motion}\not\Rightarrow\text{Oscillation}.}
]

See:

→ Function: Oscillation

---

Future Boundary

Local Stability establishes attraction toward the reference ground.

Bounded Motion additionally requires that the mode remain within a stable basin.

A future function will define the escape condition,

[
E_{mode}<E_{escape},
]

where

[
E_{escape}
]

remains undefined at this stage.

---

Assumptions

- A Ground / Zero reference state exists.
- Displacement is measured relative to ground.
- Restoring Response opposes displacement.
- The restoring response remains effective throughout the stable basin occupied by the mode.
- No external influence overwhelms the restoring response.

---

Candidate Experiment

Objective

Determine whether motion remains bounded under the restoring-response condition.

Procedure

1. Establish the reference ground.
2. Produce controlled displacement.
3. Measure the restoring response.
4. Observe whether the motion remains confined or escapes.
5. Identify the limits of the stable basin.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Differential
- Gradient
- Restoring Response
- Local Stability

Downstream Functions

- Inertial Memory
- Oscillation

---

Green Audit Result

The proof establishes that a restoring response directed toward the reference ground produces bounded motion under the stated assumptions.

This node intentionally stops before oscillation.

Questions concerning escape energy, ground crossing, overshoot, inertial carry, and repeated cycles are deferred to later functions.

---

Final Green Lock

[
\boxed{\text{Restoring Response}\Rightarrow\text{Bounded Motion}}
]

under the stated assumptions.

[
\boxed{\text{Bounded Motion}\not\Rightarrow\text{Oscillation}}
]

[
\boxed{E_{mode}<E_{escape}\ \text{(future definition)}}
]
---

Function Node

Function: Inertial Memory

Status: 🟡 Yellow

---

Purpose

Inertial Memory describes the mechanism by which a recursive field carries motion information from one update into the next.

Unlike simple state memory, Inertial Memory preserves the previous state change and allows that change to influence future evolution.

---

Definition

Let the One-Wave recursive update rule be

[
\psi_i^{,n+1}

\psi_i^{,n}
+
(1-\gamma)(\psi_i^{,n}-\psi_i^{,n-1})
+
\beta(\langle\psi_j^{,n}\rangle-\psi_i^{,n}).
]

Define the previous state change as

[
\Delta\psi_n

\psi_n-\psi_{n-1}.
]

The term

[
\boxed{(1-\gamma)\Delta\psi_n}
]

is the inertial-memory contribution carried into the next update.

---

Mathematics

Measure displacement from a common reference ground

[
x_n=\psi_n-\psi_0.
]

If

[
\boxed{\psi_{0,n}=\psi_{0,n-1},}
]

then

[
\Delta x_n

x_n-x_{n-1}

\psi_n-\psi_{n-1}

\Delta\psi_n.
]

The shared reference ground therefore cancels, preserving the previous state change without introducing artificial ground drift.

---

Proof

Assume the recursive update rule

[
\psi_i^{,n+1}

\psi_i^{,n}
+
(1-\gamma)(\psi_i^{,n}-\psi_i^{,n-1})
+
\beta(\langle\psi_j^{,n}\rangle-\psi_i^{,n}).
]

The term

[
(1-\gamma)(\psi_i^{,n}-\psi_i^{,n-1})
]

explicitly carries the previous state change into the next update.

Since that previous motion contributes directly to future evolution,

[
\boxed{(1-\gamma)\Delta\psi_n
\Rightarrow
\text{Inertial Memory}.}
]

---

Hidden Assumptions

Shared Ground

Both recursive states are referenced to the same ground.

[
\boxed{\psi_{0,n}=\psi_{0,n-1}.}
]

Ground drift remains the subject of the Ground / Zero function.

Memory Depth

The current update rule uses two-state memory to carry motion information.

Whether deeper memory contributes additional inertial behavior remains unresolved.

Memory Persistence

The parameter

[
\gamma
]

controls inertial-memory persistence.

Whether

[
\gamma
]

is constant, state-dependent, or ultimately generalized into an operator remains an open question.

Neighbor Coupling

The current update rule includes local-neighborhood coupling through

[
\beta(\langle\psi_j^{,n}\rangle-\psi_i^{,n}).
]

Whether longer-range coupling also contributes to inertial memory remains unresolved.

---

Candidate Experiment

Objective

Determine how recursive memory contributes to inertial behavior.

Procedure

1. Compare one-step and two-step recursive update rules.
2. Vary

[
\gamma.
]

3. Measure:
   - overshoot,
   - damping,
   - oscillation,
   - persistence.
4. Determine the minimum memory depth required to reproduce observed behavior.

---

Dependencies

Core Functions

- Ground / Zero
- Recursion

Supporting Functions

- Prediction

---

Yellow Audit Result

The recursive update rule contains an explicit carry-forward mechanism,

[
\boxed{(1-\gamma)\Delta\psi_n.}
]

The remaining audit questions concern memory depth, memory persistence, neighbor coupling, and possible operator generalization of

[
\gamma.
]

---

Final Yellow Lock

[
\boxed{(1-\gamma)\Delta\psi_n
\Rightarrow
\text{Inertial Memory}}
]

[
\boxed{\text{Two States}+\text{One Shared Ground}+\text{No Ground Drift}}
]

under the current One-Wave recursive update rule.
---

Function Node

Function: Oscillation

Status: 🟢 Green
Yellow Audit: Open

---

Purpose

Oscillation describes repeated motion about a shared reference ground.

It occurs when bounded motion and inertial memory combine so that a mode repeatedly crosses the reference ground rather than simply returning to it.

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

Oscillation is repeated crossing of the shared reference ground produced by the interaction of bounded motion, restoring response, and inertial memory.

---

Mathematics

Bounded Motion confines the mode to a finite stable region around the reference ground.

Restoring Response always points toward the reference ground.

Inertial Memory carries the previous state change into the next update.

At the reference ground,

[
x=0,
]

the restoring response momentarily vanishes because there is no displacement.

Whether the mode crosses the ground therefore depends upon the carried motion

[
(1-\gamma)\Delta\psi_n.
]

If sufficient motion remains, the mode crosses the reference ground and enters the opposite side of the restoring field.

The restoring response then reverses relative to the new displacement and again points toward the reference ground.

Repeated ground crossings produce oscillation.

---

Proof

Assume:

- Bounded Motion has been established.
- Restoring Response points toward the reference ground.
- Inertial Memory carries previous motion through

[
(1-\gamma)\Delta\psi_n.
]

If the carried motion remains sufficient for the mode to cross the shared ground, then the mode overshoots the reference ground.

After crossing, displacement changes sign.

The restoring response again points toward the reference ground.

Repeated ground crossings therefore produce oscillation.

Hence,

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

If inertial memory decays before the mode crosses the reference ground, the mode returns toward equilibrium without overshooting.

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

The current crossing mechanism is

[
(1-\gamma)\Delta\psi_n.
]

The exact inequality separating oscillation from non-oscillatory return has not yet been derived.

This remains the primary Yellow audit target.

---

Assumptions

- Ground / Zero exists.
- Bounded Motion has been established.
- Restoring Response points toward the reference ground.
- Inertial Memory carries previous motion.
- Oscillation requires successful ground crossing.
- This Green node treats

[
\psi
]

as a scalar field.

- Multi-component oscillation and projection consistency remain open for future audit.

---

Candidate Experiment

Objective

Determine the conditions required for repeated ground crossing.

Procedure

1. Generate bounded motion.
2. Vary

[
\gamma.
]

3. Measure:
   
   - first ground crossing,
   - overshoot,
   - repeated crossings,
   - decay,
   - instability.

4. Identify the boundary separating:
   
   - non-oscillatory return,
   - damped oscillation,
   - sustained oscillation,
   - unstable growth.

---

Dependencies

Core Functions

- Ground / Zero
- Bounded Motion
- Inertial Memory

Supporting Functions

- Restoring Response
- Prediction

---

Green Audit Result

This node establishes that oscillation is not implied by bounded motion alone.

Oscillation requires successful ground crossing produced by the interaction of bounded motion and inertial memory.

The exact mathematical crossing condition remains open for Yellow audit.

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
\text{Non\text{-}Oscillatory Return}.
}
]
---

Function Node

Function: Recursion

Status: 🟡 Yellow

---

Purpose

Recursion describes a system whose future state is produced by feeding previous states back into the update rule.

Memory alone is not recursion.

A system may store previous states without using them.

Recursion requires both memory and a feedback rule.

---

Definition

Let the One-Wave field state at step

[
n
]

be

[
\psi_n.
]

A recursive update rule has the form

[
\boxed{\psi_{n+1}=f(\psi_n,\psi_{n-1}).}
]

More generally,

[
\psi_{n+1}

f(\psi_n,\psi_{n-1},\psi_{n-2},\ldots).
]

---

Mathematics

A one-step update has the form

[
\psi_{n+1}=f(\psi_n).
]

A two-step recursive update has the form

[
\psi_{n+1}=f(\psi_n,\psi_{n-1}).
]

A deeper-memory update has the form

[
\psi_{n+1}

f(\psi_n,\psi_{n-1},\psi_{n-2},\ldots).
]

The difference

[
\Delta\psi_n=\psi_n-\psi_{n-1}
]

provides the motion information used by the current recursive update rule.

---

Proof

Assume previous states are retained:

[
\psi_n,\psi_{n-1}.
]

Assume the update rule uses those retained states:

[
\psi_{n+1}

f(\psi_n,\psi_{n-1}).
]

Previous outputs therefore become inputs to future evolution.

Hence,

[
\boxed{
\text{Memory}
+
\text{Feedback Rule}
\Rightarrow
\text{Recursion}.
}
]

Oscillation may arise from recursion, but recursion does not require oscillation.

---

Locality Rule

The current One-Wave update rule includes local-neighborhood coupling through

[
\beta(\langle\psi_j^n\rangle-\psi_i^n).
]

Recursion is therefore not purely local.

Whether longer-range coupling contributes remains an open question.

---

Inertial Memory Link

The current recursive update rule naturally supports Inertial Memory through the two-state difference

[
\Delta\psi_n=\psi_n-\psi_{n-1}.
]

Whether deeper memory contributes additional inertial behavior remains unresolved.

---

Assumptions

- Previous field states can be retained.
- A feedback rule uses previous states.
- The update rule may have finite or deeper memory.
- Local-neighborhood coupling exists.
- Longer-range coupling remains unresolved.
- Oscillation is not required for recursion.

---

Candidate Experiment

Objective

Determine the memory depth required to reproduce observed One-Wave behavior.

Procedure

1. Test one-step recursive updates.
2. Test two-step recursive updates.
3. Test deeper-memory recursive updates.
4. Compare:
   - stability,
   - convergence,
   - oscillation,
   - damping,
   - propagation.
5. Determine whether local-neighborhood coupling alone is sufficient.

---

Dependencies

Core Functions

- Inertial Memory

Supporting Functions

- Prediction

Downstream Functions

- Persistent Mode

---

Yellow Audit Result

Recursion requires both retained memory and a feedback rule.

The remaining audit questions concern memory depth and the range of recursive coupling.

---

Final Yellow Lock

[
\boxed{
\text{Memory}
+
\text{Feedback Rule}
\Rightarrow
\text{Recursion}
}
]

[
\boxed{
\psi_{n+1}

f(\psi_n,\psi_{n-1})
}
]

[
\boxed{
\Delta\psi_n

\psi_n-\psi_{n-1}
}
]---

Function Node

Function: Persistent Mode

Status: 🟢 Green

---

Purpose

Persistent Mode describes a stable recursive pattern that maintains its identity through successive updates.

Unlike a transient disturbance, a persistent mode survives because the recursive update continually reconstructs the pattern rather than allowing it to decay immediately.

---

Definition

Let the recursive field update be

[
\psi_{n+1}=f(\psi_n,\psi_{n-1},\ldots).
]

A persistent mode is a bounded recursive pattern whose identity is preserved through successive updates.

Persistence is an emergent property of the recursive process rather than a static state.

---

Mathematics

A persistent mode satisfies the condition that its defining structure remains recognizable across recursive updates,

[
\boxed{
\psi_{n+1}\sim\psi_n,
}
]

where "\sim" denotes preservation of the mode's identity rather than exact numerical equality.

The pattern may evolve while remaining the same identifiable mode.

---

Proof

Assume:

- Bounded Motion confines the mode.
- Inertial Memory carries previous motion.
- Recursion feeds previous states into future updates.

If each recursive update reconstructs the same bounded pattern, then the mode persists through time.

Therefore,

[
\boxed{
\text{Bounded Motion}
+
\text{Inertial Memory}
+
\text{Recursion}
\Rightarrow
\text{Persistent Mode}.
}
]

---

Interpretation

Persistence does not require a perfectly static field.

The field may oscillate, deform slightly, or exchange energy while maintaining its overall identity.

A persistent mode is therefore defined by continuity of structure rather than exact equality at every update.

---

Assumptions

- Ground / Zero exists.
- Motion remains bounded.
- Inertial Memory is present.
- Recursive updating continues.
- The recursive process reconstructs the mode rather than destroying it.

---

Candidate Experiment

Objective

Determine whether a recursively updated bounded mode preserves its identity over time.

Procedure

1. Generate a bounded recursive mode.
2. Allow repeated recursive updates.
3. Measure structural similarity between successive states.
4. Determine whether the mode persists, decays, or transforms into another stable mode.

---

Dependencies

Core Functions

- Bounded Motion
- Inertial Memory
- Oscillation
- Recursion

Downstream Functions

- Book 1: Micro Objects
- Quark
- Proton
- Atom
- All higher persistent structures

---

Green Audit Result

Persistent Mode is established as the first stable recursive structure produced by the interaction of bounded motion, inertial memory, and recursion.

It serves as the bridge between the foundational function library and the object-based books that follow.

---

Final Green Lock

[
\boxed{
\text{Bounded Motion}
+
\text{Inertial Memory}
+
\text{Recursion}
\Rightarrow
\text{Persistent Mode}.
}
]

[
\boxed{
\text{Persistent Mode}
\Rightarrow
\text{Stable Recursive Structure}.
}
]
Looking Ahead

Appendix Red A established the core functions of the One-Wave framework.

The remaining appendices expand these foundational functions into broader systems and relationships before the books apply them to physical structures.

With the functional language established, the next appendix builds upon this foundation and extends the framework into the next stage of development.
