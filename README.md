# Audio Decoding by Inverse Problem Solving

This is the demonstration page of the paper "Audio Decoding by Inverse Problem Solving" with the samples used for the MUSHRA-style listening tests.

## Info

### Abstract

We consider audio decoding as an inverse problem and solve it through diffusion posterior sampling. Explicit conditioning functions are developed for input signal measurements provided by an example of a transform domain perceptual audio codec. Viability is demonstrated by evaluating arbitrary pairings of a set of bitrates and task-agnostic prior models. For instance, we observe significant improvements on piano while maintaining speech performance when a speech model is replaced by a joint model trained on both speech and piano. With a more general music model, improved decoding compared to legacy methods is obtained for a broad range of content types and bitrates. The noisy mean model, underlying the proposed derivation of conditioning, enables a significant reduction of gradient evaluations for diffusion posterior sampling, compared to methods based on Tweedie's mean. Combining Tweedie's mean with our conditioning functions improves the objective performance.

### Reference

Pedro J. Villasana T., Lars Villemoes, Janusz Klejsa, Per Hedelin  (2024). **Audio Decoding by Inverse Problem Solving**.
