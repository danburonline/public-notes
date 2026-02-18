#core/appliedneuroscience

In fMRI, image quality is affected by the **balance between spatial and temporal resolution, signal-to-noise ratio (SNR), and susceptibility to various artefacts.** Optimising these factors is essential for producing accurate and interpretable neuroimaging data.

## Spatial Vs Temporal Resolution Trade-off

The fundamental tension in fMRI acquisition:

- **Spatial resolution** determines the precision with which brain regions can be localised (typically 1–4 mm³ voxels)
- **Temporal resolution** determines how finely changes in brain activity can be tracked over time (typically 0.5–3 seconds per volume)

Increasing one typically compromises the other due to acquisition time constraints. High spatial resolution requires smaller voxels, which take longer to acquire, reducing temporal sampling rate.

## Signal-to-Noise Ratio (SNR)

SNR is critical for detecting the relatively weak [BOLD signal](The%20BOLD%20effect.md) changes (typically 1–5% signal change). Key factors affecting SNR:

| Factor | Effect on SNR |
|--------|---------------|
| Magnetic field strength | Higher field (3T vs 1.5T) increases SNR roughly linearly |
| Voxel size | Larger voxels increase SNR but reduce spatial resolution |
| Repetition time (TR) | Longer TR allows more signal recovery but reduces temporal resolution |
| Number of averages | More repetitions improve SNR but increase scan duration |
| Receiver coil | Multi-channel coils improve SNR via parallel imaging |

## Common Artefacts

### Motion Artefacts

Even small head movements (< 1 mm) can introduce substantial errors, as the [BOLD signal](The%20BOLD%20effect.md) change is small. Mitigation strategies include:

- Prospective motion correction
- Retrospective realignment algorithms
- Head restraints and participant training

### Susceptibility Artefacts

Air-tissue interfaces (e.g., near sinuses, ear canals) cause magnetic field inhomogeneities leading to:

- Signal dropout in orbitofrontal and anterior temporal regions
- Geometric distortions

### Physiological Noise

Cardiac and respiratory cycles introduce systematic signal fluctuations unrelated to neural activity, particularly problematic at higher field strengths where BOLD sensitivity increases but so does physiological noise.

## Field Strength Considerations

| Field Strength | Advantages | Disadvantages |
|----------------|------------|---------------|
| 1.5T | Lower cost, fewer susceptibility artefacts | Lower SNR and BOLD contrast |
| 3T | Good balance of SNR and practicality | Increased susceptibility artefacts |
| 7T+ | Excellent spatial resolution, strong BOLD | Severe susceptibility artefacts, SAR limits, high cost |

## Relation to Other Concepts

- [The BOLD effect](The%20BOLD%20effect.md): The signal being measured
- [Initial dip in BOLD signal](Initial%20dip%20in%20BOLD%20signal.md): Early transient affecting temporal dynamics
- [Cognitive subtraction](Cognitive%20subtraction.md): Experimental design to isolate signal of interest
- [Multi-modal imaging](Multi-modal%20imaging.md): Combining fMRI with other modalities to overcome limitations
- [Comparison of neuroimaging methods](Comparison%20of%20neuroimaging%20methods.md): How fMRI compares to alternative techniques
