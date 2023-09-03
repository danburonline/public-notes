#core/mathematicalphysics #core/machinelearning

Bayes’ Theorem is a fundamental theorem in the field of statistics and probability. It **describes the probability of an event based on prior knowledge of conditions** that might be related to the event.

The theorem is named after [Thomas Bayes](https://en.wikipedia.org/wiki/Thomas_Bayes), who first provided an equation that allows new evidence to update beliefs.

## Formula

The formula for Bayes’ theorem is:

```
P(A|B) = [P(B|A) * P(A)] / P(B)
```

Where:
- `P(A|B)` is the posterior probability: the probability of event A occurring given that B is true.
- `P(B|A)` is the likelihood: the probability of event B occurring given that A is true.
- `P(A)` and `P(B)` are the probabilities of A and B independently of each other.

## Example

Let’s consider a simple example: testing for a disease.

Let’s say there’s a disease that affects 1% of the population (P(Disease) = 0.01). We have a test for this disease that’s 99% accurate (P(Positive|Disease) = 0.99). However, the test can also give false positives: in healthy individuals, the test will incorrectly be positive 2% of the time (P(Positive|Healthy) = 0.02).

Now, if a person tests positive, what’s the probability that they actually have the disease? Using Bayes’ theorem, we can calculate this.

```
P(Disease|Positive) = [P(Positive|Disease) * P(Disease)] / P(Positive)
```

We know that P(Positive|Disease) = 0.99 and P(Disease) = 0.01. However, we don’t yet know P(Positive), the probability of a positive test. We can calculate this as follows:

```
P(Positive) = [P(Disease) * P(Positive|Disease)] + [P(Healthy) * P(Positive|Healthy)]
            = [0.01 * 0.99] + [0.99 * 0.02] 
            = 0.0099 + 0.0198 
            = 0.0297
```

Now we can calculate P(Disease|Positive):

```
P(Disease|Positive) = [P(Positive|Disease) * P(Disease)] / P(Positive)
                    = [0.99 * 0.01] / 0.0297 
                    = 0.332
```

So, even if a person tests positive, there’s only a 33.2% chance that they actually have the disease.

This example highlights the importance of considering the base rate (P(Disease)) and the false positive rate when interpreting test results.
