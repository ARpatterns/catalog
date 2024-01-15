# Timed Reaction Pattern

Timed reactions are ECA rules that are fired after a given interval to carry out their action. Once the timed rule is initiated, an internal job scheduler triggers the rule at the time interval specified.

| in:5	| →	| do:say | 
|---|---|---|
> "Timed Reaction Pattern" 🗣

A sequence of timed reactions as an example:

| on:start	| →	| do:say | 
|---|---|---|
> "Here we go." 🗣

| in:4	| →	| do:say | 
|---|---|---|
> "Timed Reaction Pattern" 🗣

| in:7	| →	| do:say | 
|---|---|---|
> "Good bye" 🗣

| in:10	| →	| do:exit | 
|---|---|---|
> stop AR session ◾