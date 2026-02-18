#core/appliedneuroscience #core/artificialintelligence

![lif](../../../000_inbox/attachments/lif.png)

The [Leaky](../../../001_private/books/Neural%20Networks%20from%20Scratch/Activation%20functions%20overview.md#leaky-relu) Integrate-and-Fire (LIF) model is a **simplified version of a neuron used in computational neuroscience.** It captures the essential features of neuronal activity and is computationally less complex than the [Hodgkin-Huxley model](Hodgkin-Huxley%20model.md).

## Core Concept

In the LIF model, a neuron is represented as a simple electrical circuit with a capacitor (representing the cell membrane) in parallel with a resistor (the membrane’s resistance to the flow of current). The neuron integrates incoming signals and generates an output (a ‘fire’) when the membrane potential reaches a certain threshold.

## Equations

The dynamics of the membrane potential $V$ in the LIF model are described by:

$$ \tau_m \frac{dV}{dt} = - (V - V_{rest}) + R_m I_e $$

where:

- $\tau_m = R_m C_m$ is the membrane time constant,
- $R_m$ is the membrane resistance,
- $C_m$ is the membrane capacitance,
- $V_{rest}$ is the [resting membrane potential](../../kings%20college/01%20Techniques%20in%20Neuroscience/Resting%20membrane%20potential.md),
- $I_e$ is the external current.

When $V$ reaches the threshold voltage $V_{threshold}$, the neuron fires an action potential, and $V$ is reset to the resting potential $V_{rest}$

## Fire and Reset

The ‘fire’ condition is represented as:

$$ \text{if } V \geq V_{threshold} \text{, then } V \leftarrow V_{reset} $$


> [!example] Applications
> The LIF model is widely used in the study of neural networks and in the field of neuromorphic engineering. Its simplicity allows for the simulation of large networks of neurons, making it a powerful tool for exploring principles of neural computation.
