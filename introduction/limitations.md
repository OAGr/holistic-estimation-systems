# Imposed Limitations
- All uncertain metrics values should be described using probability distributions.
- All functions on uncertain metrics must be able to output probability distributions.
- Intermediate and output metrics should be recalculated after any input metrics change values. In order for this to work well, all functions should be immutable.
- The metric and function structure should be acyclic.  If there are any feedback effects, these should be isolated inside of specific functions, rather than exposed to the larger system.
