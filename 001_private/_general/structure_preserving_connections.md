#lead/computationalphilosophy #core/mathematicalphysics #fundamental/logic

**Structure-preserving connections** compare concepts by the operations, relations, or observations that survive a translation between them. Category theory makes this question precise: not merely “do these ideas sound alike?”, but “what maps to what, and does the mapping respect composition?”

This is a method for interdisciplinary synthesis, not a claim that every analogy is a categorical equivalence. The connections below combine established mathematical definitions with explicitly conditional applications to existing notes.

## A map of shared structures

| Bridge | Concepts connected | What is shared | What must not be conflated |
|---|---|---|---|
| [Dynamical abstraction](dynamical_abstraction.md) | Coarse-graining, scale decoupling, neural engineering, invariant brain emulation | A mapping that respects time evolution | A many-to-one reduction versus an invertible equivalence |
| [Information-preserving abstraction](information_preserving_abstraction.md) | Shannon information, sufficient statistics, latent spaces, autoencoders | Retaining information needed for a specified question | Reconstruction quality versus predictive or causal adequacy |
| [Compositional modelling](compositional_modelling.md) | Problem decomposition, software interfaces, open systems, neural models | Building a whole from typed parts and explicit connections | Separate component success versus success after coupling |
| [Inference, learning, and control](inference_learning_and_control.md) | Bayesian brain, distributed adaptive control, credit assignment | Different operations inside a perception–action loop | State estimation, parameter learning, and action selection |
| [Yoneda and the inverted spectrum](../videos/yoneda_lemma_and_the_inverted_spectrum_problem.md) | Relational identity, functionalism, the Newman problem | Identity relative to a chosen structure | Mathematical reconstruction versus discovery of phenomenal properties |

## The categorical toolkit

A **category** specifies objects, morphisms between them, identity morphisms, and associative composition. The choice of morphisms determines which structure matters. Smooth maps, probabilistic channels, and causal interventions are not interchangeable merely because each can be drawn as an arrow.

A **functor** $F:\mathcal C\to\mathcal D$ maps both objects and morphisms, preserving identities and composition:

$$
F(\mathrm{id}_A)=\mathrm{id}_{F(A)},\qquad F(g\circ f)=F(g)\circ F(f).
$$

Matching a list of concepts between two disciplines is therefore not yet a functor: the operations between the concepts must also translate consistently.

A **commuting diagram** states that two routes produce the same result. For example, [dynamical abstraction](dynamical_abstraction.md) asks whether “evolve then simplify” equals “simplify then evolve”. This gives a testable condition rather than an impression of similarity.

An **isomorphism** is a morphism with an inverse in the chosen category. A bijection of underlying sets alone need not be an isomorphism when additional structure matters. An **equivalence of categories** is different: it uses functors in both directions whose composites are naturally isomorphic to the identity functors. Neither term is a synonym for “related”.

A **natural transformation** compares two functors $F,G:\mathcal C\to\mathcal D$ using maps $\eta_A:F(A)\to G(A)$ satisfying, for every $f:A\to B$,

$$
G(f)\circ\eta_A=\eta_B\circ F(f).
$$

This is a useful target when comparing two whole modelling pipelines: conversion between their representations must be compatible with every operation being compared, not only with one example.

## A worked comparison: reduction versus replacement

[Coarse-graining](../papers/coarse_graining.md) maps detailed states onto fewer distinctions. [Invariant brain emulation](../../002_profession/eightsix/invariant_brain_emulation.md) asks whether an alternative substrate can preserve specified dynamics and measurements.

Both can be investigated using a map $q$ satisfying $q\circ T=\bar T\circ q$. But the same equation supports different claims:

- If $q$ merges states, it can describe a **reduction**. Information about the merged distinctions is lost.
- If $q$ has an inverse of the required kind, it can describe a **dynamical equivalence**.
- If only readouts match, it describes a weaker **observational agreement**, unless further conditions are established.

The shared structure transfers a question and a method of testing it. It does not make reduction, replacement, or preservation of personal identity the same phenomenon.

## How to evaluate a proposed connection

1. **Specify the objects and scale.** Are these states, whole systems, models, distributions, or interfaces?
2. **Name the arrows.** Are they measurements, state transitions, translations, or physical interventions? How do they compose?
3. **State what survives.** A prediction, probability distribution, temporal relation, causal response, or other invariant?
4. **Check a two-step operation.** Does translating a composite agree with composing the translations? If only approximately, state a metric, tolerance, and domain of validity.
5. **Look for a counterexample.** Which discarded distinction could change the outcome? Does the connection survive perturbation or a change of context?
6. **Label the result.** Use *formal result under stated assumptions*, *candidate mapping*, or *heuristic analogy*. A suggestive diagram alone is not a proof.

Approximate agreement within a tolerance is generally not transitive. Two acceptable translations in sequence can exceed the original error budget; uncertainty must travel with the connection.

## Boundaries

- A note link is a navigation aid, not a morphism with an automatically defined mathematical meaning. Chaining links does not establish a theorem.
- A common diagram does not establish a common mechanism. [Inference and control](inference_learning_and_control.md) illustrate distinct operations that fit together without becoming equivalent.
- [Yoneda](../videos/yoneda_lemma_and_the_inverted_spectrum_problem.md) determines objects up to isomorphism within an already specified category. It cannot supply properties excluded by that specification.
- The [Newman problem](../papers/newman_problem_of_the_brain.md) motivates grounding structural claims in independently constrained measurements and interventions, rather than choosing arbitrary relations that make a desired correspondence hold.

## Sources

- Fong and Spivak, [*Seven Sketches in Compositionality*](https://arxiv.org/abs/1803.05316), §§3.2–3.3 and §5.3.5 — categories, functors, natural transformations, and compositional semantics.
- Capucci, [“No, the Yoneda lemma doesn’t solve the problem of qualia”](https://matteocapucci.eu/no-the-yoneda-lemma-doesnt-solve-the-problem-of-qualia/) — limits of transferring structural results into consciousness claims.
