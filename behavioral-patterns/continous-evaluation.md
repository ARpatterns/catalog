# Continous Evaluation Pattern

Temporally controlled repetition:

| repeated each 60 secs	| →	| do:say | 
|---|---|---|
> "Another minute." 🗣


Continuous query as repeated evaluation on each state change:

| stated	| if:`function('red.box.id', 'proximity') < 1.2` | do:execute | 
|---|---|---|
> function('https://___', 'getJSON') ◀