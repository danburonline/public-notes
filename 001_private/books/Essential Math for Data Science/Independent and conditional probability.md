#core/machinelearning

## Independent [[Probability approaches|Probability]]

Independent probability refers to the **probability of an event occurring without any influence from any other event.** If the occurrence of one event does not affect the probability of the occurrence of another event, these events are said to be independent.

For two independent events A and B, the probability of both events happening, denoted as P(A ∩ B), is the product of the probabilities of each event:

```
P(A ∩ B) = P(A) * P(B)
```

### Example

Consider a fair coin and a fair die. Let’s say event A is getting a “Head” on the coin toss, and event B is getting a “6” on the dice roll. The probability of getting a “Head” (P(A)) is 1/2, and the probability of getting a “6” (P(B)) is 1/6. Since these are independent events, the probability of both events occurring is:

```
P(A ∩ B) = P(A) * P(B) = (1/2) * (1/6) = 1/12
```

## Conditional [[Probability approaches|Probability]]

Conditional probability is the **probability of one event occurring, given that another event has already occurred.** If we have two events, A and B, the conditional probability of A given B is denoted as P(A | B). It is calculated as:

```
P(A | B) = P(A ∩ B) / P(B)
```

This equation tells us that the conditional probability of A given B is the probability of A and B happening together, divided by the probability of B.

### Example

Consider a standard deck of 52 cards. Let’s say event A draws a king, and event B draws a heart. Now, these are dependent events if we draw a card without replacement.

Given that we drew a heart let’s calculate `P(A | B)`, the probability of drawing a king. There are 4 kings and 13 hearts in the deck. The intersection of hearts and kings is one card (the king of hearts), so `P(A ∩ B)` is `1/52`. `P(B)`` is `13/52`.

So, `P(A | B) = P(A ∩ B) / P(B) = (1/52) / (13/52) = 1/13`. This means that if we know we’ve drawn a heart, the probability that it’s a king is 1 out of 13.
