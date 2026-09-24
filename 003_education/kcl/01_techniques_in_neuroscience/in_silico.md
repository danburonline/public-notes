#core/appliedneuroscience #core/artificialintelligence

![in-silico](_attachments/in-silico.jpeg)

In silico refers to **computer simulations and modelling of biological systems, such as neural circuits and brain networks.** These virtual experiments can provide insights into the mechanisms of neural function and disease and can also be used to predict the effects of drugs or therapies before testing them in the lab.

## Comparison with Other Approaches

In silico complements [In vivo vs in vitro](in_vivo_vs_in_vitro.md) approaches. While _in vivo_ studies examine living organisms and _in vitro_ uses isolated cells/tissues, _in silico_ enables exploration of scenarios impossible or unethical to test experimentally—such as systematic parameter variation or long timescale simulations.

## Applications in Neuroscience

- **Neural circuit simulation**: Modelling action potential propagation, synaptic transmission, and network dynamics
- **Drug screening**: Predicting pharmacological effects on ion channels and receptors
- **Whole brain emulation**: Investigating model feasibility and computational requirements, not demonstrating established cognitive, phenomenological, or personal-identity emulation

## Model Hierarchy

Computational models make purposeful trade-offs among biological fidelity, computational cost and scale, and the information required by a question; this is not a universal better-or-worse ranking:

- [Hodgkin-Huxley model](../../epfl/hodgkin-huxley_model.md): Biophysically detailed, models individual ion channel kinetics at higher computational cost
- [Leaky integrate-and-fire neurons](../../epfl/leaky_integrate-and-fire_neurons.md): Simplified, captures spike timing with passive leak and threshold/reset dynamics without detailed channel dynamics
- [Point neuron](../../../002_profession/bluebrain/point_neuron.md): Abstract, removes spatial extent while particular models can retain spike timing and simplified membrane dynamics

[NeuroML](../../../004_subsidiary/_general/neuroml.md) provides a standardised representation and exchange format across simulation platforms; interoperability is a separate dimension from biological fidelity and computational cost.

## Computational Neural Models Cluster

In silico approaches span multiple levels of abstraction, from biophysically detailed to abstract. The comparison below describes common trade-offs rather than a fixed hierarchy of universally superior models:

| Model                                                                                                            | Biological Detail           | Computational Cost | Use Case                 |
| ---------------------------------------------------------------------------------------------------------------- | --------------------------- | ------------------ | ------------------------ |
| [Hodgkin-Huxley model](../../epfl/hodgkin-huxley_model.md)                         | High (ion channel kinetics) | High               | Understanding biophysics |
| [Leaky integrate-and-fire neurons](../../epfl/leaky_integrate-and-fire_neurons.md) | Medium (spike timing and simplified membrane dynamics) | Medium             | Network simulations      |
| [Point neuron](../../../002_profession/bluebrain/point_neuron.md)                                       | Low and model-dependent (spike timing and membrane detail) | Low                | Large-scale models       |

[NeuroML](../../../004_subsidiary/_general/neuroml.md) enables interoperability between these approaches without resolving their fidelity-versus-cost trade-offs.
