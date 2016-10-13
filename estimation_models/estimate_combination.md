# Estimate Combination

If there are multiple estimates for one specific metric, there should be some way to combine these into one aggregate estimate. This technique is similar in study to the work of Meta-Analysis, though is focussed more on the combination of simple estimates than the results of larger studies.

## Intuitive Approaches
The basics of an intuitive approach to estimate combination would involve one person reading a set of estimates for one metric and intuitively providing their take based on them. One challenge is that it may be difficult for the individual to do this without providing a higher weighting to their own estimate, or biasing it in some way.

If the agent creating the model is the individual combining a particular set of estimations, then it would make sense for the combination to simply be that individuals' estimate of the metric after taking those estimates into consideration. If the agent creating the model is not that individual, then one of two cases could happen. First, the individual could simply take their own estimate, then a contextual adjustment could be used to convert that to the probability of the agent. Second, the individual could attempt to make a more 'blind' estimate; perhaps even without information on what the metric is representing. This could make the combination effort more systematic, but do so at the expense of possible errors. There would still have to be a contextual adjustment; this could be more or less than in the first case depending on the agent's trust in the individual.

## Algorithmic Approaches
One basic algorithmic approach to estimate combination is to use a simple Bayesian adjustment, as described [here](http://blog.givewell.org/attachments/worms.pdf). A different naive approach is to assign each estimate a 1/n (where n is the number of estimates) likelihood of being true, then sampling them at that proportion.

A more complex algorithmic approach would probably be assisted by taking several factors into account.
1. How much does the shape or narrowness of the estimates tell us about how much information they draw from?
2. How reliable are the sources of these estimates?
3. Does the similarity or differences of these estimates give us information on their credibility?

The challenge here is to take whatever information is available and use that to predict the most accurate probability distribution for the output. This is an complex optimization problem, rather than a straightforward statistical formula with one correct solution. We imagine that machine learning could be useful in providing a robust algorithm for this.

One thing to note is that while it may seem like the more narrow one estimate is, the more it should be counted, this is not always the case. It can be proved mathematically that there are times when learning more information about a situation can increase the width of your probability distribution of it. We find it likely that there is a negative association with error amount and knowledge (and thus influence compared to similar estimates), but this should be treated as an empirical claim.

https://www.amazon.com/Introduction-Meta-Analysis-Michael-Borenstein-ebook/dp/B00HCCX2N6/ref=mt_kindle?_encoding=UTF8&me=

https://en.wikipedia.org/wiki/Meta-analysis

https://www.amazon.com/Essential-Guide-Effect-Sizes-Interpretation/dp/0521142466/ref=sr_1_4?s=books&ie=UTF8&qid=1476293974&sr=1-4&keywords=Meta-Analysis

http://blog.givewell.org/2011/08/18/why-we-cant-take-expected-value-estimates-literally-even-when-theyre-unbiased/
http://blog.givewell.org/attachments/worms.pdf
