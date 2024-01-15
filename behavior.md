# Behavior Patterns

> **Hint**: Work in progress

The real world context during an AR session can be seen as stage. The dynamic behavior of an AR experience is determined by its [Event-Condition-Action](eca.md) rules, which are triggered by events occurring in the actual real-world context.

| Behavioral Pattern	| Description	| Example |
|---|---|---|
| [Instant Reaction Pattern](behavioral-patterns/instant-reaction.md)	| Direct execution of action triggered by invocation of rule	| Immediate command of action or call of function |
| [Timed Reaction Pattern](behavioral-patterns/timed-reaction.md)	| Temporally executed action	| Delayed action or sequence of timed actions|
| [Conditional Reaction Pattern](behavioral-patterns/conditional-reaction.md)	| Execute an action only when a condition is fulfilled after being triggered by event	| State-driven, asynchronous programming logic|
| [Continous Evaluation Pattern](behavioral-patterns/continous-evaluation.md)	| Continuous polling of state changes that will triggers rules	|Continuous checks on value change, existence, visibility, proximity |
| [Publish-Subscribe Notification Pattern](behavioral-patterns/publish-subscribe-notification.md)	| Receive notifications via a message queue from a subscribed system	| From speech recognition system or from WebRTC system in collaboration session |
| [Request-Response Pattern](behavioral-patterns/request-response.md)	| Remote procedure call resulting in asynchronously receiving ECA rules or media assets	| REST API call via a Web URL to load rules or assets (images, 3D models)|
| [Chain Reaction Pattern](behavioral-patterns/chain-reaction.md)	| Course of events processed as sequence of indirect reactions of running subsequenced rules	| Rule changing data that will trigger a rule to update an item’s visual as a follow-up |
| [Complementary Reactions Pattern](behavioral-patterns/complementary-reactions.md)	| Two active rules with opposite reactions	|Reacting on toggling states with two complementary active rules|
| [Detector Reactivation Pattern](behavioral-patterns/detector-reactivation.md)	| Reactivate detector with only-once reaction	|Reactivate detector after resulting augmentation is no longer existing |