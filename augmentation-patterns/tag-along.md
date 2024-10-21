# Tag-Along Pattern

> An augmentation that moves together with the user

<img src="images/TagAlong.png">

An augmentation following the _Tag-Along_ pattern always moves together with the user (it _tags along_). Typically, such an augmentation also always attempts to stay within the user’s view range. The main advantage of tag-along augmentations is that they ensure the presented interaction elements are always visible and easily accessible to the user. 
User interface components in AR applications are a typical example of this pattern: These UI elements must always stay within the user's view range but are still spacially located within the AR scene.
A _Tag-Along_ augmentation is typically oriented towards the user’s position, centered on the user's face or device, using billboarding techniques. The main advantage of tag-along augmentations is that they ensure the presented interaction elements are always visible and easily accessible to the user. 
In AR applications for head-mounted displays, tag-along augmentations are usually designed to fit within the user’s arm-length range, ensuring they can interact with the elements without stretching or straining themselves.

## Requirements

_Tag-Along_ augmentations move together with the user. Therefore, they are attached to the user's position within the AR scene, and are facing the user's face, position or in more general terms, the camera.
Depending on the application, the augmentation may mirror the user's movements more or less closely. For example, a UI menu may stay at a fixed height; or it may not autmatically rotate with the user but rather require manual repositioning. Such constrained positional or rotational attachment has important properties helping to improve the usability of this pattern. We differentiate between _synchronized_ and _free_ constraints. 
- _synchronized_: The augmentation always mirrors the user's look-at direction, as if the user was wearing a helmet with a head-mounted display: This has its use in games, for example in first-person games.
- _free_: The augmentation stays in place within the scene even when the user moves their head up or down (y-axis position), tilts it (yaw), or turns around their own axis (y-axis rotation). The user may then manually reposition the augmentation, or just turn back to the place where it is position. This _free_ behaviour, independent of the user's head movement, can be useful for applications such as 3D design programs: A _synchronized_ attachment can sometimes obstruct the field of view, and the user may want the menu be outside of their view range, calling it back to their position when required.

The _Tag-Along_ pattern does not apply to every behaviour where an augmentation moves with the user. For example, a virtual dog that walks with the user, is most likely an application of the [**Ahead Staging Pattern**](ahead-staging.md) in combination with the [**Captured Twin Pattern**](captured-twin.md) and not the _Tag-Along_ pattern. The virtual dog is initially positioned in the AR scene, and then automatically positions itself near the user, taking into account envirnomental features such as the ground, walls or furniture. 

### Characteristics
* _Anchored_: On the user
* _Placed_: constraint ahead of user
* _Aligned_: constraint towards user
* _Camera_: rear-facing

## Similar Patterns

- [**Hand/Palm Pop-Up Pattern**](hand-palm-popup.md): While also primarily useful for UI components, the hand-palm popup is specifically meant to include applications where these components are attached to the user's hand and not centered in the user's position.
- [**Ahead Staging Pattern**](ahead-staging.md): Using the _Ahead Staging_ pattern, augmentations are initially placed ahead of the user. But, augmentations placed with the _Ahead Staging_ are anchored with a world-locked anchor, and do not move together with the user. See the virtual dog example in the [Requirements](#requirements) section for a more detailed explanation.


## Technical Requirements
The _Tag-Along_ pattern is one that has applications in almost all fields of AR. It is a core pattern for interacting with UI components within AR, XR and VR applications. Therefore, most of the technical challenges stem from the high usability standards for UI and UX components.

At it's most basic level, a _Tag-Along_ augmentation always stays with the user. It does not use world-locked anchors, but is attached to the scene's camera. 
When it comes to details of interacting with a _Tag-Along_ augmentation, especially these points should be considered:
- **Scene Interactions**: Typically, _Tag-Along_ augmentations do not collide with the environment, nor do they respond to scene lighting. To ensure that the UI components remain visible, it is recommended to treat _Tag-Along_ augmentations separately from the rest of the AR scone, and always draw them on top of everything else. Also, they should not respond to scene lighting, so that they are always optimally readable. In entertainment apps, where visual consistency is key, _Tag_Along_ augmentations may break the immersion, and a narrative reason for them to be there may have to be found, such as attaching them to a helmet. Also, you might have to use in-scene lighting to have them blend into the scene well.
- **Movement Constraints**: It is important to consider to what degree _Tag-Along_ augmentations are synchronized with the user's movements, or to what degree the augmentation is positionally or rotationally constrained. We differentiate between _synchronized_ and _free_ constraints. See the [Requirements section](#requirements) for a definition of these terms. In general, UI components always stay upright. They may move around the y-axis, but usually don't tilt - their rotation is constrained along x and z. This also helps the user to orient themselves. Similarly, a _tag_along_ augmentation often does not move up and down, but stays on a comfortable hip- or face-level after initial positioning, even if the user bends or crouches - the position is constrained along the y-axis, but can move freely along x and z.
- **Presence**: Users should clearly understand which UI element or scene they are currently interacting with. Visual cues, haptics and sound are important aspects of ensuring smooth interactions. For example, the concept of [tomato presence](https://ieeexplore.ieee.org/document/10108763) can be used that user's always know which button they are currently pointing at before accidentally pressing it. Similarly, haptics and sound can be used to help users navigate. 

## Scenarios and Examples

- **User Interfaces**: ‘Near Menu’ UX component of the [Mixed Reality Toolkit](https://learn.microsoft.com/windows/mixed-reality/mrtk-unity/mrtk3-overview).

