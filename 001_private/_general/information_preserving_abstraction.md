#core/artificialintelligence #core/mathematicalphysics #fundamental/logic

**Information-preserving abstraction** discards distinctions while retaining the information needed for a specified inference or task. “Preserves information” is incomplete unless it states **information about what, under which model, and for which use**.

## Exact preservation of a question

Let $q:X\to Z$ compress a state and let $h:X\to Y$ express the answer to a question. The abstraction preserves that answer exactly if a readout $\bar h:Z\to Y$ exists such that

$$
h=\bar h\circ q.
$$

This **factorisation** is possible precisely when $h$ is constant on every fibre of $q$: whenever $q(x)=q(x')$, we also have $h(x)=h(x')$. The abstraction may forget much of $x$ while losing nothing relevant to $h$.

For example, knowing only the sum of two numbers preserves their average, but not their difference. The same representation is adequate for one question and inadequate for another. This is a simple commuting-diagram instance of [structure-preserving connections](structure_preserving_connections.md).

## Statistical sufficiency

In a statistical model $p(x\mid\theta)$, a statistic $Z=q(X)$ is **sufficient for $\theta$** when the conditional distribution of $X$ given $Z$ does not depend on $\theta$. For a dominated family, the Fisher–Neyman factorisation theorem expresses this as

$$
p(x\mid\theta)=a(x)\,b(q(x),\theta).
$$

Under independent Bernoulli sampling with fixed sample size, the number of successes is sufficient for the success probability: the order of successes carries no additional information about that parameter. If order matters to the generating process, that reduction may fail.

Sufficiency is therefore model-relative, not a declaration that discarded details are unimportant for every possible purpose.

## The information-theoretic boundary

For a representation generated only from $X$, a target $Y$ and code $Z$ satisfy the Markov condition $Y\to X\to Z$. The **data processing inequality** gives

$$
I(Y;Z)\leq I(Y;X).
$$

Processing cannot create additional information about $Y$ that was absent from $X$. It can nevertheless make existing information easier for a restricted predictor to use. In a fixed joint model, the task-sufficiency condition $Y\perp X\mid Z$ gives equality when these mutual informations are finite.

[Shannon information](../books/the_feeling_of_life_itself/shannon_information.md) quantifies statistical dependence. It does not, without additional assumptions, measure semantic understanding, causal fidelity, or consciousness.

## Connections and non-equivalences

- **[Autoencoders](../videos/autoencoder.md):** minimise reconstruction loss. A code can reconstruct common features accurately while losing a rare feature crucial to a downstream task. Exact reconstruction on a domain implies injective encoding there; approximate reconstruction does not establish an isomorphism.
- **[Latent spaces](../videos/latent_space.md):** are unobserved representations, not necessarily lower-dimensional or interpretable. Use predictive, reconstruction, or intervention-based tests appropriate to the intended role.
- **[Coarse-graining](../papers/coarse_graining.md):** preserves selected macrovariables by construction, but preserving their future evolution additionally requires [dynamical closure](dynamical_abstraction.md).
- **[Bayesian inference](../papers/bayesian_brain_hypothesis.md):** a sufficient statistic can preserve parameter inference within the specified model. This mathematical fact does not establish that a brain uses that statistic or implements Bayesian computation.
- **[Inference and control](inference_learning_and_control.md):** a belief state can summarise the history needed for decisions under a correctly specified POMDP. A code that predicts observations well need not retain everything required to choose good actions.

## A practical test of an abstraction

Specify the target before choosing the compression. Ask which merged inputs would require different answers, whether those cases occur in the intended domain, and whether a change of task or distribution invalidates the map. A reduction useful for classification may be unsuitable for causal intervention or substrate replacement.

## Sources

- [Sufficient statistic](https://en.wikipedia.org/wiki/Sufficient_statistic), mathematical definition and Fisher–Neyman factorisation — parameter-relative preservation and its information-theoretic formulation.
- Goodfellow, Bengio, and Courville, [*Deep Learning*, chapter 14](https://www.deeplearningbook.org/contents/autoencoders.html) — reconstruction, capacity restrictions, and learned codes.
- The deterministic factorisation criterion and examples are direct derivations; the cross-domain connections are synthesis rather than claims of universal equivalence.
