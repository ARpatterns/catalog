# Behavior Patterns

> **Hint**: Work in progress

The real world context during an AR session can be seen as stage. The dynamic behavior of an AR experience is determined by its [Event-Condition-Action](eca.md) rules, which are triggered by events occurring in the actual real-world context.

| Behavioral Pattern	| Description	| Example |
|---|---|---|
| [Instant Reaction Pattern](behavioral-patterns/instant-reaction.md)	| Direct execution of task triggered by invocation event	| Immediate, singular command of task or function call |
| [Timed Reaction Pattern](behavioral-patterns/timed-reaction.md)	| Temporally executed action	| Delayed action, timed action sequence|
| [Conditional Reaction Pattern](behavioral-patterns/conditional-reaction.md)	| Execute an action only when a condition is fulfilled after being triggered by event	| State-driven, asynchronous programming logic|
| [Continous Evaluation Pattern](behavioral-patterns/continous-evaluation.md)	| Continous polling of state change	|Existence check, visibility check, proximity check, repeated update checks |
| [Publish-Subscribe Notification Pattern](behavioral-patterns/publish-subscribe-notification.md)	| Receive notifications via a message queue from a subscribed system	| In FaceTime/SharePlay call, in Bluetooth connection, in WebSocket/WebRTC session |
| [Request Response Pattern](behavioral-patterns/request-response.md)	| Remote procedure call resulting in asynchronously receiving ECA rules or media assets	| REST API call via a Web URL to load rules or assets (images, 3D models), e.g., `GET:JSON` or `POST:CONTEXT`|
| [Chain Reaction Pattern](behavioral-patterns/chain-reaction.md)	| Course of events processed as sequence of indirect reactions	| Rule changing data that will trigger a rule to update an item’s visual as a follow-up |
| [Complementary Reactions Pattern](behavioral-patterns/complementary-reactions.md)	| Two reactions with opposite result	|Reacting on toggling states with two complementary active rules|
| [Detector Reactivation Pattern](behavioral-patterns/detector-reactivation.md)	| Reactivate detector with only once reaction	|Reactivate detector after resulting augmentation is no longer existing |


## Immediate Reaction Pattern
| on:command	| →	| do:say | 
|---|---|---|
> "Immediate Reaction Pattern" 🗣

## Timed Reaction Pattern
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

## Conditional Reaction Pattern
| on:change	| if:`items.@count >= 1` | do:say | 
|---|---|---|
> "Conditional Reaction Pattern" 🗣

The built-in state management is observing model as well as data elements and dispatches the processing of reactions.


## Request Response Pattern
Remote request with async response:

| on:command	| →	| do:request GET:JSON | 
|---|---|---|
> Action ← response ••• https://www.company.com/actions/response.json
> 
> | on:command	| →	| do:say | 
> |---|---|---|
>> "Async Response Reaction" 🗣

Hint: REST is stateless, therefore handle state on client.

## Publish-Subscribe Notification Pattern
| on:enter	| →	| do:say | 
|---|---|---|
> "New participant entered session." 🗣

## Chain Reaction Pattern

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


## Continous Evaluation Pattern

Temporally controlled repetition:

| repeated each 60 secs	| →	| do:say | 
|---|---|---|
> "Another minute." 🗣


Continuous query as repeated evaluation on each state change:

| stated	| if:`function('red.box.id', 'proximity') < 1.2` | do:execute | 
|---|---|---|
> function('https://___', 'getJSON') ◀

## Complementary Reactions Pattern
| on:start	| →	| do:add ahead 0.0 1.0 -0.9 | 
|---|---|---|
> red.box ➕

| on:altered	| if:`function('red.box', 'visible') == true`	| do:say | 
|---|---|---|
> "you see box" 🗣

| on:altered	| if:`function('red.box', 'visible') == false` | do:say | 
|---|---|---|
> "now you don't" 🗣


## Detector Reactivation Pattern
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

