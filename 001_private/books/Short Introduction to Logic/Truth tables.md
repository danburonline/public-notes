#fundamental/logic 

A truth table is a mathematical table used in logic to compute the functional values of logical expressions on each of their functional arguments. It is used to depict the possible outcomes of a particular proposition or combination of propositions. The primary logical operators are ``NOT``, ``AND``, ``OR``, ``IF…THEN`` (implies), and ``IF AND ONLY IF`` (biconditional).

Here are some basic truth tables:

- **NOT (¬):**

|p|¬p|
|---|---|
|T|F|
|F|T|

- **AND (∧):**

|p|q|p ∧ q|
|---|---|---|
|T|T|T|
|T|F|F|
|F|T|F|
|F|F|F|

- **OR (∨):**

|p|q|p ∨ q|
|---|---|---|
|T|T|T|
|T|F|T|
|F|T|T|
|F|F|F|

- **IF…THEN (→):**

|p|q|p → q|
|---|---|---|
|T|T|T|
|T|F|F|
|F|T|T|
|F|F|T|

- **IF AND ONLY IF (↔):**

|p|q|p ↔ q|
|---|---|---|
|T|T|T|
|T|F|F|
|F|T|F|
|F|F|T|

## [[Number systems#Complex Numbers|Complex]] Expressions

Truth tables can also be used for complex logical expressions, not just individual operators. For example, the expression p ∧ (q ∨ r) can be evaluated using a truth table. Remember, when evaluating complex expressions, evaluate the innermost parentheses first. In the example above, you'd first evaluate q ∨ r and then combine that with p ∧.