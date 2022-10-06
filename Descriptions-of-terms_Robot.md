# Descriptions of terms - Robot arm

Modified specifically for the XR application.

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


## Parameters for HoloRobot application 

The interal parameters of the mixed reality interface for control robot arm, i.e the HoloRobot application, are specified as follows:

|  Parameter Types  |  subterm  | description | Assigment | Type |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| design parameter | dashboardPosition | The position of the dashboard center with regard to the user (HoloLens) | optional | array of three float |
| design parameter | dashboardScale | The scale of the dashboard, by default 1 | optional | float |
| design parameter | dashboardAngle| The angle between dashboard and the plane that is vertical to user's sight line, by default 0, i.e. vertical dashboard | optional | float |
| design parameter | visibilityUI - dashboard | whether dashboard UI is visible, by default true | optional | boolean |
| design parameter | visibilityUI - instructions | whether instructions UI is visible, by default true | optional | boolean |
| design parameter | instructions | instructions about the XR applcation | optional | string |
| design parameter | safetyZoneDisplayStyle | The hologram style of operational safe zone, either "fill" or "outline", by default "outline" | optional | string |
| control parameter | markerLocationX | The location of the registration marker in the pre-defined X dimension (cm) | optional | float |
| control parameter | markerLocationY | The location of the registration marker in the pre-defined Y dimension (cm) | optional | float |
| control parameter | markerLocationZ | The location of the registration marker in the pre-defined Z dimension (cm) | optional | float |
| control parameter | safetyZoneX | The range of operationally safe zone in the pre-defined X dimension (cm) | optional | array of two floats |
| control parameter | safetyZoneY | The range of operationally safe zone in the pre-defined Y dimension (cm) | optional | array of two floats |
| control parameter | safetyZoneZ | The range of operationally safe zone in the pre-defined Z dimension (cm) | optional | array of two floats |
| control parameter | offsetOrientationJoint | The offset orientation of a joint (degree) | optional | float |
| control | defaultSpeedJoint | The default speed of a joint (degree per second) | optional | float |
| control | OrientationRangeJoint | The orientation range of a joint (degree) | optional | array of two floats |
