# Anchored Supplement Pattern

> Shows an augmentation in relation to something that was detected

![Example of Anchored Supplement Pattern](images/AchoredSupplement.png)

## Description
The Anchored Supplement pattern shows an augmentation that adds context to something that was detected. For example, after detecting a famous painting, a description of this painting could be shown next to the painting.
This pattern is applied whenever an augmentation is shown in a fixed spacial relationship to a detected entity. In the example above, the description—i.e. the _supplement_—would be shown next to the detected painting—i.e. the _anchor_.  The anchored supplement pattern has the intention of adding context to real-world entities in order to describe them or otherwise augment them.
This pattern is especially well suited to training and educational applications or may also have its uses in any case where the real world can benefit from contextual augmentations.

### Augmentation
- _placed_: relative to detected object
- _aligned_: with detected object or towards user

### Requirements
The anchored supplement can be applied if a specific entity is detected and has a point of origin which can be designated as _anchor_. This allows the relative positioning of the _supplement_. For example, showing a 3D Object anchored in a detected tag constitutes a use of this pattern. 
The anchored supplement pattern requires that the detected entity remain visible and that the supplement be placed at a fixed spatial relationship to it.

### Use Cases
- Shopping: Show price tag and product information
- Museums: Provide contextual information about exhibit or artist
- Manufacturing: Guide product assembly with augmented support information

## Related Patterns
- [**Superimposition:**](superimposition.md) In the anchored supplement pattern, the detected object should not be covered. If the detected object is to be covered up with a replacement, the superimposition applies. For example, if a painting is covered up with another painting.
- [**Segment Overlay Pattern:**](segment-overlay.md) When the entity originates from camera image segmentation rather than the detection of an entity in 3D, the segment overlay pattern applies. For example, detecting an image segment as the sky, and then recoloring this area 
- [**Hand/Palm Pop-Up Pattern:**](hand-palm-popup.md) When the detected entity is a hand or other body part in a mixed-reality context and the goal of the augmentation is to add specific functionality with UX elements, the Hand/Palm Pop-Up Pattern applies.

