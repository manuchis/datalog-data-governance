This document writes down the rules for which the Data Intermediary is mandated to share donor's data to third parties. 
We differentiate broad and dynamic consent modes in our protocol. General policies are defined by broad consent, while dynamic consent is on-demand based consent. 

 
- If broad consent: you will be informed that your data will be given under your preferences, you will have XX days to opt-out, otherwise you will be considered to have accepted the exchange. 

https://w3c.github.io/dpv/2.1/standards/p7012/#vocab-agreement

# context
**Description:** Defines the context of any this document. E.g. the link to the JSON-LD

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/url  |   URL              | https://schema.org/   |

# type
**Description:** The name of the type document (in this case, DSC)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Thing  |   Text             | DataSharingConsent  |

# id
**Description:** A unique identifier.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

-----

# userId
**Description:** A unique identifier for the data owner.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String                  | b728d03e-c983-4322-8a46-2bf126b403de                 |

# SmartDataModel {}

**Description:** Object containing the basic information of the Smart Data Model that the DAC is referred to.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Thing   | String                  | b728d03e-c983-4322-8a46-2bf126b403de                 |

Contains the following attributes:

[id](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#id)
[type](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#type)
[dataProvider](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#dataprovider)
[typeOfSupplyCode](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#typeofsupplycode)
[consumerProfile](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#consumerprofile)
[supplier](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#supplier)
[supplierCode](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#suppliercode)
[timeInterval{}](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#timeinterval)
[startTimestamp](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#starttimestamp)
[endTimestamp](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#endtimestamp)

[typeOfLectureCode](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#typeoflecturecode)
[billingPeriodCode](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#billingperiodcode)
[consumptionPoint](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#consumptionpoint)
[pressureRange](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#pressurerange)
[description](https://github.com/manuchis/datalog-data-governance/wiki/Smart-Data-Model:--GasConsumption#description)

-----
# primary Use
**Description:** Refers to the actions that the Data Intermediary can adopt to ensure the services needed and includes personal data (and should be limited by the DGA):

## acquisitionAllowed
**Description:** Accept the Acquisition of data from the Data Holder

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|      https://schema.org/Boolean         | Boolean | `True` or `False`|

## allowedDuration
**Description:** Defines the duration for which this consent remains valid (in ISO 8601 format).


| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#Duration   | String ([ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)) | `"P6M"`, `"P24M"`, `"P60M"`, `"P120M"` or `"Undefined"` |                 

## serviceDelivery
**Description:** Allows to process the data following the IEEE P7012 standard under a service delivery purpose. Even when the specification supports all the terms, only some are applicable to our use case.  

- [SD-BY](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY) (does not allow to be shared with third party)
- [SD-BY-DP](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-DP) (does not allow to be shared with third party)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|https://w3c.github.io/dpv/2.1/standards/p7012/#ServiceDelivery| Boolean | `True` or `False`|                    

-----
# secondary Use
**Description:** It records extra data processing capacities allowed to be performed by the Data Intermediary. 
## analyticsAllowed
**Description:** Indicates whether the Data Intermediary is allowed to perform analytical processing (second-party use, no third-party sharing).
- [SD-BY-A](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-A) (does not allow to be shared with third party)
- [SD-BY-A-DP](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-A-DP) (does not allow to be shared with third party)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|https://w3c.github.io/dpv/2.1/standards/p7012/#ServiceAnalytics| Boolean | `True` or `False`|   

## trackingAllowed
**Description:** Specifies whether tracking activities are permitted (e.g., behavioral or operational tracking).
- [SD-BY-AT](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-AT) (does not allow to be shared with third party)
- [SD-BY-AT-DP](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-AT-DP) (does not allow to be shared with third party)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|https://w3c.github.io/dpv/2.1/standards/p7012/#Tracking2PAllowed| Boolean | `True` or `False`|   

## profilingAllowed
**Description:** Defines whether profiling or inference-based processing is allowed.
- [SD-BY-ATP](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-ATP) (does not allow to be shared with third party)
- [SD-BY-ATP-DP](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-ATP-DP) (does not allow to be shared with third party)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|https://w3c.github.io/dpv/2.1/standards/p7012/#Profiling2PAllowed| Boolean | `True` or `False` |

## portabilityRequired

**Description:** Specifies whether  Data Portability is required, that is, if the user requires to recover the processed or generated data by the intermediary. The default value is true.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|https://w3c.github.io/dpv/2.1/standards/p7012/#PortabilityRequired| Boolean | `True` or `False`|  

## sharingDataAnonymised3PAllowed 

**Description:** Allows to publish statistics and grouped/aggregated data publicly or to third parties
- [SD-BY-ATP-S3P](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-ATP-S3P)
- [SD-BY-ATP-S3P-DP](https://w3c.github.io/dpv/2.1/standards/p7012/#SD-BY-ATP-S3P-DP)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
|https://w3c.github.io/dpv/2.1/standards/p7012/#SharingDataAnonymised3PAllowed| Boolean| `True` or `False` |

-----

# 3PSharing

## allowedPurpose

**Description:** Specifies the purposes for which data may be shared or used.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#Purpose   | String | `"Comercial"`, `"Marketing"`, `"Internal"`, `"Public Interest"`, `"Research"` |


## allowedDuration

**Description:** Defines how long the consent remains valid or the data can be used.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#Duration   | String ([ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)) | `"P6M"`, `"P24M"`, `"P60M"`, `"P120M"` or `"Undefined"` |

## broadConsentAllowed

**Description:** Indicates whether the donor prefers to give consent for every data request (dynamic) or grant general consent (broad)


| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean   | Boolean | `True` or `False` |

-----

# Dynamic consent variables


## dynamicConsentOptIn

**Description:** Specifies the default decision if the donor does not respond to a dynamic consent request within the defined timeframe.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String | `"RejectByDefault"` or `"AcceptByDefault"`|


## dynamicConsentTimeOut

**Description:** Defines how much time the donor has to respond to a dynamic consent request before it expires

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#Duration   | String ([ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)) | `"P7D"`, `"P30D"` or `"Undefined"`|

-----

# Broad consent variables

## field

**Description:** Identifies the thematic domain or category of data covered by the consent. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String |  `"Agriculture"`, `"Climate"`, `"Mobility"`, `"EnergyWaste"`, `"Health"`, `"Demographics"`|

## 3Party 

**Description:** Specifies the types of third parties that are allowed to receive the data under this consent. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#Recipient | String | `"Research"`, `"Government"`, `"Non-profit"`, `"SME"`, `"Enterprise"`, `"Individual"`|

## retentionPeriod

**Description:** Defines how long the shared data may be retained or stored. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#StorageDuration   | String ([ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)) | `"P6M"`, `"P24M"`, `"P60M"`, `"P120M"` or `"Undefined"` |

## useAI

**Description:** Specifies whether the data can be used for artificial intelligence applications, and what kind. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String | `"Disallowed"`, `"FoundationalModel"`, `"Profiling"`, `"Analytics"`, `"IntentCasting"`|


## useLicense

**Description:** Defines the licensing terms or legal framework governing how the data may be reused or distributed. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/license| String |`"Credit"`, `"Adaptation"`, `"Derivative"`|


## storageLocation

**Description:** Indicates the geographical or jurisdictional location where the data may be stored. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#StorageLocation  | String | `"EEA"`, `"Worldwide"`|

## notification

**Description:** Defines how and when the donor should be notified about data-sharing activities. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text](https://schema.org/Text  | String | `"Always"`, `"Critical"`, `"None"`|

## broadConsentOptOut

**Description:** Indicates whether the donor wants to be informed each time an opt-out option is available. **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean   | Boolean | `True` or `False`|

## broadConsentNotSpecified

**Description:** Defines what should happen if a scenario is not covered by the donor’s preferences (contact or act on behalf). **Optional**, in case of Broad Consent.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String | `"ContactUser"` or `"ActAsRepresentative"`|

# Signature{}

## proof

**Description:** Token of the signature.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String | "z6MkiTBz1ymuepAQ4HEHYSF1H8quG5GLVVQR3djdX3mDooWp" |

## timestamp

**Description:** The exact timestamp of when the agreement was signed.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime   | DateTime | 2025-10-15T14:23:00Z |

## valid

**Description:** Boolean indicating id the consent signature is still valid or not..

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean | Boolean | `True` or `False`|

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

# consentTimestamp

**Description:** The exact timestamp of when the consent is granted.
| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime   | DateTime | 2025-10-15T14:23:00Z |


# Example
**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "@context": "https://datalog.es/",
  "@type": "DataSharingConsent",
  "@id": "b728d03e-c983-4322-8a46-2bf126b403de",

  "userId": "b728d03e-c983-4322-8a46-2bf126b403de",

  "SmartDataModel": {
    "id": "urn:ngsi-ld:GasConsumption:001",
    "type": "GasConsumption",
    "dataProvider": "UtilityCompanyX",
    "supplier": "GasSupplierY",
    "startTimestamp": "2024-01-01T00:00:00Z",
    "endTimestamp": "2024-12-31T23:59:59Z",
    "description": "Annual household gas consumption"
  },

  "primaryUse": {
    "acquisitionAllowed": true,
    "allowedDuration": "P24M",
    "serviceDelivery": true
  },

  "secondaryUse": {
    "analyticsAllowed": true,
    "trackingAllowed": false,
    "profilingAllowed": false,
    "portabilityRequired": true,
    "sharingDataAnonymised3PAllowed": true
  },

  "3PSharing": {
    "allowedPurpose": ["Research", "Public Interest"],
    "allowedDuration": "P12M",

    "broadConsentAllowed": true,
    "broadConsentOptOut": true,
    "broadConsentNotSpecified": "ContactUser",

    "dynamicConsentOptIn": "RejectByDefault",
    "dynamicConsentTimeOut": "P7D"
  },

  "field": "Research",
  "3Party": ["Research", "Non-profit"],
  "retentionPeriod": "P24M",
  "useAI": "Analytics",
  "useLicense": "Credit",
  "storageLocation": "EEA",
  "notification": "Always",

  "Signature": {
    "proof": "z6MkiTBz1ymuepAQ4HEHYSF1H8quG5GLVVQR3djdX3mDooWp",
    "timestamp": "2025-10-15T14:23:00Z",
    "valid": True
  },

  "consentTimestamp": "2025-10-15T14:23:00Z",
  "createdAt": "2025-10-15T14:23:00Z",
  "updatedAt": "2025-10-15T14:23:00Z",
}
```

# Data Sharing Licenses 
To facilitate the process of selecting the broad consent policies, we designed specific licenses that are commonly used in our community ...
TBD

# Glossary
Service Delivery (SD)
Data Portability (DP)
Analytics by Second-Party (A)
Analytics and Tracking by Second-Party (AT)
Analytics, Tracking, and Profiling by Second-Party (ATP)
Share Anonymised Data with Third Party (S3P)
Personal Data Contribution (PDC), i.e., proactive contribution of data by a person towards some specific objective/purpose
Intent Casting (INTENT)
AI Training and Operation (AI)
Public Good (GOOD)