#core/appliedneuroscience

![[in-silico.jpeg]]

In silico refers to **computer simulations and modelling of biological systems, such as neural circuits and brain networks.** These virtual experiments can provide insights into the mechanisms of neural function and disease and can also be used to predict the effects of drugs or therapies before testing them in the lab.

## Comparison with Other Approaches

In silico complements [[In vivo vs in vitro]] approaches. While *in vivo* studies examine living organisms and *in vitro* uses isolated cells/tissues, *in silico* enables exploration of scenarios impossible or unethical to test experimentally—such as systematic parameter variation or long timescale simulations.

## Applications in Neuroscience

- **Neural circuit simulation**: Modelling action potential propagation, synaptic transmission, and network dynamics
- **Drug screening**: Predicting pharmacological effects on ion channels and receptors
- **Whole brain emulation**: Investigating feasibility and computational requirements

## Model Hierarchy

Computational models vary in biological detail:
- [[Hodgkin-Huxley model]]: Biophysically detailed, models individual ion channel kinetics
- [[Leaky integrate-and-fire neurons]]: Simplified, captures spike timing without channel dynamics
- [[Point neuron]]: Abstract, represents firing rate without spatial extent

[[NeuroML]] provides a standardised XML format for exchanging neural models across simulation platforms.
