#core/artificialintelligence

![iit](_attachments/iit.png)

**Integrated Information Theory (IIT)** proposes that consciousness *is* a system's capacity for irreducible cause-effect power — the degree to which a system specifies information about its own past and future states that cannot be decomposed into independent parts. Developed by psychiatrist and neuroscientist [Giulio Tononi](https://www.linkedin.com/in/giulio-tononi-1032b538), IIT is unusual among consciousness theories in starting from [phenomenology](../../003_education/kcl/03_mental_health_in_the_community/phenomenology.md) (what experience *is like*) and deriving mathematical constraints, rather than starting from neural mechanisms and asking when they produce experience.

## Phenomenological Axioms

IIT begins with five essential properties of every conscious experience, treating them as axioms any theory of consciousness must satisfy:

1. **Intrinsicality** — experience exists *for itself*, intrinsic to the experiencing subject, not dependent on an external observer. IIT terms this *intrinsic existence*.
2. **Composition** — experience is structured; it has phenomenal distinctions (colours, shapes, emotions) that compose the whole. These are *phenomenal distinctions*.
3. **Information** — each experience is specific; it rules out alternative possible experiences. The system specifies a *cause-effect structure* that differs from chance.
4. **Integration** — experience is unified; it cannot be decomposed into independent phenomenal components. The cause-effect structure must be *irreducible*.
5. **Exclusion** — experience is definite; it has a specific spatiotemporal grain. The cause-effect structure with maximal Φ defines the *main complex* of consciousness.

These axioms form the bridge between phenomenological description and information-theoretic formalism — they translate first-person properties of experience into mathematical constraints. See [naturalisation of phenomenology](../articles/naturalisation_of_phenomenology.md) for the broader bridging programme.

## Φ (Phi) — Integrated Information

- **Definition**: Φ quantifies the degree to which a system's cause-effect structure is irreducible — how much information the whole generates beyond the sum of its parts' independent information.
- **Calculation**: Computing Φ is computationally intractable for realistic neural systems (NP-hard in general). Practical approximations exist (pyphi toolbox, MICS algorithm) but full Φ for a human brain remains out of reach.
- **Interpretation**: Φ = 0 for purely feedforward systems and systems decomposable into independent parts. Φ > 0 indicates genuine causal integration. Φ reaches its maximum for the system's *main complex* — the constellation of elements that together specify the maximally irreducible cause-effect structure.
- **Substrate independence**: Φ is defined over causal structure — a system's mechanisms, their possible states, and the transition probabilities between them — not over a specific physical substrate. Any physical system realising the right cause-effect structure with non-zero Φ is, according to IIT, conscious. This makes Φ a theoretical candidate for a **substrate-independent consciousness quantity**, not an established clinical metric or a value read directly from ordinary EEG.

## Cause-Effect Structure and Intrinsic Causality

The central mathematical object in IIT is the **cause-effect structure** — a Φ-folded constellation of concepts in cause-effect space:

- Each mechanism within a system specifies a *cause repertoire* (what states could have caused its current state) and an *effect repertoire* (what states it can cause).
- A *concept* is the maximally irreducible cause-effect repertoire of a mechanism — a point in cause-effect space.
- The full cause-effect structure is the set of all concepts across the system, and is claimed to be **identical** to the quality of the experience (not merely correlated with it — this is IIT's strong identity claim).

This notion of **intrinsic causal structure** underlies IIT's critique of purely functional approaches: two systems with identical input-output mappings but different internal causal architectures may have different Φ values — and therefore, per IIT, different conscious experiences. This is directly relevant to the comparison between [Moravec transfer](../social/twitter/moravec_transfer.md) (which out-sources computation to a digital simulation, potentially stripping intrinsic causality) and [ECP/PSNST](../_general/psnst.md) (which preserves intrinsic causal structure in the replacement substrate). The mathematical contract for substrate equivalence is formalised in [invariant brain emulation](../../002_profession/eightsix/invariant_brain_emulation.md).

## IIT 4.0 (2019–Present)

The current formal presentation is [IIT 4.0](https://doi.org/10.1371/journal.pcbi.1011465).

The current formulation introduced several refinements over earlier versions:

- **System-intrinsic partition**: Earlier versions used a minimum information partition; 4.0 uses a partition based on *difference-making* rather than information-theoretic minimum.
- **Refined exclusion**: The main complex is identified via a maximal-Φ criterion that better handles nested systems.
- **Feedforward exclusion**: Pure feedforward architectures (e.g., standard deep neural networks) are assigned Φ = 0 regardless of their functional capabilities, because they lack recurrent causal structure.

## Emergence Status

Whether IIT's Φ is best understood as a case of [weak or strong emergence](strong_emergence.md) is actively debated:

- **Weak-emergence reading**: Φ is formally derivable from a system's transition probability matrix — given the right computation, it follows from the micro-level. Consciousness is a property of the *organisation* of matter, not of matter *per se*.
- **Strong-emergence reading**: The cause-effect structure has genuinely novel intrinsic existence — it is not merely a formal description but an additional ontological fact. Tononi's language of "intrinsic existence" is sometimes read as entailing strong emergence.

This classification carries direct stakes for [consciousness engineering](../_general/consciousness_engineering.md), but it does not by itself settle the realisation question. Reproducing the causal architecture in [biomimetic neuromorphic](../../002_profession/eightsix/biomimetic_neuromorphics.md) substrates may be sufficient only if no further substrate-specific or realisation requirements hold; if such requirements do hold, causal architecture alone may not suffice.

## Empirical Tests

### Perturbational Complexity Index (PCI)

The "zap-and-zip" method (Casali et al., 2013, [*Science Translational Medicine*](https://doi.org/10.1126/scitranslmed.3006294)) is motivated by integration-differentiation, without computing Φ directly. A TMS pulse to cortex is followed by high-density EEG; the Lempel-Ziv complexity of the binarised spatiotemporal response provided evidence for discriminating studied conscious and unconscious states, including reported detection of covert consciousness in behaviourally unresponsive patients. The reported PCI* threshold (around 0.31) is study- and protocol-dependent, not a universal consciousness boundary.

**Limitations**: PCI is a specific TMS–EEG perturbational complexity measure, not IIT's causal/intrinsic Φ, and it does not compute Φ. Casali et al.'s state-discrimination evidence is not proof of phenomenal consciousness, personal identity, or continuity. See [quantitative consciousness index](../papers/quantitative_consciousness_index.md) for the comparison of QCI components.

### COGITATE Consortium (2025)

The adversarial collaboration published in *Nature* in 2025 (n = 256; [source](https://www.nature.com/articles/s41586-025-08888-1)) tested predictions from IIT and GNWT. It reported content-specific synchronisation between frontal and early visual areas, while finding no sustained posterior synchronisation of the kind predicted by the tested IIT account. The results challenged key predictions of both theories; they did not settle which theory is correct. See [neural correlate of consciousness](../books/the_feeling_of_life_itself/neural_correlate_of_consciousness.md) for the full results.

### Hemispherotomy

[Patients surviving hemispherotomy](../books/sizing_up_consciousness/hemispherotomy.md) retain consciousness — an observation that IIT can accommodate in principle. Within IIT's framework, the remaining tissue might instantiate a main complex with non-zero Φ; this is a theoretical interpretation or hypothesis, not a calculated or measured result. Φ cannot currently be computed for real brains.

## Criticisms

- **Untestability**: Φ cannot currently be computed for real brains; the theory's predictions for large neural systems remain difficult to test in practice. COGITATE (2025) challenged the tested prediction of sustained posterior synchronisation, as well as key GNWT predictions, without settling either theory.
- **Panpsychism implication**: IIT implies any system with non-zero Φ is conscious, including simple logic gates (Φ ≈ 0.00001). Critics consider this a *reductio ad absurdum*.
- **Exclusion boundary problem**: IIT must select a spatiotemporal scale for the main complex, but why neuronal firing patterns rather than molecular dynamics or field potentials? The choice of neuronal grain appears theory-driven.
- **Missing content sensitivity**: Φ cannot distinguish between phenomenologically different experiences with equal Φ values — it may capture *level* of consciousness but not *content*.
- **Causal exclusion**: How IIT's intrinsic causal powers relate to [Kim's causal exclusion argument](strong_emergence.md) against downward causation remains contested.

## Relation to Consciousness Engineering

IIT occupies a strategic position in [consciousness engineering](../_general/consciousness_engineering.md):

- **Substrate independence**: Within IIT's framework, consciousness depends on causal architecture rather than biological substrate — a theoretical argument relevant to the feasibility of synthetic neural substrates for [PSNST](../_general/psnst.md), not an empirical demonstration of that feasibility.
- **Verification**: If the causal formalism could be instantiated for a system during progressive transfer, Φ might provide a theoretical quantity relevant to consciousness preservation. PCI and other proxies may provide indirect state-related evidence, but they do not verify Φ or personal identity and continuity.
- **Risk**: If IIT is correct that every causal mechanism contributes to experience, gradual substrate replacement must preserve not just global Φ but the specific cause-effect structure — a far more demanding constraint than preserving input-output function alone. The [Moravec transfer](../social/twitter/moravec_transfer.md), which outsources computation, may fail on these grounds.

## Related Concepts

- [Shannon information](../books/the_feeling_of_life_itself/shannon_information.md) — classical information theory; IIT extends beyond Shannon
- [Neural correlate of consciousness](../books/the_feeling_of_life_itself/neural_correlate_of_consciousness.md) — empirical search programme; IIT provides one theoretical framework
- [Higher-order theories of consciousness](../books/sizing_up_consciousness/higher-order_theories_of_consciousness.md) — competing theory; see comparison
- [Access and phenomenal consciousness](access_and_phenomenal_consciousness.md) — IIT targets phenomenal, not access consciousness
- [Strong emergence](strong_emergence.md) — whether Φ is weakly or strongly emergent is debated
- [Phenomenology](../../003_education/kcl/03_mental_health_in_the_community/phenomenology.md) — IIT's axiomatic method is explicitly phenomenological
- [Naturalisation of phenomenology](../articles/naturalisation_of_phenomenology.md) — IIT as a mathematical bridge between first- and third-person methods
- [Philosophical zombies](../_general/philosophical_zombies.md) — IIT denies zombies are possible: any system with the right Φ is conscious
- [PSNST](../_general/psnst.md) — conceptual relevance of Φ to substrate-preservation questions, not a current monitoring or verification method
- [Moravec transfer](../social/twitter/moravec_transfer.md) — digitisation approaches risk losing intrinsic causal structure (Φ → 0)
