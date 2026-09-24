#core/appliedneuroscience #core/artificialintelligence

NeuroML (Neuroscience Markup Language) is an **XML-based representation and exchange standard for computational models of neural systems,** including their morphology, electrophysiology, and network connectivity. It can cover different model abstractions, including the [point-neuron model](../../002_profession/bluebrain/point_neuron.md) discussed in the [Model Hierarchy](../../003_education/kcl/01_techniques_in_neuroscience/in_silico.md#model-hierarchy). It enables exchange and reuse of [in silico](../../003_education/kcl/01_techniques_in_neuroscience/in_silico.md) models across simulation environments — from a single-compartment [Hodgkin-Huxley](../../003_education/epfl/hodgkin-huxley_model.md) example to multi-layer networks of [leaky integrate-and-fire neurons](../../003_education/epfl/leaky_integrate-and-fire_neurons.md). NeuroML does not itself resolve the trade-off between biological fidelity and computational scale or cost; those depend on the selected model and simulation.

```xml
<?xml version="1.0"?>
<neuroml xmlns="http://www.neuroml.org/schema/neuroml2"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://www.neuroml.org/schema/neuroml2 https://raw.githubusercontent.com/NeuroML/NeuroML2/development/Schemas/NeuroML2/NeuroML_v2beta4.xsd">

  <!-- Define a simple single-compartmental neuron with Hodgkin-Huxley type ion channels -->
  <cell id="hhcell" name="HHCell">
    <morphology>
      <segment id="soma" name="soma" compartment="true">
        <proximal/>
        <distal/>
        <parent segment="soma"/>
      </segment>
    </morphology>
    <biophysicalProperties>
      <membraneProperties>
        <!-- Sodium ion channels -->
        <channelDensity id="na" ion="na">
          <conductance density="120.0 pS/um2"/>
          <HHRateChannel id="na_hh" gMax="120.0 pS/um2"/>
        </channelDensity>
        <!-- Potassium ion channels -->
        <channelDensity id="k" ion="k">
          <conductance density="36.0 pS/um2"/>
          <HHRateChannel id="k_hh" gMax="36.0 pS/um2"/>
        </channelDensity>
        <!-- Leak conductance -->
        <leak conductance="0.3 mS/cm2" erev="-54.3 mV"/>
      </membraneProperties>
    </biophysicalProperties>
  </cell>

</neuroml>
```

## Applications in Brain Emulation

NeuroML can support reproducibility, exchange and comparison in work on [invariant brain emulation](../../002_profession/eightsix/invariant_brain_emulation.md), [biomimetic neuromorphics](../../002_profession/eightsix/biomimetic_neuromorphics.md), and [ECP/PSNST](../../001_private/_general/psnst.md). A NeuroML representation of neural architecture may serve as a record for comparison or migration planning, but it cannot establish substrate equivalence, personal identity or continuity on its own, nor guarantee execution on any particular substrate.
