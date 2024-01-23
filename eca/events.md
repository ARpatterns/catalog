# Events Categories in AR Applications

## Session Events
* `on:start`: immediately after start of AR session or after loading action
* `on:locating`: on locating in the world (by GPS, by SLAM device positioning)
* `on:stable`: when spatial registration of AR device gets stable
* `on:load`: after loading 3D item to AR view, e.g., to animate or occlude node
* `on:stop`: before AR session ends
  
## Invocation Events
* `on:command`: on command initiation 
* `on:call`: on function call
  
## User Events
* `on:tap`: when tapped on item
* `on:press`: when long-pressed on item
* `on:drag`: when dragging an item
* `on:select`: when selected from options of pop-up menu
* `on:dialog`: when selected from options of pop-up dialog panel 
* `on:poi`: when selected a point of interest in a map or minimap

## Temporal Events
* `in:time`: when elapsed time in seconds is reached
* `as:always`: several times per seconds
* `as:repeated`: like `as:always`, but only triggered each seconds

##  Data-driven Events
By using a state machine, both value changes and state transitions can generate data-driven events, taking into account previous values. This dynamic triggering turns ECA to active rules.
* `on:change`: on each change of data value
* `as:stated`: like as:always, but action only is triggered once when if-condition result is altered from false to true
* `as:steady`: like as:stated, but action only is triggered when condition result stays true for a certain time in seconds.
* `as:activated`: like as:always, but action always is triggered when if-condition result becomes true
* `as:altered`: like as:always, but action always is triggered when if-condition result is altered from false to true or from true to false

## Response Events
* `on:response`: on receiving response from request 
* `on:error`: on error of handling request

## Detection Events
The behavior of an AR application is primarily controlled by installing the necessary detectors to receive the corresponding detection events.

### Specialized Detector Types
| Detector Type | Description |
|---|---|
| Location Detector | Tracks world location and device pose in environment. |
| Feature Detector | classifies feature as video stream label. |
| Segment Detector | tracks feature as image segment in video stream. |
| Plane Detector | detects plane in 3D space. |
| Image Detector | recognizes and tracks image or marker in 3D space. |
| Text Detector | detects text matched by regular expression in video or 3D. |
| Code Detector | detects QR/barcode matched by regex in video or 3D. |
| Object Detector | detects object by shape in image or 3D. |
| Face Detector | tracks facial parts of humans in video or 3D. |
| Hand Detector | tracks hand, fingers, and gestures in 3D. |
| Body Detector | tracks body parts and joints of humans in video or 3D. |
| Speech Detector | recognizes voice commands. |
| Transmitter Detector | locates signal and position of wireless sender. |

* `on:detect`: on detecting occurrence of depicted type
* `on:track`: on tracked changes in occurrence of depicted type

## Notification Events
* `on:voice`: on voice command from speech recognition system
* `on:enter`: on enter of participant in collaboration session
* `on:message`: on message from participant in collaboration session 
* `on:leave`: on leave of participant in collaboration session
