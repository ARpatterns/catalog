# Conditional Reaction Pattern

An ECA rule’s condition is tested on the data available in the current AR session at the time of evaluation. The outcome of the condition evaluation is either true or false. Only if true the action of the ECA rule will be executed. In addition, a conditional reaction can be combined with a timed reaction. Together, these reactions form the core of the [continuous evaluation pattern](continous-evaluation.md).

| on:change	| if:`items.@count >= 1` | do:say | 
|---|---|---|
> "Conditional Reaction Pattern" 🗣

The built-in state management is observing model as well as data elements and dispatches the processing of reactions.