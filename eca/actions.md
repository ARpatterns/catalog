# Actions in AR Applications

Common Actions in AR applications listed by category.

|Category|
|---|
| [Item-Related Actions](#item-related-actions) |
| [Visual-Related Actions](#visual-related-actions) |
| [UI-Related Actions](#ui-related-actions) |
| [Data-Related Actions](#data-related-actions) |
| [Process-Related Actions](#process-related-actions) |
| [Detector-Related Actions](#detector-related-actions) |

## Item-Related Actions
Items are elements of the application model. An item can be represented as 3D object in the AR scene or as 2D overlay (sprite image, text label, UI element, ...) on top of the AR view.

* `do:add at`: add and anchor item at position
* `do:add onto`: add and anchor item onto another item
* `do:add to`: add item as child to another item
* `do:add ahead`: add and anchor item ahead to user position and orientation
* `do:add overlayed`: add 2D item flat on top of AR view
* `do:remove`: remove item from scene
* `do:replace`: replace item with another item at same position
* `do:move to/by`: move item absolute/relative to new position
* `do:turn to/by`: turn item absolute/relative to new orientation
* `do:tint`: set color of item
* `do:lock/unlock`: lock/unlock item to control allowed manipulation

## Visual-Related Actions
Visual-related actions do change the visual representation of items in the AR scene but are not reflected or stored in the application model.

* `do:hide/unhide`: hide/unhide visual representation of item 
* `do:translate to/by`: move absolute/relative 
* `do:rotate to/by`: rotate absolute/relative 
* `do:scale to/by`: scale absolute/relative 
* `do:animate key`: create animation of graphical parameter (key) 
* `do:stop key`: stop animation of graphical parameter (key) 
* `do:occlude`: set geometry of 3D node as occluding but not visible 
* `do:illuminate`: add additional lightning to hot spot (from above or from camera)

## UI-Related Actions
Common actions to control the user interface of an AR application.

* `do:prompt`: show instruction in a pop-up panel 
* `do:confirm`: get a YES/NO confirmation via an pop-up dialog panel 
* `do:warn`: set warning or status label 
* `do:vibrate`: vibrate device 
* `do:play`: play system sound 
* `do:stream`: play remote audio file 
* `do:pause`: pause current audio stream 
* `do:say`: say something using text-to-speech (TTS) system 
* `do:listen`: start speech recognition system and subscribe 
* `do:open service`: open service menu 
* `do:open catalog`: open item catalog 
* `do:install`: install item catalog entry or service menu entry 
* `do:filter`: filter item catalog or service menu 
* `do:screenshot`: take screen snapshot 
* `do:snapshot`: take photo shot

## Data-Related Actions
* `do:assign`: set a data variable to a value 
* `do:concat`: concatenate a string with an existing variable 
* `do:select`: select a value from a menu and assign to data variable 
* `do:eval`: set a data variable by evaluating an expression 
* `do:fetch`: fetch data from remote and map to internal data 
* `do:clear`: delete data variable

## Process-Related Actions
* `do:save`: save the AR scene / application model 
* `do:exit`: end AR session 
* `do:execute`: execute function(s) 
* `do:service`: execute service action 
* `do:workflow`: execute workflow action 
* `do:request`: request action from remote server and execute

## Detector-Related Actions
* `do:detect type`: install detector for type (feature, text, plane, image, ...) 
* `do:halt`: deactivate detector 
* `do:redetect`: reactivate detector