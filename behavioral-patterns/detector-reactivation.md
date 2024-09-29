# Detector Reactivation Pattern

Some detectors halt after capturing a first occurrence of an entity and need to be reactivated by a `do:redetect` action. The reactivation can be driven by a separate active rule, for instance, after a specific period of time or by assessing the existence or visibility of the item added by the detector based on a corresponding condition.


| on:call |  &rarr; | do:detect:plane |
|---|---|---|
 
> Install plane detector &larr; "seat" 👁
> | _on:detect_ | &rarr; | _do:execute:op_ |
> |---|---|---|
> 
> > `function('Look, a chair', 'say')`  
> 
> | _on:detect_ | &rarr; | _do:add to AR anchor_ |
> |---|---|---|
> 
>> 'detected.plane.seat' ➕
> 
> | _as:stated_ | _if:`visible('detected.plane.seat') == false`_ | _do:remove_ |
> |---|---|---|
> 
>> 'detected.plane.seat' ❌
 
 | in:300 |  &rarr; | do:redetect |
 |---|---|---|
> 'detect.plane.seat'
 