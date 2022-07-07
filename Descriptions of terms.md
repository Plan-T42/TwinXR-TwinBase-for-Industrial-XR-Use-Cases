# Descriptions of terms

based on the corresponding file in [AIIC/dt-document](https://github.com/AaltoIIC/dt-document/blob/master/descriptions-of-terms.md) project 

modified specifically for the HoloLens mixed reality application for crane operation.

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
| design parameter | targetOpacity | The opacity of the target holograms in %, by default 70? | optional | float |
| design parameter | operationalAreaDisplayStyle | The style of operational area holograms, either "fill" or "outline", by default "outline"? | optional | string |
| design parameter | operationalAreaBorderThickness | The thickness of the borders of operational area holograms in cm, by default 4? | optional | float |
| design parameter | dashboardPosition | The position of the dashboard center with regard to the user (HoloLens) | optional | array of three float |
| design parameter | dashboardScale | The scale of the dashboard, by default 1 | optional | float |
| design parameter | dashboardAngle| The angle between dashboard and the plane that is vertical to user's sight line, by default 0, i.e. vertical dashboard | optional | float |
| control parameter | markerLocation | The location of the registration marker in crane's hoist, trolley and bridge dimensions (cm) | optional | array of three floats |
| control parameter | operationalAreaHoist | The range of opeational area in crane's hoist dimension (cm) | optional | array of two floats |
| control parameter | operationalAreaTrolley | The range of opeational area in crane's trolley dimension (cm) | optional | array of two floats |
| control parameter | operationalAreaBridge | The range of opeational area in crane's bridge dimension (cm) | optional | array of two floats |
| control parameter | targetNum | The number of the fixed target holograms, by default 4 with each's location pre-defined | optional | int |
| control parameter | targetNumLocationHoist | The location of a target hologram with its number in crane's hoist dimension (cm), should be within the operational area | optional | dictionary of int:float |
| control parameter | targetNumLocationTrolley | The location of a target hologram with its number in crane's trolley dimension (cm), should be within the operational area | optional | dictionary of int:float |
| control parameter | targetNumLocationBridge | The location of a target hologram  with its number in crane's bridge dimension (cm), should be within the operational area | optional | dictionary of int:float |
