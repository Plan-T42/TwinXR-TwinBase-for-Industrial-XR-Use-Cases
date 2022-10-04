# Descriptions of terms

Based on the corresponding file in [AIIC/dt-document](https://github.com/AaltoIIC/dt-document/blob/master/descriptions-of-terms.md) project 

Modified specifically for the HoloLens mixed reality application for crane operation.

## Main terms

| Term | Subterms | Description | Assignment | Type |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| version  |  | The version of the digital twin document | mandatory | string |
| privacy  |  | The privacy of the digital twin | mandatory | string |
| id  |  | The digital twin id | mandatory | string |
| name  |  | Name of the digital twin | mandatory | string |
| description  |  | The description of the document | mandatory | string |
| createdMachine  |  | The creation date of the digital twin document (machine-readable) | mandatory | string |
| createdHuman  |  | The creation date of the digital twin document (human-readable)| mandatory | string |
| modifiedMachine  |  | The modification date of the digital twin document (machine-readable) | optional | string |
| modifiedHuman  |  | The modification date of the digital twin document (human-readable)| optional | string |
| owner  |  | Owner of the physcial asset | optional |  |
| contact  |  | The contact person of the digital twin | optional | string |
|   | name* | The name of the contact person | mandatory | string |
|   | email* | The email of the contact person | mandatory | string |
| location  |   | Location of the physcial asset | optional | string |
|   | streetAddress* | The street address of the location | mandatory | string |
|   | gpsCoordinates* | The gps coordinates of the location | mandatory | string |
| manufacturer  |  | The manufacturer of the physical twin | optional | string |
| apiGatewayAddress  |  | Address of the API gateway of the Data Link | optional | string |
| relations  |  | Relations to other digital twins | optional | string |
|   | id* | The id of the other digital twin | mandatory | string |
|   | relationType* | The relation type between the digital twins -> options: "parent", "sibling", "child" | mandatory | string |
| features  |  | The features that include information of the digital twin | optional | string |
|   | name*  | The name of the feature | mandatory | string |
|   | description*  | The description of the feature | mandatory | string |
|   | address | The internet address of the feature | optional | string |
|   | requirement*  | The requirement needed to access the feature | mandatory | string |
|   | documentation  | The internet (or other) address of the documentation of the feature | optional | string |
|   | keywords* | The keywords of the information that the feature contains | mandatory | string |
|   | custom** | A custom field that can be added to describe the feature | optional | string |
|   | parameters** | The internal parameters of the feature (application) that are relevant to be defined within the DT document | optional | string or int or float |


<br>
* mandatory subterm <br>
** any key-value pair is allowed


## Parameters for HoloCrane application 

The interal parameters of the mixed reality interface for crane operation, i.e the HoloCrane application, are specified as follows:

|  Parameter Types  |  subterm  | description | Assigment | Type |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| design parameter | targetColor | The color of the target holograms, by default yellow  | optional | string |
| design parameter | targetShape | The shape of the target holograms, by default sphere | optional | string |
| design parameter | targetSize | The size of the target holograms in cm, by default 20cm diameters (sphere) | optional | float |
| design parameter | targetOpacity | The opacity of the target holograms in %, by default 70 | optional | float |
| design parameter | dashboardPosition | The position of the dashboard center with regard to the user (HoloLens) | optional | array of three float |
| design parameter | dashboardScale | The scale of the dashboard, by default 1 | optional | float |
| design parameter | dashboardAngle| The angle between dashboard and the plane that is vertical to user's sight line, by default 0, i.e. vertical dashboard | optional | float |
| design parameter | visibilityUI - dashboard | whether dashboard UI is visible, by default true | optional | boolean |
| design parameter | visibilityUI - targets | whether targets UI is visible, by default true | optional | boolean |
| design parameter | visibilityUI - instructions | whether instructions UI is visible, by default true | optional | boolean |
| design parameter | instructions | instructions about the XR applcation | optional | string |
| design parameter | safetyZoneDisplayStyle | The hologram style of operational safe zone, either "fill" or "outline", by default "outline" | optional | string |
| control parameter | markerLocationBridge | The location of the registration marker in crane's bridge dimension (cm) | optional | float |
| control parameter | markerLocationTrolley | The location of the registration marker in crane's trolley dimension (cm) | optional | float |
| control parameter | markerLocationHoist | The location of the registration marker in crane's hoist dimension (cm) | optional | float |
| control parameter | safetyZoneHoist | The range of operationally safe zone in crane's hoist dimension (cm) | optional | array of two floats |
| control parameter | safetyZoneTrolley | The range of operationally safe zone in crane's trolley dimension (cm) | optional | array of two floats |
| control parameter | safetyZoneBridge | The range of operationally safe zone in crane's bridge dimension (cm) | optional | array of two floats |
| control parameter | targetLocationHoist | The location of a target in crane's hoist dimension (cm), should be within the operational area | optional | float |
| control parameter | targetLocationTrolley | The location of a target in crane's trolley dimension (cm), should be within the operational area | optional | float |
| control parameter | targetLocationBridge | The location of a target in crane's bridge dimension (cm), should be within the operational area | optional | float |
