# Augmentation Patterns

While a VR/3D designer is placing virtual objects using positions in a controlled world coordinate system, 
an AR content creator primarily specifies object placement intents relative to appearing anchors, 
which are dynamically produced by detectors. These spatial anchors serve as reference points for pinning objects. 
Generally in AR Patterns, the augmentation intents are formulated as ECA rules that are triggered by detector events. 
When a detector event occurs, ECA rule’s reaction will add augmentation items to the AR scene.

The following table outlines several common placement intents for event-driven augmentation patterns 
that can be used to stage AR experiences. In AR, the real world serves as the spatial context for the stage, 
making users both spectators and performers. Their movements and perspectives influence the firing of events, 
leaving limited control over time and space for AR scenography (in contrast to film, theater, and VR/3D/game design).

| Augmentation Pattern	| Description	| Example |
|---|---|---|
| Geolocated Remark Pattern	| Triggering of action or of user feedback based on GPS location data (long/lat) or address data (city, street, ...)	| Visual or audio feedback in standard UI about location-based point of interest | 
| Segment Overlay Pattern	| Presentation of 2D overlay on top of image segment detected in video stream	| Attaching 2D text description to a detected image segment | 
| Area Enrichment Pattern	| Approximately placing 3D content at area of image segment| Presenting ballons in sky area | 
| Captured Twin Pattern	| Captured element of real world added as 3D model	| Captured walls, doors and windows in an indoor AR session | 
| Anchored Supplement Pattern	| Presentation of 3D content aligned to detected entity for enhancement	| Attaching visual 3D elements to a detected image (marker) or captured object | 
| Superimposition Pattern	| Presentation of 3D content replacing a detected entity	| (Re-)Place a detected image with another one | 
| Tag-along Pattern	| Presentation of 3D content within user’s field of view while head-locked	| Place interactive 3D elements that follow the user | 
| Hand/Palm Pop-up Pattern	| Presentation of 3D content on palm of hand while visible	| Place 3D UI elements at palm of user's one hand | 
| Ahead Staging Pattern	| Presentation of 3D content ahead of user	| Placing 3D item on floor infront of spectator | 
| Pass-through Portal Pattern	| Presentation of partly hidden 3D content to force user to go through	| Placing 3D scene behind a portal / behind an opening | 
| Staged Progression Pattern | Ordered, linear story: temporal order or interaction flow of 3D presentations	| Sequence of 3D presentations with forth and optionally back movements | 
| Attention Director Pattern | Guide user’s attention to relevant place | Use animated pointers to direct user’s attention |
| Contextual Plot Pattern | Spatio-temporal setting that aggregates diverse AR patterns to form a non-linear plot | Scenography of dynamic, interactive, and animated AR | 
|

