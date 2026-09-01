#core/appliedneuroscience #core/artificialintelligence

The generalisation gradient is the graded decrement in learned responding as a test stimulus becomes less similar to the original conditioned stimulus — the behavioural signature of similarity-based generalisation.

## Origin in Learning Theory

- **Guttman & Kalish (1956)**: Pigeons trained to peck at a specific wavelength of light show a systematic, graded decrease in pecking as the test wavelength shifts away from the training value — the canonical generalisation gradient.
- It is not all-or-nothing: responding falls off smoothly with **physical or perceptual similarity** to the conditioned stimulus, not abruptly at a category boundary.
- This distinguishes generalisation from [extinction](extinction_learning.md): extinction is the removal of reinforcement, whereas generalisation is the spread of a reinforced response to similar stimuli.

## Behavioural Mechanism

- Generalisation gradients are observed in both [classical conditioning](classical_conditioning.md) and [operant learning](operant_learning.md), shaped by [reinforcement](reinforcement_and_reinforcers.md) history.
- The steepness of the gradient indexes **discrimination** — a steep gradient means the organism distinguishes sharply; a flat gradient means broad generalisation. Skinner's operant methods ([the operant chamber](the_operant_chamber_skinner_box.md)) provide the controlled setting for measuring these gradients.
- **Peak shift**: after discrimination training (rewarding S+, not S−), the gradient's peak shifts away from S− — a signature of learned discrimination, not just raw similarity.

## Neural and Computational Parallels

- **Neural tuning**: The behavioural gradient mirrors neural population tuning — neurons respond to a range of stimuli around a preferred value, and representational similarity decays with stimulus distance. This is the same logic as partial-volume blurring in neuroimaging ([partial volume effect](../../../001_private/books/introduction_to_neuroimaging_analysis/partial_volume_effect_in_mri.md)) and the tuning-curve overlap that underlies population coding.
- **Machine learning**: The generalisation gradient is the behavioural analogue of **kernel similarity** in ML — a model's response to a new input decays with its distance from training examples. In neural networks, this is formalised by similarity in activation space ([activation functions](../neural_networks_from_scratch/activation_functions_overview.md) determine the representational geometry).
- **Credit assignment**: Distinguishing which stimuli to credit with outcomes is the [credit assignment problem](../../epfl/credit_assignment_problem.md) — a steep gradient is a narrow credit assignment.

## Why It Matters Across Competencies

- **Applied neuroscience**: gradient steepness indexes learning precision and is altered in anxiety (over-generalisation) and autism (under-generalisation).
- **Artificial intelligence**: kernel similarity and representation geometry are the ML version of the same principle — generalisation is what both brains and models must do.

See: [bistability in cortical neurons](../sizing_up_consciousness/bistability_in_cortical_neurons.md) · [structural MRI modalities](structural_mri_modalities.md)
