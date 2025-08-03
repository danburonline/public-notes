#core/appliedneuroscience 

The butcher number, a metric introduced in neural interface research and adapted from Prof. Markus Meister, **quantifies the efficiency and invasiveness of intracortical recording probes by calculating the ratio of neurons destroyed (the "butcher" cost) to neurons successfully recorded.** It highlights the trade-off between scaling up neural recordings for brain-computer interfaces (BCIs) and minimising tissue damage, with an ideal value much less than 1 to enable comprehensive, non-destructive sampling of cortical activity without compromising brain function.

## Key Concepts

- **Definition and Calculation**: Defined as neurons killed per recorded neuron; includes acute damage (from initial implantation, estimated geometrically via probe volume and neuron density ~92,000/mm³) and chronic damage (from foreign body response, FBR). Focus often on acute phase, as chronic effects can be mitigated with biocompatible designs.
- **Acute vs. Chronic Butcher Number**: Acute: Immediate loss from probe insertion (e.g., displacement, bleeding). Chronic: Ongoing loss from inflammation, gliosis, or micromotion; advanced probes aim to reduce this via miniaturisation and flexibility.
- **Theoretical Scenarios**: "Tolerant" (100 cells/electrode, 64 µm sensing distance) vs. "Strict" (3 cells/electrode, 20 µm distance); requires sub-micrometer shanks to limit volume displacement.
- **Limitations**: Current probes (e.g., rigid silicon) often exceed 1 due to buckling, FBR, and vascular damage; flexible probes with shuttles still face insertion constraints.

## Examples from Probe Technologies

| Probe Type                  | Example           | Acute Butcher Number | Notes                                                 |
| --------------------------- | ----------------- | -------------------- | ----------------------------------------------------- |
| Rigid Self-Supporting       | Utah Array        | ~10-100              | High due to shank spacing and kill zones.             |
| Flexible with Shuttle       | Neuralink Threads | ~1-5                 | Reduced FBR but shuttle damage persists.              |
| Biohybrid/Living Electrodes | μTENN Constructs  | Potentially <1       | Forms synapses without large disruption; early stage. |

- **Implications for Scaling**: Butcher number <1 disrupts networks; goal for all-neuron recording requires %3C%3C1 to avoid widespread reorganisation or bleeding from dense vasculature.

> [!note] Insight on Future Directions
> Achieving a butcher number <<1 demands paradigm shifts like growth-based implantation (e.g., biohybrid fibres) over rigid insertion, avoiding capillaries and FBR while controlling synapse formation for targeted sampling.