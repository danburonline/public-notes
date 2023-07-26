#fundamental/logic 

A truth table is a mathematical table used in logic to compute the functional values of logical expressions on each of their functional arguments. It is used to depict the possible outcomes of a particular proposition or combination of propositions. The primary logical operators are ``NOT``, ``AND``, ``OR``, ``IF...THEN`` (implies), and ``IF AND ONLY IF`` (biconditional).

**2. Logical Operators:**

- **NOT (¬)**: This is a unary operator, meaning it operates on a single logical value. NOT p (¬p) is true if p is false, and vice versa.
- **AND (∧)**: This is a binary operator, meaning it operates on two logical values. p AND q (p ∧ q) is true if and only if both p and q are true.    
- **OR (∨)**: This is also a binary operator. p OR q (p ∨ q) is true if either p is true, q is true, or both p and q are true.
- **IF...THEN (→)**: This is a binary operator. IF p THEN q (p → q) is true unless p is true and q is false. It is also known as 'implies' or 'conditional'.
- **IF AND ONLY IF (↔)**: This is a binary operator. p IF AND ONLY IF q (p ↔ q) is true if both p and q have the same truth value. It is also known as biconditional or equivalence.

**3. Truth Tables:**

Here are the basic truth tables for the logical operators mentioned above:

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

- **IF...THEN (→):**

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

**4. [[Number systems#Complex Numbers|Complex]] Expressions:**

Truth tables can also be used for complex logical expressions, not just individual operators. For example, the expression p ∧ (q ∨ r) can be evaluated using a truth table. Remember, when evaluating complex expressions, evaluate the innermost parentheses first. In the example above, you'd first evaluate q ∨ r and then combine that with p ∧.