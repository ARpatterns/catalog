# Complementary Reactions Pattern
| on:start	| →	| do:add ahead 0.0 1.0 -0.9 | 
|---|---|---|
> red.box ➕

| on:altered	| if:`function('red.box', 'visible') == true`	| do:say | 
|---|---|---|
> "you see box" 🗣

| on:altered	| if:`function('red.box', 'visible') == false` | do:say | 
|---|---|---|
> "now you don't" 🗣