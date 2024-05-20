#core/appliedneuroscience #lead/cognitivecomputing

Local **learning rules adjust synaptic strengths based on local information at the synapse**, crucial for neural plasticity, learning, and memory.

## Types of Local Learning Rules

### [[Hebbian synaptic plasticity|Hebbian]] Learning

“Cells that fire together, wire together.” Synaptic strength increases when both pre- and postsynaptic neurons are active.

- **Formula**: $Δw = η * x * y$

### Spike-Timing-Dependent Plasticity (STDP)

Adjusts synaptic strength based on the timing of spikes. LTP occurs if the presynaptic spike precedes the postsynaptic spike, and LTD if the reverse happens.

### BCM Rule

Modifies synaptic strength based on postsynaptic activity and a dynamic threshold.

- **Formula**: $Δw = η * y * (y - θ_M) * x$

### Oja’s Rule

A normalised Hebbian rule preventing runaway synaptic growth.

- **Formula**: $Δw = η * (yx - w * y^2)$

> [!example] Applications
> - **Neural Network Models**: Key for developing and understanding artificial neural networks.
> - **[[Synaptic Plasticity]]**: Crucial for exploring synaptic changes and neural circuit adaptation.
> - **Cognitive Functions**: Explains local synaptic changes leading to complex behaviours.
