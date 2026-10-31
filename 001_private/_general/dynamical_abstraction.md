#core/mathematicalphysics #core/appliedneuroscience #core/artificialintelligence

**Dynamical abstraction** maps a detailed system to another description while preserving specified aspects of its evolution. It connects physical coarse-graining, learned state representations, and neural implementation through the question: **does changing representation commute with advancing time?**

## A common mathematical structure

For discrete-time deterministic systems, let $T:X\to X$ be a detailed update rule, $\bar T:Z\to Z$ a reduced rule, and $q:X\to Z$ a representation map. Exact compatibility requires

$$
q\circ T=\bar T\circ q.
$$

Consequently, $q\circ T^n=\bar T^n\circ q$ for every non-negative integer $n$. The same prediction follows whether the detailed system evolves first or the reduced system evolves after abstraction.

This gives a concrete category: objects are pairs $(X,T)$ and morphisms are maps satisfying the compatibility equation. Identity maps and ordinary composition satisfy the required laws. Continuity or smoothness can be required when those structures matter. Here, **objects are systems and arrows are maps between systems**, not individual time steps.

- A continuous, surjective $q$ gives a **semiconjugacy**: a reduced system can retain dynamics while losing distinctions.
- An invertible $q$ with continuous inverse gives a **topological conjugacy**. Requiring a smooth map and smooth inverse gives smooth conjugacy.
- A [diffeomorphism](../../002_profession/eightsix/diffeomorphic_transformation.md) alone is not a dynamical conjugacy: it must also satisfy the compatibility equation.

For continuous-time flows, the condition is $q\circ\Phi_t=\Psi_t\circ q$ for every relevant $t$. This preserves the chosen time parametrisation, not merely the shapes of trajectories.

## When can a reduced update exist?

Assume $q$ is surjective. A deterministic reduced rule is well-defined exactly when states that are merged remain merged after one step:

$$
q(x)=q(x')\quad\Longrightarrow\quad q(T(x))=q(T(x')).
$$

Then $\bar T(q(x)):=q(T(x))$ does not depend on which representative $x$ is chosen. This is the **closure problem** of reduced dynamics.

**Toy counterexample.** Let $x=(a,b)$, $T(a,b)=(b,a)$, and $q(a,b)=a$. States $(0,0)$ and $(0,1)$ initially have the same reduced state, but their next reduced states are $0$ and $1$. No deterministic update based only on $a$ can reproduce both. Retaining more state, introducing memory, or adopting a probabilistic model may be necessary.

For stochastic systems, the corresponding question concerns preservation of transition probabilities; deterministic closure cannot simply be assumed. For [open systems](../videos/open_dynamic_system.md), compatible updates must hold over a specified class of inputs, not just one unperturbed trajectory.

## Connections across the vault

| Concept | Candidate map | Preservation requirement | Limit |
|---|---|---|---|
| [Coarse-graining](../papers/coarse_graining.md) | Microstates to macrovariables | Closed or suitably approximate macro-dynamics | Averaging can discard memory needed for prediction |
| [Decoupling of scale](../videos/decoupling_of_scale.md) | Fast and slow variables to an effective description | Neglected variables have controlled effects | Scale separation helps but does not automatically prove closure |
| [Autoencoders](../videos/autoencoder.md) | Observations to latent codes | A learned latent update predicts encoded future observations | Reconstruction loss alone does not impose dynamical compatibility |
| [Neural Engineering Framework](../books/how_to_build_a_brain/principles_of_the_neural_engineering_framework.md) | Neural activity to represented variables | Decoded neural evolution approximates target dynamics | Finite populations, synapses, and noise introduce error |
| [Invariant brain emulation](../../002_profession/eightsix/invariant_brain_emulation.md) | Reference-system states to replacement-system states | Specified trajectories, inputs, and readouts agree | Neither a coordinate map nor behavioural agreement establishes preserved experience |

These are conditional applications of the same mathematical question, not established equivalences among the physical systems.

## Approximation and composition

For a metric $d_Z$, a one-step discrepancy can be written as

$$
\epsilon(x)=d_Z\bigl(q(T(x)),\bar T(q(x))\bigr).
$$

Small one-step error need not imply small long-term error: instability, feedback, or visits outside the tested region can amplify it. Report the initial conditions, input class, time horizon, and observable being tested. [Compositional modelling](compositional_modelling.md) adds a further demand: the abstraction must remain adequate after coupling to other systems.

Unlike full state reconstruction, [information-preserving abstraction](information_preserving_abstraction.md) asks which distinctions a particular prediction needs. That choice determines what it is reasonable to demand that the dynamics preserve.

## Sources

- [Topological conjugacy](https://en.wikipedia.org/wiki/Topological_conjugacy), definitions and flows — conjugacy, semiconjugacy, and time-preserving versus orbital equivalence.
- [Nengo: getting started](https://www.nengo.ai/nengo/getting-started.html), usage — represented variables, neural connections, readouts, and synaptic filtering.
- The category construction, closure criterion, and toy counterexample above are direct mathematical derivations; the cross-domain comparisons are synthesis. See [structure-preserving connections](structure_preserving_connections.md) for the method.
