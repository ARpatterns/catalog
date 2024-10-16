# Ahead Staging Pattern
> Sets up content in front of the user for convenient interaction
<img src="images/AheadStaging.png">

## What is the Ahead Staging Pattern?
Ahead Staging is a technique for aligning 3D content with a viewer's position and viewing direction in AR applications. In this technique, virtual content—referred to as an augmentation—is positioned (_staged_) directly in front (_ahead_) of the user when the AR scene begins. This ensures that the augmentation is immediately visible to the user upon scene activation, avoiding issues with content that is positioned outside of the viewers field of view.
The ahead staging pattern refers to the use of the aforementioned technique and applies whenever whenever an augmentation appears in front of the user at the start of the AR experience. This can occur whether the augmentation is automatically _staged_ by the system or if the user is prompted to place it manually within the scene. The orientation of the augmentation does not impact this pattern. Typically, augmentations are placed at a default distance of 1–2 meters (approximately 3–7 feet) in front of the user, using a world-locked anchor that is often aligned with the ground plane. The augmentation may be oriented towards the user, a geolocated reference point (e.g., Mecca), a recognized object (e.g., a chair), a detected feature (e.g., a wall), or another point of reference.
After this initial positioning, users can interact with the augmentation or move freely around it. Since the augmentation is anchored in the world (world-locked), it remains in place, distinguishing the ahead staging pattern from other augmentations patterns, such as the "tag-along" pattern, where the augmentation moves with the user. The ahead staging pattern positions the content initially in front of the user, but once placed, it remains anchored in the world and does not follow the user’s movement.

The Ahead Staging Pattern is useful in a variety of contexts where users can freely place augmentations in their environment, such as furniture, game objects, or animations. Known applications generally use the rear camera with this pattern.

## Requirements
The ahead staging pattern applies whenever AR content is placed in front of the user when an AR scene starts and positioned relative to a world-locked anchor. For world-locked anchoring to work, some form of feature detection is therefore required for this pattern to apply.
It is recommended to prompt users to move their device in order to scan the environment to enable anchoring.

* _Anchored_: any world anchor
* _Placed_: initially ahead of user
* _Aligned_: no impact
* _Camera_: Rear

## Related Patterns


## Technical Considerations

## What is the Anchored Supplement Pattern?
This pattern shows an augmentation that adds context to something that was detected. For example, after detecting a famous painting, a description of this painting could be shown next to the painting.
This pattern is applied whenever an augmentation is shown in a fixed spacial relationship to a detected entity. In the example above, the description—i.e. the _supplement_—would be shown next to the detected painting—i.e. the _anchor_.  The anchored supplement pattern has the intention of adding context to real-world entities in order to describe them or otherwise augment them.
This pattern is especially well suited to training and educational applications or may also have its uses in any case where the real world can benefit from contextual augmentations.

## Requirements
The anchored supplement can apply if a specific entity is detected with has a point of origin which can be designated the _anchor_. This allows the relative positioning of the _supplement_. For example, showing a 3D Object anchored in a detected tag constitutes a use of this pattern. 
The anchored supplement pattern requires that the detected entity remain visible and that the supplement be placed at a fixed spacial relationship to it or the user.

## Related Patterns
- [**Segment Overlay Pattern:**](segment-overlay.md) When the entity originates from camera image segmentation rather than than the detection of an entity, the segment overlay pattern applies. For example, detecting an image segment as the sky, and then recoloring with AR 
- **Hand/Palm Pop-Up Pattern:** When the detected entity is a hand or other body part in a mixed-reality context and the goal of the augmentation is to add specific functionality with UX elements, the Hand/Palm Pop-Up Pattern applies.
- **Superimposition:** In the anchored supplement pattern, the detected object should not be covered. If the detected object is to be covered up with a replacement, the superimposition applies. For example, if a painting is covered up with another painting.

## Technical Considerations
Are there any?

## Scenarios and Examples
- Shopping: Show price tags
- Museums: Provide contextual information about exhibits
- Manufacturing: Guide product assembly with augmented support information

## Code
| placed: _relative to object_ | aligned: _with object or towards object / user_ |
|---|---|
