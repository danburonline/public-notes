#core/appliedneuroscience 

![dti](../../../_inbox/attachments/dti.png)

Diffusion Tensor Imaging (DTI) is a **neuroimaging technique that measures the diffusion of water molecules in brain tissue.** It provides insights into the structural organisation of brain regions, particularly white matter tracts. DTI is often used for [Diffusion tensor tractography](../../../003_education/kings-college/04%20Biological%20Foundations%20of%20Mental%20Health/Diffusion%20tensor%20tractography.md), which maps the trajectory and connectivity patterns of neural fibers by analyzing water diffusion along them.

## Key Concepts

### Fractional Anisotropy (FA)

- **Definition**: FA quantifies the degree to which water diffusion is directionally dependent.
  - **Low FA**: Represents isotropic diffusion, where water diffuses equally in all directions. This is typical in areas like cerebrospinal fluid (CSF).
  - **High FA**: Represents anisotropic diffusion, where water preferentially diffuses along certain directions, such as parallel to white matter fiber tracts.
  - **Intermediate FA**: Found in grey matter, where diffusion has some directional preference but less organisation than white matter.

### Axial Diffusivity (AD)

- **Definition**: Measures water diffusion along the strongest direction of diffusion (the longest axis of the ellipsoid). 
- **Significance**: AD reflects the integrity of axonal structures within white matter.

### Radial Diffusivity (RD)

- **Definition**: Measures water diffusion perpendicular to the strongest direction of diffusion (the shorter axes of the ellipsoid).
- **Significance**: RD is associated with myelin integrity; changes may indicate demyelination or other pathological processes.

---

## Image Analysis

### Brain Regions

The attached image illustrates diffusion tensors in different brain regions:
1. **CSF Region**:
   - Diffusion tensors are spherical, indicating isotropic diffusion (low FA).
   - Water molecules diffuse equally in all directions due to the lack of structural barriers.
2. **Gray Matter Region**:
   - Diffusion tensors are moderately elongated ellipsoids, reflecting intermediate FA.
   - Water has some directional preference but less structural organisation compared to white matter.
1. **White Matter Region**:
   - Diffusion tensors are highly elongated ellipsoids, indicating anisotropic diffusion (high FA).
   - Water predominantly diffuses along axonal fiber tracts.

### Diffusion Metrics

- The ellipsoids represent diffusion tensors:
  - **Shape**: Indicates the degree of anisotropy.
    - Spherical shapes = isotropic diffusion.
    - Elongated shapes = anisotropic diffusion.
  - **Size**: Reflects the magnitude of diffusivity.
- Colors represent principal diffusion directions:
  - Different colours correspond to different spatial orientations of water movement.