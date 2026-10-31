#core/artificialintelligence #core/appliedneuroscience #core/mathematicalphysics

**Inference, learning, and control** solve different problems within an adaptive system: estimating what is happening, changing how the system models or responds to it, and choosing what to do. Their overlap lies in a shared perception–action architecture, not in their being the same computation.

## Keep the operations distinct

| Operation | Typical input and output | Question | Related concept |
|---|---|---|---|
| Inference | Observations and model → state estimate or posterior | What state is the world in? | [Bayesian brain hypothesis](../papers/bayesian_brain_hypothesis.md) |
| Learning | Experience → revised parameters, values, or policy | What should change with experience? | [Credit assignment](../../003_education/epfl/credit_assignment_problem.md) |
| Control | State estimate or belief and objective → action | What should the system do? | [Distributed adaptive control](../papers/distributed_adaptive_control_theory.md) |

The boundaries depend partly on the model: estimating unknown parameters can itself be Bayesian inference, while a fixed controller may operate without learning. The distinction concerns functional roles rather than mutually exclusive algorithm families.

## A precise bridge: partially observed control

A finite-state **partially observable Markov decision process (POMDP)** provides a worked example. Let $s_t$ be an unobserved state, $a_t$ an action, and $o_t$ an observation. Define transition probabilities $P(s'\mid s,a)$ and observation probabilities $P(o\mid s',a)$. A belief $b_t(s)$ is a probability distribution over states.

After action $a_t$ and observation $o_{t+1}$, Bayesian filtering gives

$$
b_{t+1}(s')\propto P(o_{t+1}\mid s',a_t)\sum_s P(s'\mid s,a_t)b_t(s).
$$

This is **inference**. A policy $a_t=\pi(b_t)$ supplies **control**, chosen against a specified reward or cost and time horizon. Changing the transition model, value estimates, or policy using experience introduces **learning**.

Under the standard Markov and observation assumptions with known model parameters and state-based rewards, the belief is a sufficient summary of history for decision-making. This connects to [information-preserving abstraction](information_preserving_abstraction.md). If relevant parameters are unknown, the state or belief may need to include them; an arbitrary learned latent vector does not inherit sufficiency automatically.

## What transfers to neuroscience?

- The **[Bayesian brain hypothesis](../papers/bayesian_brain_hypothesis.md)** concerns uncertain inference and possible neural implementations. It does not by itself specify an objective, a policy, or the body's dynamics.
- **[Distributed adaptive control](../papers/distributed_adaptive_control_theory.md)** places perception and learning within a body–environment loop, with reactive, adaptive, and contextual organisation. The POMDP example offers comparison points, not a derivation of DAC or proof that it implements exact Bayesian filtering.
- The **[credit assignment problem](../../003_education/epfl/credit_assignment_problem.md)** asks which earlier actions or internal components should be updated following an outcome. An error signal alone does not specify where or when credit belongs.
- **[Open dynamical systems](../videos/open_dynamic_system.md)** supply the interface language: observations arrive from an environment, actions change that environment, and subsequent observations depend on the coupling.

## Similar error signals are not identical claims

A sensory prediction error compares a predicted observation with an incoming signal. A reward prediction error concerns expected reward or return. A tracking error compares a controlled variable with a target. They can all guide updates, but they have different meanings, units, and objectives.

An accurate state estimate can support a poor action if the objective or policy is wrong. A successful controller can act without an explicit Bayesian posterior. Consequently, prediction-error reduction is not sufficient evidence for any one architecture or theory of consciousness.

## The category-theoretic contribution

[Compositional modelling](compositional_modelling.md) encourages typed interfaces between observation, belief update, policy, and environment. It lets us ask whether replacing one module preserves the behaviour of the coupled system. This is a **candidate modelling approach**, not an asserted equivalence of inference and control or a fully specified category of cognitive theories.

The useful experimental question is which distinction matters under intervention: changing sensory reliability, action consequences, or reward timing tests different parts of the loop. Similar performance on one task does not establish interchangeable internal mechanisms.

## Sources

- [Partially observable Markov decision process](https://en.wikipedia.org/wiki/Partially_observable_Markov_decision_process), belief update and belief MDP — the explicit mathematical bridge used here.
- The neuroscience comparisons synthesise the linked vault notes; they are not evidence that biological systems implement this exact POMDP model. See [structure-preserving connections](structure_preserving_connections.md) for the distinction between a formal example and a cross-domain hypothesis.
