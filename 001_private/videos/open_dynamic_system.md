#core/mathematicalphysics

An open dynamic system is a **system that interacts with its environment.** Unlike a closed system, where everything is self-contained, an open system is influenced by its surroundings and can exchange matter, energy, or information with them. A key feature is that the system's evolution is determined not just by its internal rules and initial state, but also by these external influences.

## Key Concepts

### Components of an Open Dynamic System

- **States (S)**: The internal configurations or "ways a system can be."
- **Inputs (I)**: What the system receives from its environment.
- **Outputs (O)**: What the system produces and sends back to the environment.
- **Update Function**: A rule that determines the system's next state based on its current state and input.
- **Readout Function**: A rule that determines the system's output based on its current state.

### System Behaviour

The "behaviour" of an open dynamic system refers to the set of all possible trajectories or signal patterns that the system can exhibit over time, following its internal laws and interactions with the environment — and it is exactly this behaviour that [invariant brain emulation](../../002_profession/eightsix/invariant_brain_emulation.md) must preserve when mapping a brain's dynamics onto an alternative substrate.

## Examples of Open Dynamic Systems

The concept of open dynamic systems is applied across various scientific fields:

- **Biology**: A living cell is a classic example of an open system. It takes in nutrients (input) from its environment, processes them through its metabolism (update function), and releases waste products (output).
- **Physics**: In modelling atmospheric or ocean flows, temperature, pressure, and moisture act as external parameters that influence the system's dynamics. A billiard ball on a table with a pocket is another simple example, where the ball's trajectory can "escape" the system.
- **Engineering**: In control theory and signal processing, systems are often designed to respond to external inputs. For instance, a thermostat receives temperature information from the environment and adjusts the heating or cooling system accordingly.

## Open vs. Closed Systems

The main distinction lies in their interaction with the environment:

| Feature                          | Open System                                                          | Closed System                                                                |
| :------------------------------- | :------------------------------------------------------------------- | :--------------------------------------------------------------------------- |
| **Interaction with Environment** | External influence is explicitly modelled through interfaces. | No external input is included in the autonomous model. |
| **Evolution** | Depends on internal state and external inputs. | Depends on internal state under the model's fixed laws. |
| **Examples** | A driven neural circuit or a controlled thermal system. | An idealised autonomous oscillator. |

Here “closed” means autonomous in a dynamical model. In thermodynamics, a closed system can still exchange energy, whereas an isolated system exchanges neither energy nor matter.

## Connections in the Vault

- [Compositional modelling](../_general/compositional_modelling.md) — connecting outputs to inputs creates a larger system; feedback requires explicit state, timing, and well-posedness conditions.
- [Dynamical abstraction](../_general/dynamical_abstraction.md) — reduced and detailed updates must agree across the intended input class, not only along a single trajectory.
- [Inference, learning, and control](../_general/inference_learning_and_control.md) — observations, belief updates, and actions occupy different interfaces in an adaptive loop.

- The regimes such trajectories settle into are studied in neural computation as [attractor states](../../003_education/kcl/08_advances_in_neuroscience/attractor_state.md), where dynamics poised near the edge of chaos let small inputs reshape the attractor landscape.
- The States/Inputs/Update/Readout components are the same vocabulary the [Neural Engineering Framework](../books/how_to_build_a_brain/principles_of_the_neural_engineering_framework.md) uses to model neural populations: representing variables through distributed activity, transforming them via update dynamics, and decoding them through readout.
