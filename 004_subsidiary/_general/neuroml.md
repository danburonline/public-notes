#core/artificialintelligence #core/appliedneuroscience

NeuroML (Neuroscience Markup Language) is an **XML-based format for representing computational models of neural systems,** including their morphology, electrophysiology, and network connectivity. It enables exchange and reuse of [in silico](../../003_education/kings-college/01_techniques_in_neuroscience/in_silico.md) models across simulation environments — from single-compartment [Hodgkin-Huxley](../../003_education/epfl/02_computational_neuroscience/hodgkin-huxley_model.md) cells to multi-layer networks of [leaky integrate-and-fire neurons](../../003_education/epfl/02_computational_neuroscience/leaky_integrate-and-fire_neurons.md).

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

NeuroML is foundational to substrate-equivalence testing in [invariant brain emulation](../../002_profession/eightsix-science/invariant_brain_emulation.md): a model validated in NeuroML can in principle run on any compliant substrate, whether biological or synthetic. This underpins the engineering goals of [biomimetic neuromorphics](../../002_profession/eightsix-science/biomimetic_neuromorphics.md) and, at the flagship level, [ECP/PSNST](../../001_private/_general/psnst.md) — where a NeuroML representation of a patient's neural architecture would serve as the continuity-verification record across substrate migration.
