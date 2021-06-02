# cordova.plugins.uid
Note: This plugin is forked from this [repository](https://github.com/hygieiasoft/cordova-plugin-uid).

Cordova plugin to get unique identifiers: UUID, IMEI, IMSI, ICCID and MAC.

This plugin defines a `cordova.plugins.uid` object.
The object is not available until after the `deviceready` event.

		document.addEventListener('deviceready', onDeviceReady, false);
		function onDeviceReady() {
				console.log(cordova.plugins.uid.IMEI);
		}

## Installation
		cordova plugin add https://github.com/ivanchaz/cordova-plugin-uid

## Properties

| Property Name | Android |                                                       IOS                                                      |
|---------------|---------|:--------------------------------------------------------------------------------------------------------------:|
| uid.UUID          |    ✓    |                                                        ✗                                                       |
| uid.IMEI          |    ✓    |                                                        ✗                                                       |
| uid.IMSI          |    ✓    |                                                        ✗                                                       |
| uid.ICCID         |    ✓    | ✓ (Not exactly an ICCID, more like combination of  `carrierName`, `mobileCountryCode` and `mobileNetworkCode`) |
| uid.IMSI          |    ✓    |                                                        ✗                                                       |

Note: All properties that is not checked are not available.

## uid.UUID
The `uid.UUID` gets the device's Universally Unique Identifier ([UUID](http://en.wikipedia.org/wiki/Universally_Unique_Identifier)).

## uid.IMEI
The `uid.IMEI` gets the device's International Mobile Station Equipment Identity ([IMEI](http://en.wikipedia.org/wiki/International_Mobile_Station_Equipment_Identity)).

## uid.IMSI
The `uid.IMSI` gets the device's International mobile Subscriber Identity ([IMSI](http://en.wikipedia.org/wiki/International_mobile_subscriber_identity)).

## uid.ICCID
The `uid.ICCID` gets the sim's Integrated Circuit Card Identifier ([ICCID](http://en.wikipedia.org/wiki/Subscriber_identity_module#ICCID)).

## uid.MAC
The `uid.MAC` gets the Media Access Control address ([MAC](http://en.wikipedia.org/wiki/MAC_address)).
