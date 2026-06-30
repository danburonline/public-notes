#core/appliedneuroscience #core/artificialintelligence

![attractor-state](_attachments/attractor-state.png)

An attractor state is a **set of points in the [phase space](phase_space_and_phasing_rotator.md) toward which a dynamical system evolves regardless of its initial state**. The set of initial conditions that flow to a given attractor is its **basin of attraction** — the geometry of these basins governs error tolerance, generalisation, and interference between stored states.

## Basin of Attraction and Content-Addressable Memory

- A **basin of attraction** is the set of all initial states whose trajectories converge to a particular attractor. Larger basins yield more robust recall; overlapping basins produce interference and spurious memories.
- **Content-addressable memory** emerges naturally: a partial or noisy cue places the system inside the basin of some stored pattern, and recurrent dynamics perform pattern completion by rolling the state toward the attractor's centre. This is the principle behind Hopfield's (1982) associative memory and its continuous and spiking descendants.

## Types of Attractors

- **Point (fixed-point) attractors**: a stable equilibrium the system settles into and remains at — the substrate of categorical decisions and discrete memories.
- **Limit cycles**: periodic orbits the system returns to after a fixed period — the basis of central-pattern-generator rhythms and oscillatory binding.
- **Strange (chaotic) attractors**: irregular yet bounded trajectories with sensitive dependence on initial conditions and fractal structure. In the olfactory bulb, different odours correspond to distinct chaotic attractors whose basins are sculpted by learning, giving a spatiotemporal code robust to noise.
- **Continuous (line) attractors**: manifolds of fixed points parameterising an analog variable such as head direction or spatial position. Their bifurcations and noise-driven drift explain the finite precision of analog working memory.

## Energy Landscapes and Edge of Chaos

- In symmetric recurrent networks (Hopfield), a **Lyapunov energy function** decreases monotonically under the update rule, so dynamics converge to local minima. Each stored pattern is a minimum; retrieval is downhill flow. Classical capacity is α_c ≈ 0.138 patterns per neuron before spurious minima proliferate.
- Neural computation appears poised near the **edge of chaos** — the bifurcation between an ordered regime (rigid convergence to few fixed points) and a chaotic regime (exponential divergence of trajectories). Near criticality, correlation lengths and times are large, slow eigenmodes support temporal integration, and small inputs can reshape the attractor landscape. Empirical signatures include neuronal avalanches (Beggs & Plenz, 2003) and 1/f-like spectra.

## Applications in Neural Signal Processing

- **Modelling neural dynamics**: attractors model how circuits stabilise to a function or behaviour — memory, pattern recognition, persistent activity. The Hopfield network (1982) is the canonical computational model: stored patterns act as point attractors, and content-addressable retrieval corresponds to settling into the nearest basin from a partial cue.
- **Understanding neural connectivity**: attractor dynamics explain how networks achieve synchronisation and maintain distinct states. In [physical reservoir computing](../../../001_private/social-media/x/physical_reservoir_computing.md), the echo state property — where dynamics asymptotically wash out initial conditions — is a direct instance of attractor-based computation.
- **Decision-making circuits**: in Wang-type (2002) models of prefrontal cortex, competing excitatory populations with shared inhibition form a low-dimensional dynamical system. As recurrent excitation crosses a critical value, a pitchfork bifurcation creates two stable choice attractors separated by a separatrix; decision commitment is the noise-driven trajectory crossing the separatrix into one basin. Reaction-time and accuracy emerge as continuous-state analogues of drift-diffusion models.
- **Signal classification**: identifying attractor states in neural signals helps distinguish cognitive states or diagnose neurological conditions.

Attractor dynamics produce deterministic yet sometimes unpredictable behaviour. In chaotic regimes this connects to [computational irreducibility](../../../001_private/videos/computational_irreducibility.md): the only way to discover the system's trajectory is to simulate it — no shortcut exists, even when the attractor's governing equations are known. Near criticality, this irreducibility couples across scales, linking attractor dynamics to the failure of [decoupling of scale](../../../001_private/videos/decoupling_of_scale.md).

## Related Concepts

- [Bistability in cortical neurons](../../../001_private/books/sizing_up_consciousness/bistability_in_cortical_neurons.md) — two stable firing states as a single-cell attractor pair with a separatrix between basins
- [Decoupling of scale](../../../001_private/videos/decoupling_of_scale.md) — attractor dynamics at criticality as a source of cross-scale coupling
- [Physical reservoir computing](../../../001_private/social-media/x/physical_reservoir_computing.md) — echo state property as attractor-based computation
- [Computational irreducibility](../../../001_private/videos/computational_irreducibility.md) — chaotic attractors and the absence of simulation shortcuts
- [Phase space and phasing rotator](phase_space_and_phasing_rotator.md) — the geometrical substrate in which attractors live
