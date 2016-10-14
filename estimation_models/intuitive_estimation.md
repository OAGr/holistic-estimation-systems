# Intuitive Estimation && Intuitive Intervals

## Fitting intuitions into Probability Distributions

Estimation models use probability distributions, but individual intuitions typically don't come in the form of complete distributions. In order to account for this, we need to approximate these distributions.

Probability distributions that perfectly represent intuitive beliefs are an [active topic of research](https://en.wikipedia.org/wiki/Bayesian_probability#Personal_probabilities_and_objective_methods_for_constructing_priors). This paper does not claim that simple fits to distribution shapes are perfect, but rather that they are useful approximation. We posit that error caused by these simplifications is often minor compared to other errors in an estimation system. As new research is produced, it may make sense to use other kinds of fitting functions instead.

One simple way that distributions can be approximated is by fitting confidence intervals to distribution shapes. This method can be quite convenient; individuals offer what is essentially an "upper" and "lower" bound, then this can get matched to a likely shape. In particular, the 'upper' and 'lower' bounds could represent specific percentiles; i.e. the 95th and 5th percentiles of expected outcomes.

The subjects of percentile estimation and calibration are well explained in [How to Measure Anything](https://www.amazon.com/How-Measure-Anything-Intangibles-Business/dp/1118539273/ref=sr_1_1?ie=UTF8&qid=1476478084&sr=8-1&keywords=how+to+measure+anything.) Individuals often begin estimates as overconfident, but with some training can become 'correctly calibrated' for a specific set of questions.

One challenge when interpreting individual estimates as probability intervals is to distinguish between individuals estimating specific parameters directly, and them estimating the probability distribution of a separate random variable. For instance, someone guessing that the "Number of cows in India" was between "30K and 200K" would have made a singular direct estimate, but if they would attempt to estimate the "height of a random person in a specific group" by generating a probability distribution of the heights within that group, that would be considered an estimate on the function of a random variable.

**Direct Estimate Examples**
"I think the number of baseball games last year was between 3,000 and 20,000."
"I think the amount of revenue my business will make this year is between $14,000 and $40,000."

**Indirect Estimates of Random Variable Examples**
"I think that the degree the clock will land on is uniformly distributed between 0 and 360."
"I think that the number of phone calls they receive per hour is represented by a poisson distribution."

## Log Normal Distributions

Classical log normal distributions cannot be 0 or negative, and have long tails to the right. These fit well for estimates following similar constraints. For instance, a human estimate of "the number of pianos in Chicago" cannot be negative and seems to have a greater likelihood of being significantly above an expected median then below.

As a general heuristic, we estimate that the majority of estimates made by humans that must be above zero, can be better fit by a log normal distribution than by a Normal Distribution.

Log normal distributions have two degrees of freedom, and thus can fit easily to a set of 5th and 95th percentiles.

## Normal Distributions

Normal distributions are symmetric. Unlike log normal distributions they can be below zero. They are somewhat of a second choice to log normal distributions.

## Uniform Distributions

Uniform distributions are useful at representing exact ranges, but imply the lack of any uncertainty. Thus they seem more useful for describing the world than representing an uncertain estimate. One option would be to use log normal or normal distributions as the lower and upper bounds.

Uniform distributions are simple but seem rare in many human estimates, at least in comparison to log normal and normal distributions. In the cases they are useful it makes more sense to use a 0% and 100% percentiles, as they typically are meaningful.

## Bimodal Distributions

There are some cases where a parameter is seen as being bimodal. These cases often reveal a more complex breakdown, which can often be represented better as multiple other distributions formally combined.

For instance, say one attempts to estimate the GDP next year, but there's an important election happening that could dramatically impact the result. In that case they may believe the result would follow a distribution with two humps. One way of approximating them would be for that person to make a log normal or normal distribution for each of the two outcomes, then for them to explicitly model the chances that each situation would be the case with a third distribution. These can be combined to make a bimodal distribution that reasonably represents that of the estimator.

In cases where they are broken up, the creation of the bimodal distribution represents an explicit model with a few distinct metrics. Rather than having each estimator come up with this from scratch, we recommend formally splitting it up so that each parameter can be estimated on by different participants.

## Other Distributions

There are many other kinds of distributions, but these typically 
