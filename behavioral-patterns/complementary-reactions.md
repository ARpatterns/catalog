# Complementary Reactions Pattern

Complementary reactions are constructed using two rules that have opposite conditions and actions with opposite results. When these two rules are evaluated continuously, they exhibit a toggling state by flipping their mutual rule execution.

| on:start	| →	| do:add ahead 0.0 1.0 -0.9 | 
|---|---|---|
> red.box ➕

| on:altered	| if:`visible('red.box') == true`	| do:say | 
|---|---|---|
> "You see a red box." 🗣

| on:altered	| if:`visible('red.box') == false` | do:say | 
|---|---|---|
> "Now you don't." 🗣