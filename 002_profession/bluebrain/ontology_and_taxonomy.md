#lead/computationalphilosophy #core/artificialintelligence #core/softwaredevelopment

**Ontology** has two relevant senses:

- **Philosophical ontology** is the branch of metaphysics concerned with being and existence: what kinds of entities, properties, and relations there are ([SEP, “Metaphysics”](https://plato.stanford.edu/entries/metaphysics/)).
- **Knowledge-representation ontology** is an explicit account of the concepts, entities, properties, and relations in a domain, together with their meanings, constraints, and inferential commitments. Formal and machine-readable applies to particular representations encoded in formalisms such as OWL 2, not to every ontology in every sense ([W3C, “OWL 2 Web Ontology Language: Document Overview”](https://www.w3.org/TR/owl2-overview/)).

## Taxonomy

A **taxonomy** is a controlled classification that organises items into categories, commonly using broader–narrower hierarchical relationships. It applies to domains beyond biology, including information and technical systems; controlled vocabularies can provide the terminology and structure for such classifications ([NISO, ANSI/NISO Z39.19](https://doi.org/10.3789/ansi.niso.z39.19-2005R2010)).

## Comparison

| Aspect | Taxonomy | Ontology |
|---|---|---|
| Main organisation | Usually a hierarchy of categories or labels | An explicit domain model that may include a hierarchy |
| Relations | Mainly broader–narrower or class-subclass relations | Typed relations such as causal, spatial, temporal, and part–whole relations |
| Membership | Places items in categories | Distinguishes classes from explicit individuals or instances and their class membership |
| Constraints | Usually limited to classification rules | Can state properties and constraints such as disjointness, cardinality, domain, and range |
| Inference | Supports category navigation and retrieval | May support logical inference from its stated meanings and constraints |

A taxonomy can therefore be embedded as the class hierarchy within a richer ontology. The [knowledge graphs](knowledge_graphs.md) note shows how entities and relations can be represented, while [RDF and RDFS](../../001_private/books/knowledge_graphs/rdf_vs_rdfs.md) illustrates related formal vocabulary and hierarchy mechanisms; neither formalism defines ontology in every philosophical or informal sense.

## Illustrative Neuroscience Example

An illustrative taxonomy might arrange **neuron → inhibitory neuron → GABAergic interneuron → parvalbumin-positive interneuron**. This is an example of hierarchical classification, not a claim about a universal cell-type schema; see [neuronal cell types](../../003_education/kcl/01_techniques_in_neuroscience/neuronal_cell_types.md) for related terminology.

An ontology could additionally represent a cell type’s relations to a brain region and cortical layer, marker properties, neurotransmitter, developmental lineage, and supporting evidence. It could also state which relations and memberships are permitted, rather than merely assigning a label.

## Blue Brain Relevance

For Blue Brain work, the distinction separates a useful classification of domain items from the richer representation of entities, relationships, and constraints. It clarifies what is being grouped, what is being asserted about those items, and what inferences a formal representation may support without assuming that Blue Brain uses one particular ontology.

## Sources

- [SEP, “Metaphysics”](https://plato.stanford.edu/entries/metaphysics/)
- [W3C, “OWL 2 Web Ontology Language: Document Overview”](https://www.w3.org/TR/owl2-overview/)
- [NISO, ANSI/NISO Z39.19](https://doi.org/10.3789/ansi.niso.z39.19-2005R2010)
