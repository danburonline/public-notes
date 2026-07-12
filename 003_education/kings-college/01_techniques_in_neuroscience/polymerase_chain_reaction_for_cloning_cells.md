#core/appliedneuroscience

![[polymerase-cloning.png]]

## Polymerase Chain Reaction (PCR) for cLoning

- **PCR amplifies a specific DNA sequence in vitro**, generating many copies of a target region from a small amount of template DNA.
- In cloning workflows, PCR is commonly used to **amplify a gene (insert) of interest** while optionally adding sequences needed for downstream assembly.

## Why PCR is Used before Cloning

- Enriches a specific target sequence from complex DNA (e.g., cDNA, genomic DNA, plasmid).
- Can add features via primer design, such as:
- Restriction enzyme sites
- Homology arms (Gibson/HiFi assembly)
- Tags or linkers (e.g., His-tag, fluorescent proteins)
- Mutations (site-directed mutagenesis strategies)

## What Happens after PCR (Typical cLoning fLow)

- PCR product is **purified** (to remove primers, nucleotides, polymerase).
- Insert is **assembled into a vector** (e.g., plasmid) using:
- Restriction digest + ligation, or
- Gibson/HiFi assembly, or
- TA cloning (depending on polymerase/end chemistry)
- Recombinant plasmid is **transformed into host cells** (commonly bacteria) for propagation.
- Clones are **verified** (e.g., colony PCR, restriction digest screen, Sanger sequencing).
- Verified construct can be used for **expression or further manipulation** in the target system.

## Quick Cautions

- Use a **high-fidelity polymerase** for cloning when sequence accuracy matters.
- Confirm insert sequence by **Sanger sequencing** before downstream experiments.
