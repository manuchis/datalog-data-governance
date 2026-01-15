This document defines an extended set of descriptive and contextual attributes for the ConsumptionPoint entity within the [Smart Data Models – Consumption domain](https://smart-data-models.github.io/dataModel.Consumption/ConsumptionPoint/)
.
These features provide additional information about the functional characteristics, usage, and physical attributes of the consumption point, such as its category, occupancy, thermal systems, and construction details.

This extension aims to enhance analytical capabilities and contextual understanding for use cases involving energy, water, or gas consumption, by linking operational data with building or infrastructure context.

# id

**Description**: A unique identifier for the Consumption Point.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

# CUPS

**Description**: Unique identifier (20–22 characters) assigned to each electricity or gas supply point, independent of the energy retailer.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text | String | "ES0021000001234567AB"|

# type 

**Description**:  NGSI entity type, in this case "ConsumptionPoint".

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://smartdatamodels.org/dataModel.Consumption/ConsumptionPoint   | String       | ConsumptionPoint |

# owner 

**Description**: A unique identifier for the owner of the Consumption Point. It can reference an organization, municipality, company, or individual who owns or operates the point.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

----
# address{} 
 
**Description**: Mailing address or location of the Consumption Point, following the [Schema.org Address model](https://schema.org/address).
Includes the locality, postal code, and other components of a physical or postal address.

## postalCode 

**Description**: Postal Code of the address where Consumption Point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/https://schema.org/postalCode |   String | "24004 "  |

## addressCountry 

**Description**: Country where consumption point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/addressCountry  |   String | "Spain"  |

## addressLocality 

**Description**: Locality where consumption point is located.


| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/addressLocality  |   String | "Barcelona"  |

## addressRegion 

**Description**: Region or autonomous community where consumption point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/addressRegion  |   String | "Catalonia"  |

## districtName

**Description**: Street where consumption point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/streetAdress |   String | "Llacuna"  |

## districtName

**Description**: Name of the district where consumption point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/AdministrativeArea |   String | "Sant Martí"  |

## districtCode

**Description**: Code of the district where consumption point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text |   String | "07"  |

## neighborhoodName

**Description**: Name of the neighborhood where consumption point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DefinedRegion  |   String | "Sant Pere, Santa Caterina i la Ribera"  |

## neighborhoodCode

**Description**: Code of the neighborhood where Consumption Point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/https://schema.org/Text |   String | "04 "  |

----
# consumptionPointFeatures{}

**Description**: Object containing set of attributes that describe the functional, operational, and occupancy characteristics of the Consumption Point, such as its category, usage type, occupancy, and thermal systems. The object contains 3 main objects that organize the different types of features: staticFeatures, operationalFeatures, and equipmentFeatures.

## staticFeatures{}
**Description**: Attributes that describe permanent characteristics of the consumption point and its infrastructure, such as construction year, surface area, orientation, or building category.

### location{} 

**Description**: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/GeoCoordinates | Object  | "{ "type": "Point", "coordinates": [2.195, 41.514] }" |

### category 

**Description**: Indicates whether the point corresponds to a building, office, etc.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String | "Building" |  

### constructionYear

**Description**: Year of construction of the infrastructure or assetwhere the Consumption Point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer | 1980|  

### surface

**Description**: Surface in square meters of the infrastructure or assetwhere the Consumption Point is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer | 50 |  

### orientation

**Description**: Indicates the predominant compass direction of the main façade or exposure of the asset (e.g., North, South, East, West).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String | "North" |  

## operationalFeatures{}

**Description**: Attributes that describe how the consumption point is typically used or occupied.

### usageType

**Description**: Defines the primary purpose or activity for which the consumption point is used (e.g., residential, educational, industrial, commercial, etc.).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String | "Residential" |  

### occupancyPattern  

**Description**: Indicates the temporal pattern of occupancy or usage of the point — for example, whether it is permanently occupied, seasonal, or limited to office hours.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String | "Seasonal" |  

### numberOfUsers
 
**Description**: Estimated number of users who inhabit or regularly use the facilities served by this consumption point.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number   | Integer | 2|  

## equipmentFeatures{}

**Description**: Attributes describing the presence of heating, cooling, or major household equipment that can significantly influence energy consumption at the consumption point. These features are optional and may change over time.

### electricHeating

**Description**: Indicates whether the consumption point has an electric heating system. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String| `true` or `false`|  

### gasHeatingType

**Description**: Indicates whether the consumption point has a gas-based heating system. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String| "Gas", `true` or `false`|  

### ACRooms

**Description**: Number of rooms with Air Conditioning present in the infrastructure.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer | 3|


### electricDishwasher

**Description**: Indicates whether there is an electric dishwasher at the consumption point. Optional. 

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|  


### electricOven

**Description**: Indicates whether there is an electric oven at the consumption point. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|  

### gasOven

**Description**: Indicates whether there is a gas oven at the consumption point. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|  

### washingMachine

**Description**: Indicates whether there is a washing machine at the consumption point. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|  

### electricDryer

**Description**: Indicates whether there is an electric clothes dryer installed at the consumption point. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|  

### numberOfBathrooms

**Description**: Number of complete bathrooms present in the infrastructure. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer | 1 |

### numberOfToilets

**Description**: Number of toilet rooms present in the infrastructure. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer | 2 |

### swimmingPool

**Description**: Boolean type indicating whether there is a swimming pool in the infrastructure. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|

### garden

**Description**: Boolean type indicating whether there is a garden in the infrastructure. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|

### terrace

**Description**: Boolean type indicating whether there is a terrace in the infrastructure. Optional.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean| Boolean| `true` or `false`|

----
# dateCreated

**Description**: Entity creation timestamp.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime | DateTime | "2025-10-14T11:00:00Z" |

# dateModified

**Description**: Timestamp of the last modification of the entity.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime | DateTime | "2025-10-14T11:00:00Z" |

# description

**Description**: Further description of this item

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String | "Consumption Point of second residence" |


# Example

**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "id": "b728d03e-c983-4322-8a46-2bf126b403de",
  "type": "ConsumptionPoint",
  "owner": "a928d03e-c983-4322-8a46-2bf126b403de",
  "address": {
    "postalCode": "08019",
    "addressCountry": "Spain",
    "addressRegion": "Catalonia",
    "addressLocality": "Barcelona",
    "districtName": "Sant Martí",
    "districtCode": "10",
    "neighborhoodName": "El Poblenou",
    "neighborhoodCode": "04"
  },
  "consumptionPointFeatures": {
    "staticFeatures": {
      "category": "Building",
      "constructionYear": 1980,
      "surface": 85,
      "orientation": "North",
      "location": {
        "type": "Point",
        "coordinates": [2.195, 41.514]
      }
    },
    "operationalFeatures": {
      "usageType": "Residential",
      "occupancyPattern": "Permanent",
      "numberOfUsers": 4
    },
    "equipmentFeatures": {
      "electricHeating": true,
      "gasHeatingType": "Gas",
      "ACRooms": 3,
      "electricDishwasher": true,
      "electricOven": true,
      "gasOven": false,
      "washingMachine": true,
      "electricDryer": false,
      "numberOfBathrooms": 2,
      "numberOfToilets": 1,
      "swimmingPool": false,
      "garden": true,
      "terrace": true
    }
  },
  "dateCreated": "2025-10-14T11:00:00Z",
  "dateModified": "2025-10-20T12:00:00Z",
  "description": "Consumption Point in a residential building",
  "@context": [
    "https://smartdatamodels.github.io/dataModel.Consumption/context.jsonld"
  ]
}


```
