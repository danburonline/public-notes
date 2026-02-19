#core/appliedneuroscience

The Talairach Atlas and the MNI/ICBM AVG152 template are pivotal tools in neuroimaging, providing a **standardised framework for reporting spatial coordinates of structural and functional brain images.** Developed from different methodologies, they’ve become standards for comparing and sharing research findings across studies.

---

## Talairach Atlas

![talairach-atlas](../../../_inbox/attachments/talairach-atlas.jpg)

- **Origin**: Developed by Jean Talairach and Pierre Tournoux, it’s based on a detailed postmortem study of a single 60-year-old French woman’s brain.
- **Structure**: It divides the brain into a three-dimensional grid, using an orthogonal coordinate system centred around the Commissural-Reference system (the anterior and posterior commissure points).
- **Usage**: Widely used for locating brain regions in PET and fMRI studies. It’s particularly noted for its detailed partitioning of the cerebral cortex into Brodmann areas.

---

## MNI/ICBM AVG152 Template

![mni_icbm152](../../../_inbox/attachments/mni_icbm152.jpg)

- **Origin**: Developed by the Montreal Neurological Institute (MNI) and the International Consortium for Brain Mapping (ICBM), this template is an average of 152 normal MRI scans.
- **Structure**: Provides a probabilistic atlas and a stereotaxic space for brain mapping. Unlike the Talairach atlas, which is based on a single brain, the AVG152 reflects variations across individuals, offering a more representative spatial context.
- **Usage**: Commonly used in fMRI and voxel-based morphometry studies. It’s favoured for its representation of a ‘standard’ brain and is often employed in automated spatial normalisation algorithms.

---

## Comparative Insights

- **Resolution & Detail**: The Talairach Atlas is known for its detailed cortical structure delineation, while the MNI/ICBM AVG152 is preferred for its probabilistic approach and representation of group characteristics.
- **Applicability**: While both are used for brain mapping, the choice between them may depend on the research question, with the Talairach being more suited for precise localisation and the MNI for broader population-based studies.
- **Transformation**: Tools like the Talairach Daemon and icbm2tal allow researchers to convert coordinates between the two systems, acknowledging their different origins and structural delineations.
