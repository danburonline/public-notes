#fundamental/logic

Tense operators are used in temporal logic to reason about time and the order of events.

## Future Tense [[Logic operators|Operators]]

Future tense operators represent propositions that will be true at some point in the future.

- **Next Operator (X or N)**: Represents a proposition that will be true in the next state of the system.
    - Example: `X P` means “P will be true at the next moment in time”.
- **Eventually Operator (F or ◇)**: Represents a proposition that will be true at some point in the future.
    - Example: `F P` means “P will be true at some point in the future”.

## Past Tense Operators

Past tense operators represent propositions that were true at some point in the past.

- **Previously Operator (P or ◯)**: Represents a proposition that was true in the previous state of the system.
    - Example: `P P` means “P was true at the previous moment in time”.
- **Historically Operator (H or □)**: Represents a proposition that has been true at all points in the past.
    - Example: `H P` means “P has been true at all points in the past”.

These tense operators can be combined with logical operators like `AND`, `OR`, and `NOT` to create more complex temporal expressions. For example, `F (P AND Q)` would mean “P and Q will both be true at some point in the future”, while `H (NOT P)` would mean “P has never been true in the past”.
