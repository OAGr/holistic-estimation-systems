# Holistic Systems
One challenge with sophisticated estimation models is that they can take a significant amount of effort when used for one-time analyses. They may be more practical to do in the context of Holistic Systems.

Holistic Systems are termed as an alternative to single use numeric analyses. Single use analyses are mathematical models created with a narrow set of outputs in mind. Holistic Systems are a structure of inputs, models, and interesting outputs that are interconnected.

The focus on interconnecting large systems of models raises important questions about the interfaces between these models.

## Features
- The presence of many (over 20) functions, inputs, and outputs.
- The use of improving & tracking important metrics over periods of time, rather than for one specific project

The large size & timeline is pragmatic for the careful uncertainty account for two reasons.  First, uncertainty accounting allows for very large models.  Second, the creation of large models takes more resources than for small models.  These are more worthwhile when the modeling can be reused for multiple purposes and at different times. Therefor we think that is useful to fit these different needs into one type of system.

## Restrictions
- All functions must be pure (no side-effects) and immutable. There can be complex models involving agent-based modeling or feedback loops, but these must be encapsulated in pure and immutable functions.
- The metric and function structure should be acyclic.  
- Metrics estimated using functions should be automatically recalculated after any input metrics change values.
