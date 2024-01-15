# Augmentation Patterns

> **Hint**: Work in progress

While a VR/3D designer is placing virtual objects using positions in a controlled world coordinate system, 
an AR content creator primarily specifies object placement intents relative to appearing anchors, 
which are dynamically produced by detectors. These spatial anchors serve as reference points for pinning objects. 
Generally in AR Patterns, the augmentation intents are formulated as [Event-Condition-Action](eca.md) (ECA) rules that are triggered by detector events. 
When a detector event occurs, ECA rule’s reaction will add augmentation items to the AR scene.

The following table outlines several common placement intents for event-driven augmentation patterns 
that can be used to stage AR experiences. In AR, the real world serves as the spatial context for the stage, 
making users both spectators and performers. Their movements and perspectives influence the firing of events, 
leaving limited control over time and space for AR scenography (in contrast to film, theater, and VR/3D/game design).

| Augmentation Pattern	| Description	| Example |
|---|---|---|
| [Geolocated Remark Pattern](augmentation-patterns/geolocated-remark.md)	| Triggering of action or of user feedback based on GPS location data or on address data	| Visual or audio feedback about location-based point of interest | 
| [Segment Overlay Pattern](augmentation-patterns/segment-overlay.md)	| Presentation of 2D overlay on top of image segment detected in video stream	| Attaching 2D text description to a detected image segment | 
| [Area Enrichment Pattern](augmentation-patterns/area-enrichment.md)	| Approximately placing 3D content at area of image segment| Presenting ballons in sky area | 
| [Captured Twin Pattern](augmentation-patterns/captured-twin.md)	| Captured element of real world added to 3D data model	| Captured walls and doors and windows in an indoor AR session | 
| [Anchored Supplement Pattern](augmentation-patterns/anchored-supplement.md)	| Presentation of 3D content aligned to detected entity for enhancement	| Attaching visual 3D elements to a detected image (marker) or captured object | 
| [Superimposition Pattern](augmentation-patterns/superimposition.md)	| Presentation of 3D content replacing a detected entity	| Cover a detected object with a virtual one | 
| [Tag-along Pattern](augmentation-patterns/tag-along.md)	| Presentation of 3D content within user’s field of view while head-locked	| Place 3D control panel that follows the user | 
| [Hand/Palm Pop-up Pattern](augmentation-patterns/hand-palm-popup.md)	| Presentation of 3D content on hand or palm while visible	| Place 3D UI elements at palm of user's one hand | 
| [Ahead Staging Pattern](augmentation-patterns/ahead-staging.md)	| Presentation of 3D content ahead of user	| Placing 3D item on floor in front of spectator | 
| [Pass-through Portal Pattern](augmentation-patterns/pass-through-portal.md)	| Present partly hidden 3D content to force user to go through	| Placing 3D scene behind a portal / behind an opening | 
| [Staged Progression Pattern](augmentation-patterns/staged-progression.md) | Ordered, linear story: temporal order or interaction flow of 3D presentations	| Sequence of 3D content with forth and optionally back movements | 
| [Attention Director Pattern](augmentation-patterns/attention-director.md) | Guide user’s attention to relevant place | Use animated pointers to direct user’s attention |
| [Contextual Plot Pattern](augmentation-patterns/contextual-plot.md) | Spatio-temporal setting that aggregates diverse AR patterns to form a non-linear plot | Scenography of dynamic, interactive, and animated AR | 


