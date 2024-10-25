# Publish-Subscribe Notification Pattern

In a similar manner to monitoring changes in the data model, changes in subsystems can also generate events that trigger rules. Subsystems can be observed through a publish-subscribe notification mechanism. For instance, a speech recognition system might be initiated (by a `do:listen` action) and subscribed to. When a voice command is recognized, an `on:voice` event is published as message. Another example is the usage of a collaboration subsystem that sends notifications when a participant joins or leaves a session.

## ECA Diagram

| on:enter	| →	| do:say | 
|---|---|---|
> "New participant entered session." 🗣
