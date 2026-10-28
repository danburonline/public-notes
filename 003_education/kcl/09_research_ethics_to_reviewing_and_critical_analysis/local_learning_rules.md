#core/appliedneuroscience #core/artificialintelligence

**Local learning rules update synaptic strength using information available at or near the synapse; this locality does not imply access to global or behavioural output error.** They are computational models of
[synaptic plasticity](../04_biological_foundations_of_mental_health/synaptic_plasticity.md), not complete theories of learning.

## Local learning rules

- **Hebbian:** [Hebbian plasticity](../04_biological_foundations_of_mental_health/hebbian_synaptic_plasticity.md) strengthens co-active connections: $\Delta w = \eta x_{\mathrm{pre}}y_{\mathrm{post}}$.
  Correlation can form [Hebbian assemblies](../../../004_subsidiary/_general/hebbian_assemblies.md), but unbounded gain and no task error signal limit the rule.
- **STDP:** The canonical phenomenological protocol potentiates pre-before-post spikes and depresses the reversed order.
  Its sign and timing window are context-dependent across synapses, cells, development, neuromodulation, and protocol; it is not universal.
- **BCM:** A sliding threshold, $\theta_M$, tracks postsynaptic activity history: $\Delta w = \eta x y(y-\theta_M)$.
  Activity above or below it favours potentiation or depression, limiting runaway Hebbian gain; BCM is not a complete biophysical account. This connects to [homeostatic plasticity](../../../001_private/books/augmenting_cognition/activity-dependent_plasticity.md).
- **Oja:** Normalisation limits Hebbian weight growth: $\Delta w_i = \eta y(x_i-yw_i)$.
  For a linear neuron under suitable input, learning-rate, and convergence assumptions, weights approach the first principal component; this is not general-purpose PCA.

In multilayer or recurrent circuits, local activity does not reveal a synapse’s distant effect on output error.
Eligibility traces retain a local activity mark while a delayed, often broadcast modulatory third factor gates change, $\Delta w_i \propto e_i m$: a qualified bridge to the [credit-assignment problem](../../epfl/credit_assignment_problem.md), not equivalent to exact backpropagation.

Local plasticity can link repeated activity to assemblies, while delayed third-factor signals link local traces to consequences; these constraints connect biological mechanisms to event-driven [leaky integrate-and-fire neurons](../../epfl/leaky_integrate-and-fire_neurons.md) and [biomimetic neuromorphics](../../../002_profession/eightsix/biomimetic_neuromorphics.md), without assuming that biological plausibility has been solved.

## Sources

- Hebb, D. O. (1949). *The Organization of Behavior*. [Archive](https://archive.org/details/organizationofbe00hebb).
- Bienenstock, Cooper and Munro (1982). [BCM theory](https://doi.org/10.1523/JNEUROSCI.02-01-00032.1982).
- Oja, E. (1982). [Oja’s rule](https://doi.org/10.1007/BF00275687).
- Markram, Gerstner and Sjöström (2012). [STDP review](https://doi.org/10.3389/fnsyn.2012.00002); Gerstner et al. (2018). [Eligibility traces](https://doi.org/10.3389/fncir.2018.00053).
