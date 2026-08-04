#core/appliedneuroscience

- **Extracellular recording:** Measures electrical activity near neuron surface.
- **Intracellular recording:** Measures electrical activity inside a neuron. Invasive.
- **Single-channel recording:** Records ionic currents through individual [Ion channels](ion_channels.md). High resolution.

## Technique Hierarchy

From most to least invasive (and highest to lowest spatial resolution):

| Technique                             | Spatial Resolution | Temporal Resolution | Invasiveness |
| ------------------------------------- | ------------------ | ------------------- | ------------ |
| Patch clamp                           | Single channel     | μs                  | High         |
| [Field potential](field_potential.md) | Local circuit      | ms                  | Medium       |
| EEG/MEG                               | Whole brain        | ms                  | Low          |

## Trade-offs

- **Spatial vs temporal**: EEG has excellent temporal resolution (ms) but poor spatial localisation; fMRI has good spatial resolution but slow temporal dynamics.
- **Invasiveness vs detail**: Intracellular recordings provide the most detailed information about membrane potentials but require surgical access.

## Signal Sources

Neural electrical signals arise from [Types of biological electrical activity](types_of_biological_electrical_activity.md): action potentials, synaptic potentials, and oscillations. Surface recordings (EEG) primarily detect synchronised postsynaptic potentials in cortical pyramidal neurons, which create [dipoles](../06_neuroimaging_in_mental_health/dipoles_in_eeg.md) detectable at the scalp.
