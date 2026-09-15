#core/appliedneuroscience

![pve-mri](_attachments/pve-mri.png)

The **partial volume effect (PVE)** occurs when finite spatial resolution causes multiple tissue types to contribute to one MRI voxel or to its effective point-spread function (PSF). It is common at tissue boundaries, such as grey/white matter interfaces, and in small structures.

## Causes and Mechanism

- **Voxel size and effective resolution**: Larger voxels and a broader effective PSF increase the opportunity for signal mixing. Structures whose dimensions approach the effective resolution are more vulnerable.
- **Tissue and geometry**: The magnitude and direction of PVE bias depend on tissue contrast, tissue fractions, structure geometry, boundary orientation, and noise, as well as registration, segmentation, and any partial-volume correction ([González Ballester et al., 2002](https://pubmed.ncbi.nlm.nih.gov/12494949/); [Manjón & Coupé, 2014](https://pmc.ncbi.nlm.nih.gov/articles/PMC4241492/)).
- **RF pulse imperfections**: Excitation of tissue outside the intended slice (cross-talk) can alter effective resolution and tissue signals; this is an acquisition effect that can compound, but is not identical to, geometric partial voluming.
- **Linear-mixture approximation**: In a simple two-tissue model,
  $$ S_V \approx f_A S_A + f_B S_B $$
  where _S_V_ is the voxel signal, _f_ is fractional tissue volume, and _S_ is tissue signal. This is a linear-mixture approximation, not a universal MRI signal model.

## Impact

1. **Quantitative measurements**: PVE can bias estimated volumes, cortical-thickness measurements, and tissue classifications. The magnitude and direction are not fixed; they depend on the acquisition, anatomy, and analysis pipeline.
2. **Other derived measures**: Tissue mixing can also bias [diffusion tensor imaging](diffusion_tensor_imaging.md) (DTI) metrics and contaminate tissue-specific or functional MRI analyses, including resting-state connectivity measures.

## Key Terms

- **Voxel**: 3D pixel; smaller voxels can reduce, but do not eliminate, PVE.
- **Cross-Talk**: Signal interference from adjacent slices.
- **Point-spread function (PSF)**: The effective spatial response of an acquisition and reconstruction; it can be broader than the nominal voxel dimensions.
- **Resolution threshold**: There is no universal MRI rule that structures below a fixed multiple of FWHM are necessarily underestimated. Small structures near the effective resolution are simply more susceptible to PVE bias.

> [!info] Takeaway
> PVE cannot generally be eliminated, but its effects can be reduced or modelled through acquisition choices, higher effective resolution, and partial-volume correction. It is important in neuroimaging and quantitative studies.

> [!example]
> A thicker slice can blend signals from adjacent tissues, whereas finer sampling can make boundaries more distinct; finer voxels do not remove all PVE.

## Sources

- [González Ballester et al. (2002)](https://pubmed.ncbi.nlm.nih.gov/12494949/)
- [Manjón & Coupé (2014)](https://pmc.ncbi.nlm.nih.gov/articles/PMC4241492/)
