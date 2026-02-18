#core/appliedneuroscience

Bistability in cortical neurons refers to their **ability to maintain two stable states of membrane potential or firing rates, switching between them in response to transient inputs.** This property is fundamental to various neural computations and memory functions.

## Mechanisms and Properties

The phenomenon of bistability primarily arises from the interplay of voltage-gated [ion channels](../../../003_education/kings%20college/01%20Techniques%20in%20Neuroscience/Ion%20channels.md), particularly persistent sodium currents and calcium-activated potassium currents. These create positive feedback loops that can sustain depolarized states. A key feature of bistable neurons is hysteresis, where the neuron’s state depends not only on current inputs but also on its history.

Conceptually, the two stable states can be viewed as attractors in the neuron’s state space, with a separatrix dividing their basins of attraction. This attractor dynamics underlies the neuron’s ability to maintain distinct states.

[Neuromodulators](../../../003_education/kings%20college/04%20Biological%20Foundations%20of%20Mental%20Health/Neurotransmitters%20vs.%20neuromodulators%20vs.%20neuropeptides.md#neuromodulators) like acetylcholine and norepinephrine can significantly influence the bistable properties of neurons, affecting their computational capabilities. While individual neurons can exhibit bistability, network interactions can further stabilize or destabilize these states, leading to emergent bistable behavior at the circuit level.

## Functional Implications and Observations

Bistability is thought to play a crucial role in working memory, decision-making, and the maintenance of persistent activity in the absence of ongoing stimulation. It has been observed in various cortical regions, including the prefrontal cortex and sensory areas, often using intracellular recordings and pharmacological manipulations.

To study bistable dynamics, researchers employ computational models ranging from detailed [Hodgkin-Huxley](../../../003_education/epfl/02%20Computational%20Neuroscience/Hodgkin-Huxley%20model.md) type models with additional currents to simplified models like the FitzHugh-Nagumo model.
