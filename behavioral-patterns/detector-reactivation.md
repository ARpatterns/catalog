# Detector Reactivation Pattern
Some detectors stop after capturing a first occurence of the depicted entity and need be reactivated by a do:redetect task. The reactivation can be driven by a separate active rule, e.g. by evaluating in the condition the visibility of an added item by the detector.

| on:command	| →	| do:detect:feature | 
|---|---|---|
> chair 👁

| on:detect	| →	| do:execute:op | 
|---|---|---|
>function('I found a chair', 'say') ◀

| on:detect	| →	| do:add | 
|---|---|---|
> detected.feature.chair ➕

| on:altered	| if:`function('detected.feature.chair', 'visible') == false` | do:redetect | 
|---|---|---|
> detected.feature.chair