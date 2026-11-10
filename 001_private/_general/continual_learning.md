#core/artificialintelligence #core/biomimeticneuromorphics

**Continual learning** is learning from a non-stationary stream of tasks or data without retraining from scratch, while keeping earlier competence. Its central tension is the **stability-plasticity dilemma**: weights plastic enough to absorb new experience tend to overwrite old knowledge, a failure called **catastrophic forgetting** ([McCloskey and Cohen, 1989](https://doi.org/10.1016/S0079-7421(08)60536-8)).

## Mechanisms borrowed from brains

- **Synaptic consolidation:** protect parameters that mattered for earlier tasks, as in elastic weight consolidation ([Kirkpatrick et al., 2017](https://doi.org/10.1073/pnas.1611835114)), an abstraction of [synaptic plasticity](../../003_education/kcl/04_biological_foundations_of_mental_health/synaptic_plasticity.md) with stabilised synapses.
- **Complementary learning systems:** a fast episodic store replays experience into a slow, structured learner ([McClelland et al., 1995](https://doi.org/10.1037/0033-295X.102.3.419)).
- **Sparse, modular codes:** distinct [assemblies](../../004_subsidiary/_general/hebbian_assemblies.md) reduce interference between memories.

## Why embodiment matters

An agent acting in an open world faces distribution shift it partly causes, so learning cannot be separated from [inference and control](inference_learning_and_control.md). Robots make this concrete and measurable: drift in behaviour is observable and costly.

## Safety and control

For deployed agents, the open question is not only how to keep learning but how to **bound** it: limits on behavioural drift, verifiable or reversible updates, and evaluation that tracks retained as well as new skills. A neuro-inspired learner is attractive here only if its consolidation rules make such guarantees easier to state and test.

## Related

- [Biomimetic neuromorphics](../../002_profession/eightsix/biomimetic_neuromorphics.md): substrate-level plasticity that must also avoid overwriting function
- [Universal approximation theorem](universal_approximation_theorem.md): capacity says nothing about retention
