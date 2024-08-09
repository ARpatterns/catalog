# Detector Reactivation Pattern

Some detectors halt after capturing a first occurrence of an entity and need to be reactivated by a `do:redetect` action. The reactivation can be driven by a separate active rule, for instance, after a specific period of time or by assessing the existence or visibility of the item added by the detector based on a corresponding condition.

| on:command	| →	| do:detect:feature | 
|---|---|---|
> chair 👁

| on:detect	| →	| do:execute:op | 
|---|---|---|
>function('I found a chair', 'say') ◀

| on:detect	| →	| do:add | 
|---|---|---|
> detected.feature.chair ➕

| on:altered	| if:`visible('detected.feature.chair') == false` | do:redetect | 
|---|---|---|
> detected.feature.chair