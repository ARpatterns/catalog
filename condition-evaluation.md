# Condition Evaluation Within Spatial AR Context

The data model reflecting the AR context is exposed for condition evaluation for any ECA rule. This model typically includes the following types of data:

| Data Type | Description |
|---|---|
| Session Data| time, date, device data, temporary data variables, UI mode |
| Location Data | longitude, latitude, address, country, ambience |
| User Data | position, orientation (tilt, yaw), name, user settings |
| Detected Occurrences | results of installed detectors
| Augmentation Items | model elements with visual representation (scene nodes) |

Conditions are typically formulated by predicates as logical statements using an expression syntax that has access to key-values in the data model. Additionally spatial functions can be included in condition evaluations such as:

| Spatial Function | Description |
|---|---|
| Existence | does item with ID exist in AR world |
| Visibility | is item with ID visible to user |
| Proximity | distance in meters from user (virtual camera) to item with ID |
| Gazing | is user gazing at item with ID |
| Geo-Distance | distance in meters from user to place in latitude/longitude |