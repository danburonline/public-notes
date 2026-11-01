#core/mathematicalphysics #core/softwaredevelopment

An **open dynamical system** models an internal state evolving under external inputs and producing observable outputs. The interface is a modelling choice; outputs need not reveal the full state.

## Minimal model

For a deterministic discrete-time model, let $S$, $I$ and $O$ denote the state, input and output sets:

$$
s_{t+1}=u(i_t,s_t),\quad o_t=r(s_t),
\qquad u:I\times S\to S,\quad r:S\to O.
$$

An initial state and input sequence determine a trajectory. With finite sets and a chosen initial state, this is precisely a **finite Moore machine**: a direct correspondence between dynamical and computational descriptions.

## Composition and use

Connecting one system's readout to another's input retains both internal states. Signal types and update timing must match; stateful composition is not simply chaining instantaneous functions. [Compositional modelling](../_general/compositional_modelling.md) formalises the wiring rules.

- [Dynamical abstraction](../_general/dynamical_abstraction.md) — test whether state abstraction preserves dynamics across intended inputs, not just one trajectory.
- [Neural Engineering Framework](../books/how_to_build_a_brain/principles_of_the_neural_engineering_framework.md) — distinguish neural activity from decoded variables; successful readout alone does not establish correct dynamics.

**Scope:** this model assumes deterministic updates and state-only readout; continuous-time or stochastic dynamics need other formulations. “Autonomous” means no variable input, unlike thermodynamic “closed”, which permits energy exchange.

## Sources

- Spivak, [discrete systems and Moore machines](https://arxiv.org/html/1512.00802v2#S4), Definition 2.1 and Remark 2.3.
- Vagner, Spivak and Lerman, [wiring-diagram semantics](https://arxiv.org/html/1408.1598v2), Definition 3.1 and Proposition 4.5.
- Nengo, [represented variables and readouts](https://www.nengo.ai/nengo/getting-started.html#usage).
