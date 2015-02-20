### Control Types
The meta topic ```/devices/$SystemId/controls/$deviceUniqueControlId/meta/type``` defines different types of controls that decide which interface is shown to the user.

#### Switch
A control that toggles it's value when pressed by the user.
* Meta topic value: switch
* Possible values: 0 or 1

#### Range
A range slider that takes integer values between 0 and any other integer that is greater 1
* Meta topic value: range
* Possible values: 0 - max
* Default max: 255
Different values can be set by publishing an arbitrary integer that is greater than 1 to ```/devices/$SystemId/controls/$deviceUniqueControlId/meta/max```.

#### Text
A read-only control that displays it's value as text.
* Meta topic value: text
* Possible values: Anything

#### Generic value type control

A read-only control for a arbitrary value.

* Meta type value: "value"
* Possible values: float

Units should be specified in "meta/units" topic.



#### Specific value type controls

A read-only control for a certain type of value.

| Type 	| meta/type	| units  	| value format  	|   	|
|---	|---	|---	|---	|---	|
| Temperature  	| temperature| °C  	| float  	|   	|
| Relative humidity  	| rel_humidity| %, RH  	| float, 0 - 100  	|   	|
| Atmospheric pressure  	| atmospheric_pressure | millibar (100 Pa)  	| float  	|   	|
| Relative humidity  	| rel_humidity| %, RH  	| float, 0 - 100  	|   	|
| Precipitation rate (rainfall rate) | rainfall | mm per hour | float | |
| Wind speed |  wind_speed | m/s | float | |
| Power |  power | watt | float | |
| Power consumption |  power_consumption | kWh | float | |