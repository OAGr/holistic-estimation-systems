# Estimation Model Terminology

## Metrics & Estimates
Metrics are specific things that can be estimated.  Estimates are numbers, ranges, or probability distributions that approximate those metrics.

For instance, Sophia may estimate that her business will have between 200 and 500 customers tomorrow. The "number of customers in Sophia's business tomorrow" would be the metric, and the approximation of "200 and 500" is one available estimate of that metric.

There could be many ways of estimating one metric. In addition to Sophia's estimate, her business partner Frank may provide a different one. There may also be a small numeric model that uses other metrics to estimate this one. These can be combined using either an algorithm or one person's intuition from taking the existing estimates into account.

## Different Kinds of Estimates
There are a few ways for obtaining an estimate.

### Function Outputs
Functions can use the values of some metrics to estimate other metrics. These are discussed further below.

### Intuitive Estimates
Individuals can estimate metrics directly. If the individual who has produced the estimate is not the same one as that doing or analyzing the results, contextual adjustment can be used.

### Statistics
Specific statistics can be used to estimate metrics.  However, unless the metric is defined as being identical to that statistic, contextual adjustment should be used to account for its expected error. For example, there may be a report that stated there were 3800 car injuries in California in 2008. This should not be used directly in an estimate of the number of injuries in California in 2008 as a metric, because the number is likely to be not completely correct. The whole number (3800) implies that there was rounding, it may have been undercounted or overcounted, they may have used a definition for accident different than in the rest of the model, and so on.

Statistics can be updated dynamically from external sources.  However, if this happens, the adjustment factor may have to result in more uncertainty in order to accommodate for future changes in context.

## Contextual Adjustment
Even in the case where there exists only one estimate of a metric, the party documenting it may not completely trust it.  Say that Sophia doesn't know much about the number of customers tomorrow, but does hear about Frank's estimate.  She knows Frank quite well and realizes that he's generally quite good at estimating, but is often both overconfident and optimistic.  Thus, from her perspective, the value of the metric is not equal to Frank's estimate, but is in fact slightly different. She can use what we call a **contextual adjustment** to estimate this metric using Frank's estimate.

In other cases she may have estimates from sources that are known to be extremely biased. These still represent information, but should be adjusted heavily to represent the best estimate of this metric that Sophia would consider reasonable.

This brings up the point that all adjustment factors would vary depending on the observer or analyzer. One ideal is to come up with one reasonable perspective that a group could come to consensus on. The purpose of Large Estimation Systems is not to create objective models of reality, but instead to best approximate metrics with the use of human analysis.  Human perception and analysis is very often biased; we believe this should be accounted for and minimized as part of the modeling process.

## Applied Functions
Applied functions are mathematical relationships between some metrics and others. For instance, the force of object A is equal to the mass of that object times it's acceleration.

Some applied functions are completely certain, as common in a priori knowledge.  The number of large pears and small pairs I have is equal to the sum of the two, with zero additional uncertainty.

But many other applied functions are not completely certain or can be expected to be incorrect to various extents.  In these cases adjustment factors can be used to account for their biases, and arrive at the expected conclusions.

For instance, Newton's laws do not take into account relativistic effects. In many cases the expected error that this would create is not significant in the context of the problem, but in others a more accurate set of equations would be beneficial. If one is familiar with the class of inputs that are being dealt with, they could approximate the error of Newton's equations for specific questions. In this sense; it's not interesting in itself that Newton's laws are 'wrong'; what matters is how useful they are in approximating questions and making decisions.

There is a difference between applied and theoretical functions.  A theoretical function is one that applies to any set of metrics that match a set of specifications.  A applied function is a theoretical function applied for specific metrics. Adjustment factors can be applied more narrowly to applied functions than theoretical ones. Unless specifically stated otherwise, in this paper when we describe functions we refer to applied functions.


## Probability Distributions
While uncertain estimates could be represented by ranges or by numbers, it is much more precise to use probability distributions. It's generally difficult to understand what is not measured; in the cases of large approximation systems, uncertainty can cascade through many stages and become very large, so it is particularly important to have a good grasp on how much of it exists and where.  For this reason we suggest that large approximation systems should use probability distributions for metric estimates in order to be meaningful.

There are many ways of performing math on probability distributions.  Monte Carlo simulations aren't always optimal in terms of performance, but they are very pragmatic in that they can be used on a great number of functions and inputs.
