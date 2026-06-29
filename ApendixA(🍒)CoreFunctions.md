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

$$
\psi
$$

Let the reference ground be

$$
\psi_0.
$$

Displacement from ground is defined as

$$
\boxed{x=\psi-\psi_0.}
$$

This definition is meaningful only if the reference ground is well-defined.

---

Same-Ground Rule

When comparing two successive field states,

$$
\psi_n
\quad\text{and}\quad
\psi_{n-1},
$$

both must be measured relative to the same reference ground:

$$
\boxed{\psi_{0,n}=\psi_{0,n-1}.}
$$

Under this assumption,

$$
\Delta x_n
=
x_n-x_{n-1}
=
(\psi_n-\psi_0)-(\psi_{n-1}-\psi_0)
=
\psi_n-\psi_{n-1}
=
\Delta\psi_n.
$$

This establishes that the common ground cancels when successive states share the same reference.

---

No Ground, No Displacement

Without a defined reference ground,

$$
x=\psi-\psi_0
$$

cannot be evaluated.

Therefore,

$$
\boxed{\text{No Ground} \Rightarrow \text{No Displacement}.}
$$

---

Open Question 1: Geometry Invariance

Does the reference ground remain the same under compressed and expressed representations?

$$
\boxed{\psi_{0,2D}\ ?=\ \psi_{0,3D}.}
$$

This question remains open and is inherited by Projection (see Blocker 0: Projection–Gradient Consistency).

---

Open Question 2: Time Invariance

Does the reference ground remain constant through recursive updates?

$$
\boxed{\psi_{0,n}=\psi_{0,n-1}}
$$

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
- Restoring Response
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

$$
\boxed{x=\psi-\psi_0}
$$

$$
\boxed{\psi_{0,n}=\psi_{0,n-1}\ \text{(assumed for successive comparisons)}}
$$

$$
\boxed{\psi_{0,2D}\ ?=\ \psi_{0,3D}}
$$

$$
\boxed{\text{No Ground} \Rightarrow \text{No Displacement}}
$$

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

$$
\psi(x,t),
$$

where \psi represents the local field state.

Let the reference ground be

$$
\psi_0.
$$

A displacement is any local field state that differs from the reference ground.

Mathematically,

$$
\boxed{\psi(x,t)\neq\psi_0.}
$$

---

Differential

Define displacement from ground as

$$
\boxed{x=\psi-\psi_0.}
$$

Properties:

If

$$
\psi=\psi_0,
$$

then

$$
x=0.
$$

If

$$
\psi\neq\psi_0,
$$

then

$$
x\neq0.
$$

---

Immediate Logical Consequence

By definition,

$$
\psi\neq\psi_0
$$

implies

$$
x=\psi-\psi_0.
$$

Therefore,

$$
\boxed{\text{Displacement}\Rightarrow\text{Differential}.}
$$

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

$$
\boxed{x=\psi-\psi_0}
$$

$$
\boxed{\text{Displacement}\Rightarrow\text{Differential}}
$$

$$
\boxed{\text{No Displacement}\Rightarrow\text{No Differential}}
$$

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

$$
\psi.
$$

Let the reference ground be

$$
\psi_0.
$$

The local differential is defined as

$$
\boxed{\Delta\psi=\psi-\psi_0.}
$$

Equivalently,

$$
\boxed{\Delta\psi=x,}
$$

where

$$
x=\psi-\psi_0
$$

is the displacement from Ground / Zero.

---

Properties

If

$$
\psi=\psi_0,
$$

then

$$
\Delta\psi=0.
$$

If

$$
\psi\neq\psi_0,
$$

then

$$
\Delta\psi\neq0.
$$

The magnitude of the differential measures the departure from the reference ground.

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

This node defines the differential itself. The logical step from Differential to Gradient is established in the Gradient node below, and is stated there as a derivation rather than as a restatement of definitions, to avoid the circularity of defining Gradient and proving its own definition in the same breath.

---

Final Green Lock

$$
\boxed{\Delta\psi=\psi-\psi_0}
$$

$$
\boxed{\Delta\psi=x}
$$

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

$$
\psi(x,t).
$$

The spatial gradient is defined as the spatial rate of change of the field:

$$
\boxed{\nabla\psi.}
$$

This definition states what the gradient measures. It does not, by itself, establish that a differential produces a gradient — that derivation follows below.

---

Mathematics

If

$$
\nabla\psi=0,
$$

the field is locally uniform.

If

$$
\nabla\psi\neq0,
$$

the field contains a spatial imbalance.

---

Proof: Differential Creates Gradient

Assume a differential exists across space, meaning the field takes different values at two locations:

$$
\psi(x_1)\neq\psi(x_2).
$$

A spatial difference between locations means the field changes with position.

By the definition of Gradient as the spatial rate of change of the field, this spatial change is represented by

$$
\nabla\psi\neq0.
$$

Therefore,

$$
\boxed{\text{Differential}\Rightarrow\text{Gradient}.}
$$

This derives the relationship from the existence of a spatial difference, rather than restating the definition of Gradient as if it were itself a proof.

---

Immediate Logical Consequence

A nonzero gradient represents unresolved spatial imbalance.

Therefore,

$$
\boxed{\text{Gradient}\Rightarrow\text{Restoring Response}.}
$$

(See Function: Restoring Response for the response operator that acts on this imbalance, including the Blocker 0 caveat below on which gradient is meant.)

---

Interpretation

The gradient is not a force.

It is a mathematical description of spatial imbalance.

Later functions determine how the field responds to that imbalance.

---

Blocker 0: Projection–Gradient Consistency (Open)

The framework defines both a full expressed state \psi_{3D} and a compressed projection \psi_{2D}=P_{2D}(\psi_{3D}) (see Function: Projection). This means two gradients are possible:

$$
\nabla\psi_{3D}
\quad\text{and}\quad
\nabla\psi_{2D}.
$$

This node does not yet specify which gradient is meant whenever \nabla\psi appears above. The open mathematical question is whether projection commutes with the gradient operator:

$$
P_{2D}(\nabla\psi_{3D})
\stackrel{?}{=}
\nabla(P_{2D}\psi_{3D}).
$$

This is evaluated using the Hungry Gremlin test defined in the Projection node, with G=\nabla. The current working understanding (pending the Intra-State Coupling node) is that commutation fails if the six state components (E,C,F,B,U,D) are cross-coupled; it holds if they evolve separably. Until resolved, any use of \nabla\psi in this node or downstream should be understood as provisional and geometry-unspecified.

---

Assumptions

- Ground / Zero has been established.
- Differential is well-defined.
- The field is continuous enough for spatial derivatives to exist.
- Spatial comparisons are made within the same reference frame.
- Which gradient (\nabla\psi_{2D} or \nabla\psi_{3D}) is intended remains open (Blocker 0).

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

Supporting Functions

- Projection (Blocker 0)

Downstream Functions

- Restoring Response
- Pressure Response
- Local Stability

---

Green Audit Result

This node establishes Gradient as the mathematical measure of spatial imbalance, derived from Differential rather than asserted as a restatement of its own definition.

It does not define the field's response to that imbalance; that relationship is established by the Restoring Response function.

It does not yet resolve which geometry (2D or 3D) the gradient operator is being applied to; that is Blocker 0, inherited from Projection.

---

Final Green Lock

$$
\boxed{\nabla\psi}
$$

$$
\boxed{\nabla\psi=0\Rightarrow\text{Local Uniformity}}
$$

$$
\boxed{\nabla\psi\neq0\Rightarrow\text{Spatial Imbalance}}
$$

$$
\boxed{\text{Differential}\Rightarrow\text{Gradient}}
$$

$$
\boxed{\text{Gradient}\Rightarrow\text{Restoring Response}}
$$

$$
\boxed{\text{Blocker 0: which geometry's gradient is meant remains open}}
$$

---

Function Node

Function: Restoring Response

Status: 🟡 Yellow

---

Purpose

A restoring response is the field's response to imbalance.

A gradient indicates that the field state is not spatially uniform.

Restoring Response defines the rule by which the field reacts to that imbalance.

---

Definition

Let the One-Wave field state be:

$$
\psi
$$

Let the field gradient be:

$$
\nabla\psi
$$

The earlier Green form was:

$$
F_{\text{OW}}=-\alpha\nabla\psi
$$

where:

$$
\alpha>0
$$

This Yellow revision replaces the scalar coefficient with a response operator:

$$
\boxed{
F_{\text{OW}}=-\mathcal{A}(\nabla\psi)
}
$$

where:

$$
\mathcal{A}
$$

is the One-Wave restoring-response operator.

---

Why the Revision Is Needed

The scalar form:

$$
F_{\text{OW}}=-\alpha\nabla\psi
$$

assumes one universal response coefficient.

That is too narrow.

A field imbalance may appear through different channels, including:

- compression / density imbalance,
- expression / phase imbalance,
- projection-visible imbalance,
- projection-hidden imbalance.

These may not share the same response coefficient.

Therefore:

$$
\alpha
$$

is promoted to:

$$
\mathcal{A}
$$

a response operator.

---

Mathematics

If:

$$
\nabla\psi=0
$$

then no restoring response is required:

$$
F_{\text{OW}}=0
$$

If:

$$
\nabla\psi\neq0
$$

then the restoring operator may produce a nonzero response:

$$
F_{\text{OW}}=-\mathcal{A}(\nabla\psi)
$$

So:

$$
\nabla\psi\neq0
\Rightarrow
F_{\text{OW}}\neq0
$$

provided:

$$
\mathcal{A}(\nabla\psi)\neq0
$$

---

Proof: Gradient Creates Restoring Response

Assume a spatial imbalance exists:

$$
\nabla\psi\neq0
$$

Define Restoring Response as the field response that acts against unresolved imbalance.

The response is represented by:

$$
F_{\text{OW}}=-\mathcal{A}(\nabla\psi)
$$

If:

$$
\mathcal{A}(\nabla\psi)\neq0
$$

then:

$$
F_{\text{OW}}\neq0
$$

Therefore:

$$
\boxed{
\text{Gradient}
\Rightarrow
\text{Restoring Response}
}
$$

within the stated One-Wave definition of a responsive field.

---

Channel Rule

Restoring Response may have multiple channels.

Compression / Density Channel

A compression imbalance may produce an acoustic-style restoring response. This is the channel that later may connect to density, pressure, compressibility, and sound speed.

Expression / Phase Channel

An expression or phase imbalance may produce a circulation, twist, or dispersion response. This channel should not be collapsed into the same scalar coefficient as compression.

Projection Channel

A projected gradient may produce only a visible readout response. Hidden components may still contribute through the full expressed state. This channel inherits the open Blocker 0 status from Gradient and Projection — it is not yet a settled channel like the other two.

---

Current Working Postulate

The negative sign remains a working postulate.

It means the response acts against unresolved imbalance.

Alternative response laws remain open until an experiment is specified once Blockers 0–3 (origin of the equation, linearity, the constant/operator question, and channel separability) are resolved.

---

Candidate Experiment

Objective

Determine whether a measured imbalance produces a restoring response, and whether the response depends on the channel of imbalance.

Procedure

1. Measure the full field gradient signature \nabla\psi without presupposing a channel decomposition.
2. Determine whether the measured signature is classifiable into compression, expression, or projection-visible/hidden channels.
3. Measure the resulting response:

$$
F_{\text{OW}}
$$

4. Test whether the response opposes the imbalance.
5. Compare whether the same coefficient fits all channels or whether separate response behavior is required.

If one scalar coefficient fits all channels, then:

$$
\mathcal{A}\rightarrow\alpha
$$

within the tested regime.

If different channels respond differently, then the operator form is required.

---

Assumptions

- A field gradient can represent imbalance.
- The field can respond to imbalance.
- The response may depend on the imbalance channel.
- The scalar coefficient \alpha is not assumed universal.
- The response operator \mathcal{A} must be characterized by later experiment, simulation, or derivation.
- Projection effects remain inherited from Projection and Blocker 0.
- Which gradient (\nabla\psi_{2D} or \nabla\psi_{3D}) feeds this operator remains open, per Blocker 0.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Differential
- Gradient

Supporting Functions

- Projection (Blocker 0)
- Prediction

---

Yellow Audit Result

Restoring Response reaches Yellow because the scalar assumption has been exposed and replaced by a testable operator form.

The node now points to a concrete experiment:

- measure the gradient signature,
- identify channel,
- measure response,
- test whether one scalar coefficient is sufficient or whether an operator is required.

The node does not yet claim that the full response law has been experimentally validated.

---

Final Yellow Lock

$$
\boxed{
\text{Gradient}\Rightarrow\text{Restoring Response}
}
$$

$$
\boxed{
F_{\text{OW}}=-\mathcal{A}(\nabla\psi)
}
$$

$$
\boxed{
\alpha\rightarrow\mathcal{A}
}
$$

$$
\boxed{
\text{Restoring Response is channel-dependent until proven otherwise.}
}
$$

---

Function Node

Function: Pressure Response

Status: 🟡 Yellow

---

Purpose

Pressure Response describes how the field reacts when imbalance is not only present, but spatially curved.

A gradient shows directional change.

Curvature shows change in the gradient itself.

Pressure Response is the field's distributed reaction to that curvature.

---

Definition

Let the One-Wave field be

$$
\psi.
$$

Curvature is represented by the Laplacian:

$$
\boxed{
\nabla^2\psi
}
$$

Pressure Response is defined as the response produced by field curvature:

$$
\boxed{
P_{\text{OW}}=-\mathcal{C}(\nabla^2\psi)
}
$$

where

$$
\mathcal{C}
$$

is the curvature-response operator.

The earlier Green form was:

$$
P=-c^2\nabla^2\psi
$$

This is now treated as a special scalar case of the operator form.

---

Mathematics

If the field has no curvature:

$$
\nabla^2\psi=0
$$

then no curvature-pressure response is produced:

$$
P_{\text{OW}}=0
$$

If the field has curvature:

$$
\nabla^2\psi\neq0
$$

then pressure response may be nonzero:

$$
P_{\text{OW}}\neq0
$$

provided:

$$
\mathcal{C}(\nabla^2\psi)\neq0
$$

---

Proof: Curvature Creates Pressure Response

Assume field curvature exists:

$$
\nabla^2\psi\neq0
$$

Pressure Response is defined as the field's distributed response to curvature.

Represent that response by:

$$
P_{\text{OW}}=-\mathcal{C}(\nabla^2\psi)
$$

If the curvature-response operator acts nontrivially:

$$
\mathcal{C}(\nabla^2\psi)\neq0
$$

then:

$$
P_{\text{OW}}\neq0
$$

Therefore:

$$
\boxed{
\text{Curvature}
\Rightarrow
\text{Pressure Response}
}
$$

---

Scalar Special Case

If the curvature-response operator reduces to a scalar coefficient, then:

$$
\mathcal{C}(\nabla^2\psi)=c^2\nabla^2\psi
$$

so:

$$
P_{\text{OW}}=-c^2\nabla^2\psi
$$

This gives the earlier Green proof form:

$$
\boxed{
P=-c^2\nabla^2\psi
}
$$

where:

$$
c^2>0
$$

acts as the curvature-pressure response coefficient.

---

Relation to Restoring Response

Restoring Response responds to first spatial imbalance:

$$
F_{\text{OW}}=-\mathcal{A}(\nabla\psi)
$$

Pressure Response responds to curvature of that imbalance:

$$
P_{\text{OW}}=-\mathcal{C}(\nabla^2\psi)
$$

So:

$$
\boxed{
\nabla\psi
\Rightarrow
\text{Restoring Response}
}
$$

and:

$$
\boxed{
\nabla^2\psi
\Rightarrow
\text{Pressure Response}
}
$$

Restoring Response tracks directional imbalance.

Pressure Response tracks distributed curvature imbalance.

Whether \mathcal{C} is independent of \mathcal{A}, or whether \mathcal{C} is \mathcal{A} applied to the gradient of \nabla\psi itself, remains an open structural question.

---

Working Postulate

The negative sign is a working postulate.

It means the pressure response acts against unresolved curvature imbalance.

Alternative pressure laws remain open until future mathematical derivation or experimental validation.

---

Response Channels

Pressure Response may contain multiple channels.

Possible channels include:

- compression / density curvature,
- expression / phase curvature,
- surface or boundary curvature,
- coupling curvature between field components.

These are not assumed to share one universal scalar coefficient.

---

Projection Note

Projection is not a pressure channel.

Projection is an observational layer.

This node inherits Projection–Gradient consistency questions when curvature is computed from projected states.

Specifically, this node must eventually ask whether:

$$
P_{2D}(\nabla^2\psi_{3D})
\stackrel{?}{=}
\nabla^2(P_{2D}\psi_{3D})
$$

until proven.

---

Candidate Experiment

Objective

Determine whether field curvature produces a measurable distributed pressure response, isolated from any concurrent Restoring Response contribution.

Procedure

1. Produce a controlled field shape with measurable curvature.
2. Measure the field curvature:

$$
\nabla^2\psi
$$

3. Measure the distributed response:

$$
P_{\text{OW}}
$$

4. Account for and separate any concurrent contribution from Restoring Response \mathcal{A}(\nabla\psi) acting at the same location, so the two are not confounded.
5. Compare the measured response against the scalar prediction:

$$
P_{\text{OW}}=-c^2\nabla^2\psi
$$

6. Test whether one scalar coefficient:

$$
c^2
$$

fits all measured curvature responses.

7. If one scalar coefficient fails, test whether an operator form is required:

$$
P_{\text{OW}}=-\mathcal{C}(\nabla^2\psi)
$$

---

Assumptions

- Curvature is represented by \nabla^2\psi.
- Field curvature can produce a distributed response.
- The response may oppose curvature imbalance.
- The scalar coefficient c^2 is not assumed universal.
- The curvature-response operator \mathcal{C} must be characterized by experiment, simulation, or later derivation.
- Projection effects remain open when curvature is computed from projected field states.
- The relationship between \mathcal{C} and \mathcal{A} remains open.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Differential
- Gradient
- Restoring Response

Supporting Functions

- Projection
- Prediction

---

Yellow Audit Result

Pressure Response reaches Yellow because the hidden scalar assumption has been exposed.

The original scalar law:

$$
P=-c^2\nabla^2\psi
$$

has been generalized into a testable operator form:

$$
P_{\text{OW}}=-\mathcal{C}(\nabla^2\psi)
$$

The node now points to a concrete experiment:

- create curvature,
- measure curvature,
- measure pressure response,
- separate it from any concurrent Restoring Response contribution,
- test whether scalar c^2 is enough, or whether operator \mathcal{C} is required.

---

Final Yellow Lock

$$
\boxed{
\text{Curvature}
\Rightarrow
\text{Pressure Response}
}
$$

$$
\boxed{
P_{\text{OW}}=-\mathcal{C}(\nabla^2\psi)
}
$$

$$
\boxed{
c^2
\text{ is a possible scalar special case of }
\mathcal{C}
}
$$

$$
\boxed{
\text{Pressure Response is curvature-dependent until proven otherwise.}
}
$$

---

Function Node

Function: Local Stability

Status: 🟡 Yellow

---

Purpose

Local Stability describes a state that returns toward ground after small displacement.

It does not claim that motion is globally bounded.

It only claims that the field has a locally attractive ground state.

---

Definition

Let the field state be

$$
\psi
$$

Let the ground state be

$$
\psi_0
$$

Define displacement from ground:

$$
x=\psi-\psi_0
$$

A state is locally stable when small displacements produce a response back toward ground.

---

Mathematics

Let the restoring response be

$$
F_{OW}=-\mathcal{A}(x)
$$

where

$$
\mathcal{A}
$$

is the restoring-response operator.

A local return condition is:

$$
xF_{OW}<0
$$

For

$$
F_{OW}=-\mathcal{A}(x),
$$

this becomes:

$$
x[-\mathcal{A}(x)]<0,
$$

so:

$$
\boxed{x\mathcal{A}(x)>0.}
$$

---

Energy Form

Define the local potential:

$$
V(x)=\int_0^x \mathcal{A}(s)\,ds
$$

The ground state is locally stable when:

$$
V(0)=0
$$

and for small nonzero displacement:

$$
V(x)>0
\quad
\text{near}
\quad
x=0.
$$

Equivalently, in the scalar linear case:

$$
\mathcal{A}(x)=\alpha x,
\quad \alpha>0,
$$

$$
V(x)=\frac{1}{2}\alpha x^2,
\qquad
\frac{d^2V}{dx^2}=\alpha>0,
$$

so the ground state is a local minimum.

---

Proof: Restoring Response Produces Local Stability

Assume a small displacement from ground:

$$
x\neq0.
$$

Assume the restoring response:

$$
F_{OW}=-\mathcal{A}(x).
$$

If:

$$
x\mathcal{A}(x)>0,
$$

then:

$$
xF_{OW}<0.
$$

This means the response points opposite displacement.

Therefore the field is driven back toward ground.

So:

$$
\boxed{
\text{Restoring Response tied to Ground}
\Rightarrow
\text{Local Stability}
}
$$

---

Ground / Zero Rule

Local Stability requires a defined ground.

Without

$$
\psi_0
$$

there is no displacement

$$
x=\psi-\psi_0
$$

and therefore no meaningful local stability condition.

So:

$$
\boxed{
\text{No Ground, No Local Stability}
}
$$

This node assumes a well-defined ground exists. If 2D compressed and 3D expressed states define different grounds, then displacement must be defined per geometry:

$$
x_{2D}=\psi_{2D}-\psi_{0,2D}
\qquad
x_{3D}=\psi_{3D}-\psi_{0,3D}
$$

(see Ground / Zero, Open Question 1, and Blocker 0).

---

Channel Rule

Local Stability may need to be checked per response channel.

If Restoring Response has multiple channels, then each channel may have its own local potential:

$$
V_i(x)=\int_0^x \mathcal{A}_i(s)\,ds
$$

A mode may be locally stable in one channel and unstable in another.

Therefore, global stability is not assumed from one local channel check.

---

Boundary to Bounded Motion

Local Stability is not the same as Bounded Motion.

Local Stability means:

$$
V(x)>0
\quad\text{near}\quad
x=0.
$$

Bounded Motion requires the mode to remain inside a stable basin.

That requires an additional escape condition:

$$
E_{\text{mode}}<E_{\text{escape}}
$$

where

$$
E_{\text{escape}}
$$

is not yet defined by this node.

Therefore:

$$
\boxed{
\text{Local Stability}\neq\text{Bounded Motion}
}
$$

and:

$$
\boxed{
\text{Local Stability}+E_{\text{mode}}<E_{\text{escape}}\Rightarrow\text{Bounded Motion}
}
$$

---

Assumptions

- A ground state exists.
- Displacement is measured relative to ground.
- The restoring response acts on displacement from ground.
- The local return condition is xF_{OW}<0.
- The potential V(x) is locally defined near ground.
- Local Stability does not imply global boundedness.
- Escape energy is not yet defined.
- Stability may need to be checked per channel rather than assumed global from one channel.

---

Candidate Experiment

Objective

Determine whether a displaced mode returns toward ground for small displacements, accounting for which response channel is being tested.

Procedure

1. Identify a ground state:

$$
\psi_0
$$

2. Create a small displacement:

$$
x=\psi-\psi_0
$$

3. Measure the restoring response, noting which channel (compression, expression, projection-visible) is dominant:

$$
F_{OW}
$$

4. Test whether:

$$
xF_{OW}<0
$$

5. Repeat for small positive and negative displacements.
6. Estimate the local potential:

$$
V(x)=\int_0^x \mathcal{A}(s)\,ds
$$

7. Check whether:

$$
V(x)>0
$$

near

$$
x=0.
$$

If both conditions hold, the ground is locally stable within the tested regime and channel.

---

Dependencies

Core Functions

- Ground / Zero
- Displacement
- Restoring Response

Supporting Functions

- Projection
- Prediction

---

Yellow Audit Result

Local Stability reaches Yellow because the mathematical condition has been defined:

$$
xF_{OW}<0
$$

and the potential condition has been stated:

$$
V(x)>0\quad\text{near}\quad x=0.
$$

The node explicitly avoids claiming full Bounded Motion.

Bounded Motion requires a later escape-energy or stable-basin condition.

---

Final Yellow Lock

$$
\boxed{
\text{Restoring Response tied to Ground}\Rightarrow\text{Local Stability}
}
$$

$$
\boxed{xF_{OW}<0}
$$

$$
\boxed{V(x)>0\text{ near }x=0}
$$

$$
\boxed{\text{No Ground, No Local Stability}}
$$

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

$$
x=\psi-\psi_0.
$$

Assume the restoring response

$$
F_{OW}=-\mathcal{A}(x),
$$

where

$$
\mathcal{A}(x)
$$

is the restoring-response function.

A mode is bounded if its motion remains confined within a finite stable region surrounding the reference ground.

---

Two Cases

Whether \mathcal{A}(x) remains restoring for all x, or only near ground, is not yet settled. The honest Yellow-direction move is to state both cases explicitly rather than assume one.

Case 1: Global Restoring Basin

If \mathcal{A}(x) keeps restoring for all x, then

$$
V(x)=\int_0^x \mathcal{A}(s)\,ds
\;\to\;\infty
\quad\text{as}\quad
|x|\to\infty.
$$

The mode cannot escape with finite energy. Bounded Motion is automatic within the model, with no escape condition required.

Case 2: Local Restoring Basin

If \mathcal{A}(x) restores only near \psi_0, escape becomes possible at some basin edge x_{\text{edge}}. Define

$$
E_{\text{escape}}=V(x_{\text{edge}}).
$$

Then:

$$
\boxed{
\text{Local Stability}+E_{\text{mode}}<E_{\text{escape}}\Rightarrow\text{Bounded Motion}.
}
$$

where

$$
E_{\text{mode}}=K_{\text{motion}}+V(x)
$$

and \(K_{\text{motion}}\) depends on the later Inertial Memory / Motion Energy characterization, not yet fully defined by this node.

---

Asymmetry Note

These two paths are not equally settled. Case 1 is checkable now, directly from whatever explicit form \mathcal{A}(x) eventually takes — it requires no new machinery. Case 2 is checkable only once the basin edge / E_{\text{escape}} definition and the Inertial Memory kinetic term K_{\text{motion}} both exist. Case 2 should not be read as equally actionable as Case 1 until those dependencies are resolved.

---

Mathematics

If

$$
x\mathcal{A}(x)>0,
$$

then

$$
xF_{OW}<0,
$$

meaning the restoring response always points toward the reference ground. This establishes Local Stability.

If the restoring response continues to oppose displacement throughout the stable region occupied by the mode (Case 1), or if the mode's energy remains below the escape energy (Case 2), then the motion remains confined within that region.

---

Proof

Assume a displaced mode

$$
x\neq0.
$$

Assume the restoring response

$$
F_{OW}=-\mathcal{A}(x).
$$

If

$$
x\mathcal{A}(x)>0,
$$

then

$$
xF_{OW}<0.
$$

Therefore the restoring response always acts toward the reference ground.

Provided either Case 1 or Case 2 holds, the motion remains confined.

Hence,

$$
\boxed{\text{Local Stability}+\text{Global Restoring Basin}\Rightarrow\text{Bounded Motion}}
$$

or

$$
\boxed{\text{Local Stability}+E_{\text{mode}}<E_{\text{escape}}\Rightarrow\text{Bounded Motion}}
$$

---

Boundary to Oscillation

Bounded Motion is not equivalent to Oscillation.

This node establishes only that motion remains confined.

Oscillation additionally requires successful ground crossing through Inertial Memory.

Therefore,

$$
\boxed{\text{Bounded Motion}\not\Rightarrow\text{Oscillation}.}
$$

See: Function: Oscillation

---

Assumptions

- A Ground / Zero reference state exists.
- Displacement is measured relative to ground.
- Restoring Response opposes displacement.
- Whether \mathcal{A}(x) is globally or only locally restoring is not yet settled (Case 1 vs Case 2).
- E_{\text{escape}} and K_{\text{motion}} are not yet defined; they are named placeholders pending later nodes.
- No interaction mechanism overwhelms the restoring response.

---

Candidate Experiment

Objective

Determine whether motion remains bounded under the restoring-response condition, and which case (global or local basin) applies.

Procedure

1. Establish the reference ground.
2. Produce controlled displacement.
3. Measure the restoring response across a wide range of x, not just near ground.
4. Determine whether \mathcal{A}(x) remains restoring at large |x| (Case 1) or weakens/reverses (Case 2).
5. If Case 2, identify the basin edge and estimate E_{\text{escape}}.
6. Observe whether the motion remains confined or escapes.

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

The proof establishes that a restoring response directed toward the reference ground produces bounded motion under either of two explicitly stated cases.

This node intentionally stops before oscillation.

Questions concerning escape energy, ground crossing, overshoot, inertial carry, and repeated cycles are deferred to later functions.

---

Final Green Lock

$$
\boxed{\text{Local Stability}+\text{Global Restoring Basin}\Rightarrow\text{Bounded Motion}}
$$

$$
\boxed{\text{Local Stability}+E_{\text{mode}}<E_{\text{escape}}\Rightarrow\text{Bounded Motion}}
$$

$$
\boxed{\text{Bounded Motion}\not\Rightarrow\text{Oscillation}}
$$

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

$$
\psi_i^{n+1}
=
\psi_i^{n}
+
(1-\gamma)(\psi_i^{n}-\psi_i^{n-1})
+
\beta(\langle\psi_j^{n}\rangle-\psi_i^{n}).
$$

Define the previous state change as

$$
\Delta\psi_n
=
\psi_n-\psi_{n-1}.
$$

The term

$$
\boxed{(1-\gamma)\Delta\psi_n}
$$

is the inertial-memory contribution carried into the next update.

---

Mathematics

Measure displacement from a common reference ground

$$
x_n=\psi_n-\psi_0.
$$

If

$$
\boxed{\psi_{0,n}=\psi_{0,n-1},}
$$

then

$$
\Delta x_n
=
x_n-x_{n-1}
=
\psi_n-\psi_{n-1}
=
\Delta\psi_n.
$$

The shared reference ground therefore cancels, preserving the previous state change without introducing artificial ground drift. (See Ground / Zero, Same-Ground Rule.)

---

Proof

Assume the recursive update rule

$$
\psi_i^{n+1}
=
\psi_i^{n}
+
(1-\gamma)(\psi_i^{n}-\psi_i^{n-1})
+
\beta(\langle\psi_j^{n}\rangle-\psi_i^{n}).
$$

The term

$$
(1-\gamma)(\psi_i^{n}-\psi_i^{n-1})
$$

explicitly carries the previous state change into the next update.

Since that previous motion contributes directly to future evolution,

$$
\boxed{(1-\gamma)\Delta\psi_n\Rightarrow\text{Inertial Memory}.}
$$

---

Hidden Assumptions

Shared Ground

Both recursive states are referenced to the same ground.

$$
\boxed{\psi_{0,n}=\psi_{0,n-1}.}
$$

Ground drift remains the subject of the Ground / Zero function.

Memory Depth

The current update rule uses two-state memory — the depth used to carry motion information in this specific update rule, not a proven minimum for inertia in general. A different functional form (e.g. a richer single-state ψ containing a velocity-like component) could in principle encode motion differently. Whether deeper memory contributes additional inertial behavior remains unresolved.

What Is Being Remembered

The update rule remembers the previous state change, \Delta\psi_n, not merely the previous state value. The quantity propagated forward is (1-\gamma)\Delta\psi_n — the field remembers motion, not just history.

Memory Persistence

The parameter \gamma controls inertial-memory persistence.

- \gamma=0: complete carry-forward of the previous state change.
- \gamma=1: no carry-forward of the previous state change.

Whether \gamma is constant, state-dependent, or ultimately generalized into an operator \Gamma (paralleling the \alpha\to\mathcal{A} promotion in Restoring Response) remains an open question. \gamma is the leading candidate for the damping term Γ in the parked oscillation criterion \Gamma^2<4MK.

Neighbor Coupling

The current update rule includes local-neighborhood coupling through

$$
\beta(\langle\psi_j^{n}\rangle-\psi_i^{n}).
$$

This is a separate coupling axis from Intra-State Coupling (which asks whether E,C,F,B,U,D couple to each other within one node). This is inter-node coupling: whether longer-range neighbor coupling also contributes to inertial memory remains unresolved. Both axes are open and should be tracked as siblings.

---

Assumptions

- Previous states are retained.
- The update rule depends upon at least two successive states.
- Motion information is carried through recursive memory.
- Ground is shared across the compared states (inherits Ground / Zero).
- Memory depth as used here reflects the current update rule's structure, not a proven general minimum.

---

Candidate Experiment

Objective

Determine how recursive memory contributes to inertial behavior.

Procedure

1. Compare one-step and two-step recursive update rules.
2. Vary \gamma.
3. Measure: overshoot, damping, oscillation, persistence.
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

$$
\boxed{(1-\gamma)\Delta\psi_n.}
$$

The remaining audit questions concern memory depth, memory persistence, neighbor coupling, and possible operator generalization of \gamma.

---

Final Yellow Lock

$$
\boxed{(1-\gamma)\Delta\psi_n\Rightarrow\text{Inertial Memory}}
$$

$$
\boxed{\text{Two States}+\text{One Shared Ground}+\text{No Ground Drift}}
$$

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

$$
x=\psi-\psi_0.
$$

Let the restoring response be

$$
F_{OW}=-\mathcal{A}(x).
$$

Let inertial memory be carried by

$$
(1-\gamma)\Delta\psi_n.
$$

Oscillation is repeated crossing of the shared reference ground produced by the interaction of bounded motion, restoring response, and inertial memory.

---

Mathematics

Bounded Motion confines the mode to a finite stable region around the reference ground.

Restoring Response always points toward the reference ground.

Inertial Memory carries the previous state change into the next update.

At the reference ground, x=0, the restoring response momentarily vanishes because there is no displacement.

Whether the mode crosses the ground therefore depends upon the carried motion (1-\gamma)\Delta\psi_n.

If sufficient motion remains, the mode crosses the reference ground and enters the opposite side of the restoring field.

The restoring response then reverses relative to the new displacement and again points toward the reference ground.

Repeated ground crossings produce oscillation.

---

Proof

Assume:

- Bounded Motion has been established.
- Restoring Response points toward the reference ground.
- Inertial Memory carries previous motion through (1-\gamma)\Delta\psi_n.

If the carried motion remains sufficient for the mode to cross the shared ground, then the mode overshoots the reference ground.

After crossing, displacement changes sign.

The restoring response again points toward the reference ground.

Repeated ground crossings therefore produce oscillation.

Hence,

$$
\boxed{
\text{Bounded Motion}+\text{Inertial Memory}+\text{Ground Crossing}\Rightarrow\text{Oscillation}.
}
$$

---

Alternative Outcome

If inertial memory decays before the mode crosses the reference ground, the mode returns toward equilibrium without overshooting.

This produces non-oscillatory return rather than oscillation.

Therefore,

$$
\boxed{
\text{Bounded Motion}+\text{Inertial Memory}\not\Rightarrow\text{Oscillation}
}
$$

unless ground crossing occurs.

---

Crossing Condition

The current crossing mechanism is (1-\gamma)\Delta\psi_n.

The exact inequality separating oscillation from non-oscillatory return has not yet been derived. This is structurally the same question as the classical underdamped/overdamped boundary (parked as \Gamma^2<4MK), to be re-derived natively from \gamma, \mathcal{A}, and the update rule rather than imported wholesale. This remains the primary Yellow audit target.

---

Assumptions

- Ground / Zero exists.
- Bounded Motion has been established.
- Restoring Response points toward the reference ground.
- Inertial Memory carries previous motion.
- Oscillation requires successful ground crossing.
- This Green node treats \psi as a scalar field.
- Multi-component oscillation and projection consistency (whether oscillation commutes with Projection, an extension of Blocker 0) remain open for future audit.

---

Candidate Experiment

Objective

Determine the conditions required for repeated ground crossing.

Procedure

1. Generate bounded motion.
2. Vary \gamma.
3. Measure: first ground crossing, overshoot, repeated crossings, decay, instability.
4. Identify the boundary separating: non-oscillatory return, damped oscillation, sustained oscillation, unstable growth.

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

$$
\boxed{
\text{Bounded Motion}+\text{Inertial Memory}+\text{Ground Crossing}\Rightarrow\text{Oscillation}.
}
$$

$$
\boxed{
\text{No Ground Crossing}\Rightarrow\text{Non-Oscillatory Return}.
}
$$

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

Let the One-Wave field state at step n be \psi_n.

A recursive update rule has the form

$$
\boxed{\psi_{n+1}=f(\psi_n,\psi_{n-1}).}
$$

More generally,

$$
\psi_{n+1}=f(\psi_n,\psi_{n-1},\psi_{n-2},\ldots).
$$

---

Mathematics

A one-step update has the form \psi_{n+1}=f(\psi_n).

A two-step recursive update has the form \psi_{n+1}=f(\psi_n,\psi_{n-1}).

A deeper-memory update has the form \psi_{n+1}=f(\psi_n,\psi_{n-1},\psi_{n-2},\ldots).

The difference \Delta\psi_n=\psi_n-\psi_{n-1} provides the motion information used by the current recursive update rule.

---

Proof

Assume previous states are retained: \psi_n,\psi_{n-1}.

Assume the update rule uses those retained states: \psi_{n+1}=f(\psi_n,\psi_{n-1}).

Previous outputs therefore become inputs to future evolution.

Hence,

$$
\boxed{
\text{Memory}+\text{Feedback Rule}\Rightarrow\text{Recursion}.
}
$$

Oscillation may arise from recursion, but recursion does not require oscillation.

---

Locality Rule

The current One-Wave update rule includes local-neighborhood coupling through \beta(\langle\psi_j^n\rangle-\psi_i^n).

This confirms the recursion is nonlocal at the nearest-neighbor level. The remaining open question is narrower than "local or nonlocal" — it is whether additional nonlocal effects beyond nearest-neighbor coupling exist.

---

Inertial Memory Link

The current recursive update rule naturally supports Inertial Memory through the two-state difference \Delta\psi_n=\psi_n-\psi_{n-1}.

Whether deeper memory contributes additional inertial behavior remains unresolved. (See Function: Inertial Memory for the full treatment, including memory depth and what is being remembered.)

---

Assumptions

- Previous field states can be retained.
- A feedback rule uses previous states.
- The update rule may have finite or deeper memory.
- Nearest-neighbor coupling exists and is confirmed nonlocal.
- Coupling beyond nearest-neighbor remains unresolved.
- Oscillation is not required for recursion.

---

Candidate Experiment

Objective

Determine the memory depth required to reproduce observed One-Wave behavior.

Procedure

1. Test one-step recursive updates.
2. Test two-step recursive updates.
3. Test deeper-memory recursive updates.
4. Compare: stability, convergence, oscillation, damping, propagation.
5. Determine whether nearest-neighbor coupling alone is sufficient, or whether longer-range coupling is needed.

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

The remaining audit questions concern memory depth and the range of recursive coupling beyond nearest-neighbor.

---

Final Yellow Lock

$$
\boxed{
\text{Memory}+\text{Feedback Rule}\Rightarrow\text{Recursion}
}
$$

$$
\boxed{
\psi_{n+1}=f(\psi_n,\psi_{n-1})
}
$$

$$
\boxed{
\Delta\psi_n=\psi_n-\psi_{n-1}
}
$$

---

Function Node

Function: Persistent Mode

Status: 🟡 Yellow

---

Purpose

A Persistent Mode is a recursive field pattern that survives repeated evolution without collapsing.

Recursion alone does not guarantee persistence.

Persistence requires stable recursive behavior.

---

Definition

Let the recursive update rule be

$$
\psi_{n+1}=f(\psi_n,\psi_{n-1}).
$$

A Persistent Mode is a recursive pattern that remains stable through repeated updates.

---

Mathematics

Operational Stability Criterion (testable now)

A recursive mode is operationally considered persistent if

$$
\boxed{
\|\psi_{n+k}-\psi_n\|<\varepsilon
}
$$

for sufficiently large k, where \varepsilon is the chosen stability tolerance. This is a direct trajectory test and is directly measurable in simulation or experiment.

Future Analytical Criterion (deferred)

Once the recursive update rule has been fully specified, stability may also be analyzed through perturbation methods. One possible analytical criterion is

$$
\lambda_{\max}<0,
$$

where \lambda_{\max} is the largest perturbation growth rate. This is a linearized-perturbation test, distinct from the operational trajectory test above — a system can satisfy one while not yet having been checked against the other, particularly near a bifurcation or at timescales longer than the operational test's window. This analytical test is deferred until the recursive dynamics have been fully derived.

---

Proof

Assume the recursive field evolves according to \psi_{n+1}=f(\psi_n,\psi_{n-1}).

If repeated recursive evolution satisfies \|\psi_{n+k}-\psi_n\|<\varepsilon, then the recursive pattern remains stable through repeated evolution.

Therefore

$$
\boxed{
\text{Stable Recursion}\Rightarrow\text{Persistent Mode}
}
$$

---

Hidden Assumptions

The proof leaves four measurable quantities to be defined.

Stability

The operational definition is \|\psi_{n+k}-\psi_n\|<\varepsilon. Future analytical criteria (\lambda_{\max}<0) remain open, to be applied once an explicit form for \mathcal{A} or f exists.

Persistent Mode (type)

A persistent mode may be periodic, quasiperiodic, stationary, localized, traveling, topological, or another stable recursive structure. This node does not yet distinguish among these possibilities.

Persistence Time

Persistence requires a measurable observation window. Future work must determine whether persistence means finite duration, experimental duration, or indefinite recursion.

Failure Modes

A Persistent Mode may fail through changes in one or more interaction mechanisms, including:

- instability,
- damping,
- mode coupling,
- flowback,
- surface tension,
- resistance / friction,
- electrical locking,
- numerical error.

The mathematical conditions under which these interaction mechanisms destabilize a Persistent Mode remain open.

---

Candidate Experiment

Objective

Determine which recursive structures remain persistent.

Procedure

1. Construct a recursive update rule.
2. Seed an initial mode.
3. Iterate the system over increasing time.
4. Measure \|\psi_{n+k}-\psi_n\|.
5. Classify the resulting behavior as convergence, oscillation, persistence, or collapse.
6. Apply controlled perturbations.
7. Determine which interaction changes preserve or destroy the Persistent Mode.

---

Dependencies

Core Functions

- Recursion
- Inertial Memory

Supporting Functions

- Prediction

Downstream Functions

- Book 1: Micro Objects
- Quark
- Proton
- Atom
- All higher persistent structures

---

Yellow Audit Result

The Green proof remains valid.

The Yellow audit identifies four measurable quantities requiring further definition: stability, persistence (mode type), persistence timescale, and failure conditions.

The operational stability criterion has been identified and is testable now. The future analytical stability test (\lambda_{\max}<0) remains open, pending an explicit form for the recursive dynamics.

This node serves as the bridge between the foundational function library and the object-based books that follow.

---

Final Yellow Lock

$$
\boxed{
\text{Stable Recursion}\Rightarrow\text{Persistent Mode}
}
$$

$$
\boxed{
\|\psi_{n+k}-\psi_n\|<\varepsilon
}
$$

subject to measurable definitions of stability, mode type, persistence timescale, and failure conditions.

---

Looking Ahead

Appendix Red A established the core functions of the One-Wave framework.

The remaining appendices expand these foundational functions into broader systems and relationships before the books apply them to physical structures.

With the functional language established, the next appendix builds upon this foundation and extends the framework into the next stage of development.
