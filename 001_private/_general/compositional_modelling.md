#core/softwaredevelopment #core/mathematicalphysics #core/appliedneuroscience #fundamental/logic

**Compositional modelling** constructs a system's model from models of its parts and explicit rules for connecting them. Its central requirement is stronger than decomposition: **interpreting the connected whole must agree with connecting the interpretations of its parts**.

## Interfaces before analogies

In a process-oriented categorical model, **objects are interfaces** and **morphisms are processes**. A process $f:A\to B$ can feed into $g:B\to C$, producing $g\circ f:A\to C$. The matching interface is part of the claim, not a detail to be filled in later.

For ordinary functions, identities are pass-through functions and composition is associative. Parallel processes can be represented by

$$
f\times g:A\times C\to B\times D
$$

for $f:A\to B$ and $g:C\to D$. More generally, a monoidal product $\otimes$ describes parallel composition. Stateful physical systems require a suitable semantics for state, time, and coupling; they are not automatically ordinary functions from instantaneous inputs to outputs.

This differs from [dynamical abstraction](dynamical_abstraction.md), where objects are whole dynamical systems and morphisms translate their states. Both viewpoints are useful, but their arrows mean different things.

## Functorial semantics

Let a category describe permissible wiring diagrams and another their mathematical meanings. An interpretation $F$ is functorial when

$$
F(g\circ f)=F(g)\circ F(f),\qquad F(\mathrm{id}_A)=\mathrm{id}_{F(A)}.
$$

Fong and Spivak's signal-flow example interprets diagrams as matrices: connecting diagrams in series corresponds to matrix multiplication, and placing them in parallel corresponds to the appropriate block construction. This is an established example of [structure preservation](structure_preserving_connections.md), not merely a visual analogy.

## Cross-domain applications

| Existing concept | Compositional question | What the correspondence adds |
|---|---|---|
| [Problem decomposition](../people/problem_decomposition.md) | What interfaces let partial solutions become a valid whole? | Makes integration obligations explicit rather than assuming independence |
| Software modules | Do output types, units, timing, and preconditions satisfy the receiving module's contract? | Distinguishes interchangeable implementations from superficially similar APIs |
| [Open dynamical systems](../videos/open_dynamic_system.md) | How do one system's outputs become another's inputs? | Retains environmental coupling rather than treating every component as isolated |
| [Neural Engineering Framework](../books/how_to_build_a_brain/principles_of_the_neural_engineering_framework.md) | How do represented variables and decoded transformations combine? | Relates neural implementation to the computation specified at the interface |
| [NeuroML](../../004_subsidiary/_general/neuroml.md) | Which model components and connections can be represented and exchanged? | Separates reusable descriptions from verified simulator or physical equivalence |

These applications motivate explicit models; they do not establish a single functor connecting all software, biology, and neural simulation.

## Feedback is an additional obligation

Sequential and parallel composition do not by themselves define feedback. Closing a loop requires a well-defined solution or update rule, including how delay and state are handled. Even an apparently simple algebraic loop can have no solution or multiple solutions.

A toy discrete-time example shows why independent validation is insufficient:

$$
x_{t+1}=a x_t+u_t,\qquad y_t=x_t,\qquad u_t=k y_t.
$$

The uncoupled system is stable when $|a|<1$, but the closed loop evolves as $x_{t+1}=(a+k)x_t$ and is stable only when $|a+k|<1$. With $a=0.5$ and $k=0.75$, coupling produces an unstable multiplier of $1.25$.

A component that behaves acceptably under one input regime may therefore fail after replacement or reconnection. This matters to [adaptive control](../papers/distributed_adaptive_control_theory.md) and [brain-emulation criteria](../../002_profession/eightsix/invariant_brain_emulation.md): matching isolated responses is weaker than preserving behaviour in the intended environment.

## Relation to reductionism

[Methodological reductionism](reductionist_research_approach.md) studies parts. Compositionality asks what information about parts **and their interactions** suffices to recover the whole. It does not assume that interactions are negligible, that coupling is linear, or that emergent behaviour is absent. If the chosen interfaces omit essential coupling, refine the interfaces or abandon that decomposition.

## Sources

- Fong and Spivak, [*Seven Sketches in Compositionality*](https://arxiv.org/abs/1803.05316), §4.4 and §5.3.5 — monoidal composition and functorial semantics for signal-flow graphs.
- [Nengo: getting started](https://www.nengo.ai/nengo/getting-started.html), usage — ensembles, represented variables, transformations, connections, and probes.
- The feedback example is a direct calculation; the comparisons with neural modelling and software contracts are synthesis.
