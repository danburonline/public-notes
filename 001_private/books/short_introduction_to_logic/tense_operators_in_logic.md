#fundamental/logic

Tense operators are central to temporal logic, which **extends classical logic to reason explicitly about time and the temporal ordering of events.**

## Types of Tense Operators

### Future Tense Operators

Future tense operators describe propositions concerning future states or events.

- **Next Operator ($X$ or $N$):** $X P$ means “$P$ will be true at the next moment in time.”  
  - Formal: $X P$ is true at time $t$ if $P$ is true at time $t+1$.
- **Eventually Operator ($F$ or $\Diamond$):** $F P$ means “$P$ will be true at some point in the future.”  
  - Formal: $F P$ is true at time $t$ if there exists a future time $t' \geq t$ such that $P$ is true at $t'$.
- **Always Operator ($G$ or $\Box$):** $G P$ means “$P$ will be true at all points in the future.”  
  - Formal: $G P$ is true at time $t$ if $P$ is true at every future time $t' \geq t$.

### Past Tense Operators

Past tense operators describe propositions about prior states or events.

- **Previous Operator ($P$ or $O$):** $P P$ means “$P$ was true at the previous moment in time.”  
  - Formal: $P P$ is true at time $t$ if $P$ was true at time $t-1$.
- **Once Operator ($F^-$ or $\Diamond^-$):** $F^- P$ means “$P$ was true at some point in the past.”  
  - Formal: $F^- P$ is true at time $t$ if there exists a past time $t' \leq t$ such that $P$ was true at $t'$.
- **Historically Operator ($H$ or $\Box^-$):** $H P$ means “$P$ has always been true in the past.”  
  - Formal: $H P$ is true at time $t$ if $P$ was true at every past time $t' \leq t$.

## Usage and Combination

Tense operators can be combined with classical logical operators (such as $AND$, $OR$, $NOT$) to form complex temporal statements:

- $F (P \wedge Q)$: “$P$ and $Q$ will both be true at some point in the future.”
- $H (\neg P)$: “$P$ has never been true in the past.”
- $G (P \rightarrow Q)$: “Whenever $P$ is true in the future, $Q$ will also be true.”

## Notes

- The specific symbols used for tense operators ($X$, $F$, $G$, $P$, $H$, etc.) may vary between different temporal logic systems.
- Temporal logic is widely used in computer science (especially in model checking and verification), philosophy, linguistics, and artificial intelligence.