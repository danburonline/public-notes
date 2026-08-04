#core/appliedneuroscience

![extracellular-recordings](_attachments/extracellular-recordings.png)

**Extracellular recording** measures electrical activity from outside the neuronal membrane — detecting signals propagated through the extracellular medium rather than via an intracellular electrode. Unlike [intracellular approaches](electrophysiology_measurements.md), it requires no membrane penetration, trading sub-threshold voltage resolution for the ability to monitor many neurons simultaneously across both [in vivo and in vitro](in_vivo_vs_in_vitro.md) preparations. The table above summarises five canonical configurations, differing in spatial scale, cell identifiability, and experimental constraints.

## Technique comparison

- **Field potentials** — sum the [synchronised activity](field_potential.md) of many neurons into a single local voltage trace. Excellent for network-level oscillations. Cannot resolve individual cells or membrane potential; summed synaptic currents (PSPs) are detectable as a population contribution but not at single-cell resolution. Recordable both in vivo and in vitro.
- **Whole nerve** — records the compound signal from a population of [axons](ion_channels.md). Subgroups can be separated by **conduction velocity** and **stimulus threshold**, but individual cells are not identifiable; PSPs and membrane potential remain inaccessible. Both in vivo and in vitro.
- **Multi-unit** — monitors a small cluster of nearby cells at once, offering a middle ground between population and single-cell resolution. Can characterise a single axon or neuron within the ensemble, and is recordable both in vivo and in vitro.
- **Single units** — isolates the spiking of a single (typically *putative*) neuron at a time, maximising spatial resolution; in practice often requires spike sorting to separate units recorded on the same electrode. Feasible in vitro and in vivo, though in vivo recordings are notably harder due to stability and targeting constraints.
- **MEAs (microelectrode arrays)** — dense grids of electrodes recording [network activity](types_of_biological_electrical_activity.md) from many cells at once while also resolving single units. Predominantly in vitro and **minimally invasive**, but individual cells cannot be targeted in advance.

> [!info] Shared limitation
> No extracellular configuration directly resolves **single-cell membrane potential** or **single-cell PSPs** — both require intracellular or patch-clamp access. Population synaptic currents do contribute to field potentials at the network level, but otherwise extracellular signals are dominated by **spikes** (action potentials). This is the defining trade-off against the [intracellular ladder](electrophysiology_measurements.md): breadth of observation in exchange for sub-threshold detail.

## Choosing a configuration

The choice is governed by three axes — **spatial scale** (network vs single cell), **environment** ([in vivo vs in vitro](in_vivo_vs_in_vitro.md)), and **cell identifiability**. Field potentials and whole-nerve recordings sacrifice cellular resolution for population context, whereas single-unit and multi-unit work zoom in at the cost of network information. [MEAs](types_of_biological_electrical_activity.md) bridge the two but remain largely an in vitro tool, making them the workhorse of cultured-network and slice studies where stable, long-term, multi-site recording is needed.
