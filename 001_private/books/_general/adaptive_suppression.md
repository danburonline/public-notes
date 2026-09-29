#core/artificialintelligence

In signal processing, **adaptive suppression** describes adjusting a system's parameters to reduce unwanted interference as conditions change. Here it is a descriptive label, not the name of one specific algorithm.

## Example: Adaptive Noise Cancellation

An adaptive filter uses a reference input correlated with the unwanted noise, but ideally uncorrelated with the desired signal, to estimate the noise contaminating a recording. This estimate is subtracted from the recording; the residual output provides the error signal used to update the filter.

For example, this can reduce electrical mains interference in an electrocardiogram. Performance depends on the reference and the filter's ability to track changes: cancellation is not guaranteed, and desired-signal contamination of the reference can cause distortion.

## Source

- Widrow et al. (1975), [*Adaptive Noise Cancelling: Principles and Applications*](https://isl.stanford.edu/~widrow/papers/j1975adaptivenoise.pdf), especially §§III–V.
