# Chain Reaction Pattern

A sequence of several chained reactions. 
Execute an action that is triggered by a changed state caused by a former event

Loosly coupled reactive programming.

Active rules are processed asynchronously to avoid coordination and waiting. Coupling of data and visuals or audio can be achieved by observing state changes.

| on:command	| →	| do:assign |
|---|---|---|
> data.flag = 1

| as:stated	| if:data.flag == 1	| do:say | 
|---|---|---|
> "Indirect Reaction Pattern" 🗣