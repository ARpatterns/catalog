# Geolocated Remark Pattern
> Augmentations placed at specific geographic locations

<img src="images/GeolocatedRemark.png">

## What is the Geolocated Remark Pattern?

The _Geolocated Remark_ pattern is about placing AR augmentations at locations defined by map coordinates. Most often, _Geolocated Remark_ augmentations are used in conjunction with GPS-enabled devices, and try to enforce the correct location of the user. Examples of _Geolocated Remarks_ are pervasive games like Pokemon Go, where monsters spawn at specific geographic locations, as well as map applications

 Typically, the reaction to a geolocated remark is presented as text in the 2D user interface or as audio feedback. 


## Requirements

* _Anchored_: On GPS location
* _Placed_: On GPS location, often paired with _Attention Director_ pattern to help users identify their own relative position.
* _Aligned_: N/A or towards user


## Related Patterns


## Technical Considerations

Due to the precision restrictions of GPS signals, the reaction is not precisely placed in 2D or 3D space.

Geolocated Remarks require AR devices with GPS capabilities if enforcing the actual location of the user is important. Otherwise, simply entering an address or coordinates can and should be offered. Location spoofing is an issue with the _Geolocated Remark_ pattern: In Pokemon Go, for example, developer Niantic has taken considerable measures to prevent or discourage location spoofing.
Often however, geolocated remark patterns exist to provide better usability, for example in map or navigation applications. 


## Scenarios and Examples
- Gaming: 

## Event-Condition-Action Diagram

A geolocated remark is a rule that is triggered by GPS location data (latitude and longitude) or by address data (i.e., country, city, street, building name).
