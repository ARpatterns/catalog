# Anchored Supplement Pattern
> Shows an augmentation in relation to something that was detected

![Example of the Anchored Supplement Pattern](augmentation-patterns/images/AchoredSupplement.png)

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
