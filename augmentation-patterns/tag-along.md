# Tag-Along Pattern

<img src="images/TagAlong.png">

A tag-along augmentation attempts to always stay within the user’s view range, which is constrained to their eye position. To achieve this, the augmentation is typically always oriented towards the user’s face using billboarding techniques. The main advantage of tag-along augmentations is that they ensure the presented interaction elements are always visible and easily accessible to the user. In AR applications for head-mounted displays, tag-along augmentations are usually designed to fit within the user’s arm-length range, ensuring they can interact with the elements without stretching or straining themselves. An example is the ‘Near Menu’ UX component of the [Mixed Reality Toolkit](https://learn.microsoft.com/windows/mixed-reality/mrtk-unity/mrtk3-overview).

* _Placed_: constraint ahead of user
* _Aligned_: constraint towards user
