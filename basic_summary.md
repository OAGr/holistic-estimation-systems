# Overview
## Main Features of Large Approximation Systems
- Carefully acounting of uncertainty of computed metrics through sets of functions
- The presense of many (over 20) functions, inputs, and outputs.
- The use of improving & tracking important metrics over periods of time, rather than for one specific project

The large size & timeline is pragmatic for the careful uncertainty account for two reasons.  First, uncertainty accounting allows for very large models.  Second, the creation of large models takes more resources than for small models.  These are more worthwhile when the modeling can be reused for multiple purposes and at different times. Therefor we think that is useful to fit these different needs into one type of system.

## Main Technical Restrictrions
- All uncertain metrics values should be described using probability distributions.
- All functions on uncertain metrics must be able to output probability distributions.
- Intermediate and output metrics should be recalculated after any input metrics change values. In order for this to work well, all functions should be immutable.
- The metric and function structure should be acyclic.  If there are any feedback effects, these should be isolated inside of specific functions, rather than exposed to the larger system.
