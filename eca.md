# Event-Condition-Action Pattern

To design reactive systems, breaking down the system’s behavior into discrete events, conditions, and actions provides a structured and modular approach. An event is a signal that something has occurred, such as the start of an AR session (`on:start`), a user tapping on an item (`on:tap`), or the detection of an image marker (`on:detect`). The no-code editors [Apple Reality Composer](https://developer.apple.com/augmented-reality/tools/) and [Adobe Aero](https://www.adobe.com/products/aero.html) are using a triggeraction mechanism to define the behavior of an AR scenario. We propose to use more flexible Event-Condition-Action (ECA) rules that perform an action in response to an event, provided that certain conditions are met. ECA rules are widely used in event-driven and reactive systems, such as active databases and workflow systems. In the context of AR patterns, ECA rules provide a generic abstraction of the reactive behavior of AR software systems.

## Reactive AR Using Active ECA Rules
AR systems utilize a variety of sensors, such as cameras, LiDAR, accelerators, gyroscopes, magnetometers, and microphones, along with various event producers in operating system and user interfaces. These sensors and producers generate events asynchronously, which are then handled by event-driven programs. Unlike traditional programs that make function calls to these event producers themselves (in an inner loop), an event-driven program relies on the execution environment to dispatch events to installed event handlers. Thus, control over the execution of program logic is inverted (inversion of control).

To address the reactive nature of AR applications we promote ECA rules as a means of loosely coupling AR patterns with the underlying system architecture, while also abstracting from implementation details. AR patterns are designed to be loosely bound to the specific run-time system, since events that trigger actions within AR applications are not necessarily aware of the consequences of their occurrence. As a result, creators of AR experiences are primarily responsible for defining a set of event handling rules that govern how the system responds to various arising signals and events.

## Events Categories in AR Applications

[Events Categories in AR](eca/events.md)

## Condition Evaluation Within Spatial AR Context

[Condition Evaluation within AR](eca/condition-evaluation.md)

## Actions in AR Applications

[Actions in AR](eca/actions.md)

## AR Pattern Diagram

[AR Pattern Diagram](../../../diagram)


