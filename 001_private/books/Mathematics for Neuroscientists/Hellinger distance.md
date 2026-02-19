#core/mathematicalphysics #core/appliedneuroscience 

![hellinger-distance](../../../_inbox/attachments/hellinger-distance.png)

The **Hellinger distance** is a statistical metric used to measure the similarity or difference between two probability distributions. It is a type of f-divergence and is closely related to the Bhattacharyya distance.

> [!info] What is f-divergence?
> **f-divergence** is a general class of functions used to measure the difference between two probability distributions. Given distributions $P$ and $Q$ (with densities $p(x)$ and $q(x)$), the f-divergence is defined for a convex function $f$ as:
> 
> $$
> D_f(P \| Q) = \int q(x) \, f\left(\frac{p(x)}{q(x)}\right) dx
> $$
> 
> Many familiar divergence measures, such as Kullback-Leibler divergence, total variation distance, and the Hellinger distance, are special cases of f-divergence, each corresponding to a different choice of the function $f$. These divergences provide a systematic way to quantify how one probability distribution differs from another.

## Formulas

### Continuous Distributions

For probability density functions $f$ and $g$:

$$
H(f, g) = \left( \frac{1}{2} \int \left( \sqrt{f(x)} - \sqrt{g(x)} \right)^2 dx \right)^{1/2}
$$

Alternatively:

$$
H^2(f, g) = 1 - \int \sqrt{f(x)g(x)} \, dx
$$

**Range:** $0$ (identical) to $1$ (completely different)

### Discrete Distributions

For discrete probability distributions $( P = (p_1, \ldots, p_k)$ and $Q = (q_1, \ldots, q_k)$:

$$
H(P, Q) = \frac{1}{\sqrt{2}} \sqrt{\sum_{i=1}^k \left( \sqrt{p_i} - \sqrt{q_i} \right)^2}
$$

## Properties

- **Metric:** Non-negative, symmetric, and satisfies the triangle inequality.
- **Bounded:** Always between 0 and 1 (with standard normalisation).
- **Interpretation:** Measures differences in the "square roots" of probability distributions, giving more weight to differences in the tails.
- **Relation to Bhattacharyya:** $H^2 = 1 - BC$, where $BC$ is the Bhattacharyya coefficient.

## Applications

- **Statistics:** Comparing probability distributions, hypothesis testing.
- **Machine Learning:** Clustering, distribution comparison.
- **Image Processing:** Image similarity.
- **Ecology:** Comparing species distributions.

----

> [!abstract] Hellinger distance in neural signals and mathematical neuroscience
> The **Hellinger distance** is valuable in mathematical neuroscience for quantifying differences between neural signals and population activity patterns. It can be used to:
> - **Compare probability distributions** of neural responses (e.g., spike trains, firing rates) across different experimental conditions or brain states.
> - **Assess changes in information content** by measuring how the probability distribution of neural features shifts due to learning, plasticity, or disease.
> - **Cluster or classify neural activity patterns** by evaluating the similarity between distributions from different brain regions, time periods, or subject groups.
> - **Analyse population coding**, where the Hellinger distance helps determine how distinguishable different stimulus-evoked neural responses are.
> 
> Overall, the Hellinger distance provides a principled, interpretable metric to compare probabilistic models of neural data and can reveal subtle changes in neural dynamics, supporting both theoretical and applied neuroscience research.
