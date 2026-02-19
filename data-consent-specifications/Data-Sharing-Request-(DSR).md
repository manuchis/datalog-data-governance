The Data Sharing Request (DSR) is the document where the data user reclaim specific data. We consider that datasets are complex group of multiple datasets that are constrained by geographical and timespace boundaries.
Once a data user is interested in a group of data, a matchmaking process ocurrs. This enables our system to compare the request with the consent gave by donors. In case of dynamic consent, consent is required and requested to data donors within a specific time. 
This request tracks each of the datasets requested and the general information about the intended use of the data and retention policies. 
It is also linked to a description of the project or campaign submitted by the data user. At the end, a Data Sharing Agreement (DSA) is signed by the data user based on the final dataset. 

- Information about user, project and outcomes should be linked to the request_

# context
**Description:** Defines the context of any this document. E.g. the link to the JSON-LD

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/url  |   URL              | https://schema.org/   |

# type
**Description:** The name of the type document (in this case, DSR)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Thing  |   Text             | DataSharingRequest  |

# id
**Description:** A unique identifier.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

-----
# DSR variables

## datasets[]
**Description:** List of IDs of each dataset requested.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | ["b728d03e-c983-4322-8a46-2bf126b403de", "b728d03e-c983-4322-8a46-2bf126b873de" ] |



## projectId
**Description:** A unique identifier.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


## field

**Description:** Defines the thematic domain or data category for the requested dataset(s)
| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String |  `"Agriculture"`, `"Climate"`, `"Mobility"`, `"EnergyWaste"`, `"Health"`, `"Demographics"`|

## purpose 

**Description:** Indicates the intended purpose for which the data will be used.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#Purpose   | String | `"Comercial"`, `"Marketing"`, `"Internal"`, `"Public Interest"`, `"Research"` |

## useAI

**Description:** Specifies whether AI technologies will be used, and for what kind of processing.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String | `"Disallowed"`, `"FoundationalModel"`, `"Profiling"`, `"Analytics"`, `"IntentCasting"`|

## useLicense

**Description:** Defines the usage license or conditions under which data can be reused or distributed.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/license| String |`"Credit"`, `"Adaptation"`, `"Derivative"`|

## dpiaUrl

**Description:** Url linking to the formal assessment to determine whether a data processing activity is safe, proportionate, and respectful of privacy, and to identify the measures that should be applied.”

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/url | URL |`https://example.com/dpia`|

## lawfulBasis 

**Description:**: The legal basis under which the data is provided or processed, as defined in the Data Act. This may include legitimate interest, contract, vital interest, or other applicable lawful grounds.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|  https://schema.org/Text| String  |`consent`|

## timeScope

**Description:** Defines the temporal range or period for which the data is requested.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/startDate / https://schema.org/endDate | DateTime | `{ "startDate": "2023-01-01T00:00:00Z", "endDate": "2023-12-31T23:59:59Z"}` |

## geographicalScope

**Description:** Defines the geographical region or jurisdiction that limits the scope of the requested data.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Place   | String | `"Spain"`, `"European Union"`, `"Worldwide"` |

## retentionPeriod

**Description:** Specifies how long the requested data may be stored or used. Expressed in [ISO 8601 format(https://en.wikipedia.org/wiki/ISO_8601).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#StorageDuration   | String ([ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)) | `"P6M"`, `"P24M"`, `"P60M"`, `"P120M"` or `"Undefined"` |

## storageLocation

**Description:** Indicates the geographical or jurisdictional location where data will be stored.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#StorageLocation  | String | `"EEA"`, `"Worldwide"`|

## timestamp

**Description:** The exact timestamp of when the request is submitted.
| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime   | DateTime | 2025-10-15T14:23:00Z |

# createdAt

**Description:** The exact timestamp of when the document is created.
| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime   | DateTime | 2025-10-15T14:23:00Z |

# updatedAt

**Description:** The exact timestamp of the last update of the document.
| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime   | DateTime | 2025-10-15T14:23:00Z |

# Example
**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "@context": "https://datalog.es/",
  "@type": "DataSharingRequest",
  "@id": "f3d9c28b-7a64-41d1-93b0-35cfb5fdc88d",
  
  "userId": "d8b2c03e-54a6-4a29-9d45-7f6e128c30f1",
  "projectId": "a1b5e44d-02c1-42cf-b1a7-fc7b1b93b912",
  datasets[
  ...
  ],
  "field": [
    "Health",
    "Mobility"
  ],
  
  "purpose": [
    "Research",
    "PublicInterest"
  ],
   "lawfulBasis": "consent",
  "useAI": "Analytics",
  "useLicense": "Credit",
  
  "timeScope": {
    "startDate": "2023-01-01T00:00:00Z",
    "endDate": "2024-01-01T00:00:00Z"
  },
  
  "geographicalScope": "Spain",
  "retentionPeriod": "P24M",
  "storageLocation": "EEA",

  "createdAt": "2025-10-15T10:00:00Z"
  "updatedAt": "2025-10-15T10:00:00Z"
}

```

