
# Title of AR Scenario 

![illustration image](illustration.jpg) {Hint: [AR Illustrations](https://arpatterns.dev/illustrations)}

Text decription of AR scenario ...

* _Use Case_: name of AR Use Case Category {Hint: [Use Cases]([../README.md](https://github.com/ARpatterns/catalog/blob/main/usecases.md))}
* _Technology Platform_: [name of used technology](../README.md) {Hint: [Tech Platforms]([../README](https://github.com/ARpatterns/catalog/blob/main/platforms.md).md)}
* _Device Type_: handheld | headmounted
* _Vision System_: world camera | mirrored face camera 

![screen or video](screen.jpg) {Hint: screen shot or animated gif}

## AR Patterns

{Hint: List of used behavior and augmentation patterns. Link the patterns to their catalog references as shown in the samples below}

__Behavior Pattern__

* [Instant Reaction](https://github.com/ARpatterns/catalog/blob/main/behavioral-patterns/instant-reaction.md): Immediate execution of the staging ahead action
  * _Event_: on start {Hint: [Events](https://github.com/ARpatterns/catalog/blob/main/eca/events.md)}

__Augmentation Pattern__
* [Ahead Staging](https://github.com/ARpatterns/catalog/blob/main/augmentation-patterns/ahead-staging.md): presenting 3D object `red.box` 1.5 m  in front of the user.
  * _Placed_: initial ahead of the user on the floor.
  * _Aligned_: initial towards the user in view direction.
  * _Pivot_ {optional}: Objects in the local coordinate system are centered on the ground floor. If the object is rotated around the AR anchor in the world coordinate system, it turns by it's center up axis.

## ECA Diagram {optional but recommended}

{Hint: Use [ECA Diagram](https://github.com/ARpatterns/diagram) as a kind of pseudo code to document this AR scenario.}

 | on:start |  &rarr; | do:add ahead 0 0 -1.2 |
 |---|---|---|
> 'red.box' ➕

## Code {optional}

```json
{
  script | code 
  --> only for low-code implementations,
      otherwise use link to source code or project folder 
}
```

## Links {optional}

* _Detailed Docu_: [docu_as_markdown.md](docs/docu.md)
* _Source Code_: [project/source.code](project/source.code)
* _Assets_: [media](project/media.asset), ...


## References {optional}

- [Technical Documentation](https://___/docu/)
- [AR App](https://___)
- AR Patterns [Diagram](https://github.com/ARpatterns/diagram)
