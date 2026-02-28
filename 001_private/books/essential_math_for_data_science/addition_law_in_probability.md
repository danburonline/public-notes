#core/artificialintelligence

The addition law in probability is a **fundamental concept that describes the probability of the union of two events.**

## Mutual Exclusivity

For any two events, `A` and `B`, that cannot occur simultaneously (i.e., they are mutually exclusive), the addition law can be expressed as follows:

```
P(A ∪ B) = P(A) + P(B)
```

In this equation, “∪” represents the union of two events, i.e., the event that `A`, `B`, or both occur.

### Example

Consider a single roll of a standard six-sided die, and let `A` be the event that the roll is an even number and `B` the event that the roll is a 5. Since `A` and `B` cannot both occur at the same time, they are mutually exclusive. The probability of rolling a 5 or an even number is:

```
P(A ∪ B) = P(A) + P(B) = 1/2 + 1/6 = 2/3
```

## Non-Mutual Exclusivity

When the events are not mutually exclusive (i.e., they can both occur at the same time), the addition law is adjusted to account for the overlap. The equation becomes:

```
P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
```

In this equation, “∩” represents the intersection of two events, which is the event that both `A` and `B` occur.

### Example

Consider a single card drawn from a standard deck of 52 cards, and let `A` be the event that the card is a heart and `B` the event that the card is a queen. Since a card can be both a heart and a queen, these events are not mutually exclusive. The probability of drawing a heart or a queen is:

```
P(A ∪ B) = P(A) + P(B) - P(A ∩ B) = 13/52 + 4/52 - 1/52 = 16/52 = 4/13
```

To calculate the probability of the union of more than two events, these formulas can be applied iteratively.
