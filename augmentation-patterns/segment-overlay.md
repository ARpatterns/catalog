# Segment Overlay Pattern

<img src="images/SegmentOverlay.png">

By utilizing computer vision and machine learning techniques, a segment detector can recognize and track designated landmarks and image segments. The outcomes of the image segmentation process may include:

* __point (pixel)__: room corner, object corner, pupil center, ...
* __edge__: horizon line, wall-floor edge, ...
* __bounding box__: depicting rectangle border of detected text, image, face, ...
* __path (open path)__: eyebrow, body skeleton, ...
* __contour (closed path)__: face, mouth, eye, ...
* __image mask__: sky, grass, hair, ...

In the AR view, the overlay is positioned based on the pixels relative to the segment within the 2D image, on top of the video stream.

* _Placed_: on screen at image segment
* _Aligned_: flat on top as overlay