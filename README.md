# Holistic Estimation Systems

Many important things aren't known for sure, but can be estimated.  What will the global economy be like in 5 years? How quickly will Global Warming occur? Exactly how big is the universe? These questions have been approximated; and while these approximations aren't exact, they are still very useful for making decisions.

A subset of similar questions can be very well approximated by simple machine learning. These are typically very repeatable events with a lot of existing data. However, many important questions come from very novel circumstances that would be hard to use direct data analysis on.  We don't have a long table of similar planets that have experienced similar economic and technological conditions, or a table of similar universes and their sizes.

Fortunately, our understanding of the universe has led to a host of predictive models that we can apply to novel situations to result in our predictions of unknown variables. Some of these are mathematical, (F=ma), others are more heuristical (an increase in buyers is correlated with increases in price under specific conditions.)

In this paper we outline the idea of Holistic Estimation Systems, a structured approach of mathematical modeling aimed to help reduce uncertainty of many variables. These have two primary distinctions. First, uncertainty is accounted for in accordance to a specified set of rules. Second, large networks of models are connected and used to understand many variables over time. These ideas can be understood separately (we call these Estimation Models and Holistic Systems), but we think that their combination provides unique and powerful benefits.

Holistic Estimation Systems are meant and optimized for the use of humans making intuitive judgements.

## Principal Features
- Careful accounting of uncertainty of computed metrics through sets of functions
- The presence of many (over 20) functions, inputs, and outputs.
- The use of improving & tracking important metrics over periods of time, rather than for one specific project

The large size & timeline is pragmatic for the careful uncertainty account for two reasons.  First, uncertainty accounting allows for very large models.  Second, the creation of large models takes more resources than for small models.  These are more worthwhile when the modeling can be reused for multiple purposes and at different times. Therefor we think that is useful to fit these different needs into one type of system.

## Important Technical Restrictions
- All uncertain metrics values should be described using probability distributions.
- All functions on uncertain metrics must be able to output probability distributions.
- Intermediate and output metrics should be recalculated after any input metrics change values. In order for this to work well, all functions should be immutable.
- The metric and function structure should be acyclic.  If there are any feedback effects, these should be isolated inside of specific functions, rather than exposed to the larger system.
