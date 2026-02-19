#core/appliedneuroscience #core/artificialintelligence

![hodgkin-huxley](../../../_inbox/attachments/hodgkin-huxley.png)

The Hodgkin-Huxley model is a **mathematical model that describes how action potentials in neurons are initiated and propagated.** It is a set of nonlinear differential equations that approximate the electrical characteristics of excitable cells such as neurons.

## Key Components

The model is based on the concept of the neuron as an electrical circuit, which includes:

- **Membrane capacitance (C)**: Represents the ability of the neuron membrane to store charge.
- **Ion conductances (g)**: These are variable and depend on voltage; they determine how easily ions can flow across the membrane.
- **Ion equilibrium potentials (E)**: The voltage at which there is no net flow of a particular ion across the membrane.

## Gating Variables

[Ion channels](../../kings-college/01%20Techniques%20in%20Neuroscience/Ion%20channels.md) are gated by variables that change with voltage and time, reflecting the probability of a channel being open or closed. There are three main gating variables:

- **n**: Potassium channel activation gate
- **m**: Sodium channel activation gate
- **h**: Sodium channel inactivation gate

These variables obey first-order kinetics and are described by their rate constants for opening (\(\alpha\)) and closing (\(\beta\)).

## Equations

The fundamental equations of the Hodgkin-Huxley model include:

1. **[Membrane](../../kings-college/01%20Techniques%20in%20Neuroscience/Resting%20membrane%20potential.md) equation:**

   $$ C \frac{dV}{dt} = I - (g_{Na} m^3 h (V - E_{Na}) + g_{K} n^4 (V - E_{K}) + g_{L} (V - E_{L})) $$

2. **Gating variables**:

   $$ \frac{dn}{dt} = \alpha_n(V) (1-n) - \beta_n(V) n $$

   $$ \frac{dm}{dt} = \alpha_m(V) (1-m) - \beta_m(V) m $$

   $$ \frac{dh}{dt} = \alpha_h(V) (1-h) - \beta_h(V) h $$

3. **Rate constants**:
   - For $n$:

     $$ \alpha_n(V) = 0.01 \frac{V + 55}{1 - e^{-\frac{V + 55}{10}}} $$

     $$ \beta_n(V) = 0.125 e^{-\frac{V + 65}{80}} $$

   - For $m$:

     $$ \alpha_m(V) = 0.1 \frac{V + 40}{1 - e^{-\frac{V + 40}{10}}} $$

     $$ \beta_m(V) = 4 e^{-\frac{V + 65}{18}} $$

   - For $h$:

     $$ \alpha_h(V) = 0.07 e^{-\frac{V + 65}{20}} $$

     $$ \beta_h(V) = \frac{1}{1 + e^{-\frac{V + 35}{10}}} $$

4. **Currents**:
   - Sodium current $I_{Na}$:

     $$ I_{Na} = g_{Na} m^3 h (V - E_{Na}) $$

   - Potassium current $I_{K}$:

     $$ I_{K} = g_{K} n^4 (V - E_{K}) $$

   - Leakage current $I_{L}$:

     $$ I_{L} = g_{L} (V - E_{L}) $$


> [!example] Applications
> The Hodgkin-Huxley model has been fundamental in neurophysiology, contributing to our understanding of the ionic basis of action potentials. It is widely used in computational neuroscience to simulate the behaviour of neurons and neural circuits.
