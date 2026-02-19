#core/appliedneuroscience

![in-silico](../../../_inbox/attachments/in-silico.jpeg)

In silico refers to **computer simulations and modelling of biological systems, such as neural circuits and brain networks.** These virtual experiments can provide insights into the mechanisms of neural function and disease and can also be used to predict the effects of drugs or therapies before testing them in the lab.

## Comparison with Other Approaches

In silico complements [In vivo vs in vitro](In%20vivo%20vs%20in%20vitro.md) approaches. While *in vivo* studies examine living organisms and *in vitro* uses isolated cells/tissues, *in silico* enables exploration of scenarios impossible or unethical to test experimentally—such as systematic parameter variation or long timescale simulations.

## Applications in Neuroscience

- **Neural circuit simulation**: Modelling action potential propagation, synaptic transmission, and network dynamics
- **Drug screening**: Predicting pharmacological effects on ion channels and receptors
- **Whole brain emulation**: Investigating feasibility and computational requirements

## Model Hierarchy

Computational models vary in biological detail:
- [Hodgkin-Huxley model](../../epfl/02%20Computational%20Neuroscience/Hodgkin-Huxley%20model.md): Biophysically detailed, models individual ion channel kinetics
- [Leaky integrate-and-fire neurons](../../epfl/02%20Computational%20Neuroscience/Leaky%20integrate-and-fire%20neurons.md): Simplified, captures spike timing without channel dynamics
- [Point neuron](../../../002_profession/blue%20brain%20project/Point%20neuron.md): Abstract, represents firing rate without spatial extent

[NeuroML](../../../004_subsidiary/_%20general%20knowledge/NeuroML.md) provides a standardised XML format for exchanging neural models across simulation platforms.

## Computational Neural Models Cluster

In silico approaches span multiple levels of abstraction, from biophysically detailed to abstract:

| Model | Biological Detail | Computational Cost | Use Case |
|-------|------------------|-------------------|----------|
| [Hodgkin-Huxley model](../../epfl/02%20Computational%20Neuroscience/Hodgkin-Huxley%20model.md) | High (ion channel kinetics) | High | Understanding biophysics |
| [Leaky integrate-and-fire neurons](../../epfl/02%20Computational%20Neuroscience/Leaky%20integrate-and-fire%20neurons.md) | Medium (spike timing) | Medium | Network simulations |
| [Point neuron](../../../002_profession/blue%20brain%20project/Point%20neuron.md) | Low (firing rate) | Low | Large-scale models |

[NeuroML](../../../004_subsidiary/_%20general%20knowledge/NeuroML.md) enables interoperability between these approaches.
