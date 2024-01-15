# Continous Evaluation Pattern

The continuous evaluation of rules can be driven by a constant time interval or by each state change of the data model. A built-in state management is observing the data model and does dispatch the processing of rules according to the [data-driven events](../eca/events.md#data-driven-events) that are bound to the ECA rules.

Temporally controlled repetition:

| repeated each 60 secs	| →	| do:say | 
|---|---|---|
> "Another minute." 🗣


Continuous query as repeated evaluation on each state change:

| stated	| if:`function('red.box.id', 'proximity') < 1.2` | do:execute | 
|---|---|---|
> function('https://___', 'getJSON') ◀