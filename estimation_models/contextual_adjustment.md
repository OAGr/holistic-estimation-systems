# Applying Contextual Adjustment

Contextual Adjustment is the adjustment of a probability distribution to represent a metric from the standpoint of an modeling agent. Typically, this is something an agent applies to probability distributions they themselves did not create, or ones they did create but with a slightly different meaning. These are practical when you obtain the probability distribution from a third party, external source, or old self estimate, and want to use them in a estimation model that represents your perspective.

### Third-Party Intuitive Estimates
**Calibration & Directional Biases**  
The third-party may be known to be biased in specific directions, or may be poorly calibrated. For instance, it is very common for people to be overconfident, so here this can be compensated for.

**Meaning Uncertainty**  
The third-party estimate may be meant to represent a different thing than the metric in question. This may be obviously different; for instance, their estimate could be for the "GDP per day" in the context of a leap day, while the metric is for a year without a leap day. It could also exist where it's not obvious that the meaning is different, but it seems likely. For instance, if the metric is vague ("Amount of bravery in the world"), it's likely the estimator held a different understanding of this metric than the agent.

###  Models
**Meaning Uncertainty**  
As in the adjustment factor for Intutive Estimates, it's possible a model is for a slightly different thing than an intended metric.

**Simplification**  
All models are simplifications. This may effect the answer. For instance, a [Spherical Cow](https://en.wikipedia.org/wiki/Spherical_cow) model could be useful. If it were compensated to add error to represent the lack of complexity, it should render a calibrated probability distribution, though not a particularly high resolution one.

**Mathematical Error**  
Large mathematical equations could have errors. The error rates for Excel spreadsheets have been studied and understood. The expected precense of errors should lead to a loss of resolution in contextual adjustment.
