The Data Sharing Agreement (DSA) is the final document which establishes a link between the DSC and DSR, this document is tokenized and signed by the Data Intermediary and the data user. The conditions of the data access is established with a period of review and limitation of scope. 

See sharing agreement statuses in P7012: 
https://w3c.github.io/dpv/2.1/standards/p7012/#vocab-status

# context
**Description:** Defines the context of any this document. E.g. the link to the JSON-LD

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/url  |   URL              | https://schema.org/   |

# type
**Description:** The name of the type document (in this case, DSA)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Thing  |   Text             | DataSharingAgreement  |

# id
**Description:** A unique identifier for the DSA.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

# userId

**Description:** A unique identifier for the user requesting information.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


# controllerId
**Description:** A unique identifier for the entity that acts as an intermediary of the agreement.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


# requestId

**Description:** A unique identifier for the DSR linked to this agreement.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


# previousDSA

**Description:** A unique identifier for the previous DSA in case of consent revocation.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


# datasets

In addition, the list of datasets with the following information: 

## datasetId

**Description:** A unique identifier of the dataset.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de|

## DSCId

**Description:** A unique identifier of the linked Data Sharing Agreement document.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de|

## ownerId

**Description:** A unique identifier of the User that owns the dataset.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

## retentionPeriod

**Description:** The allowed storage or retention period for the requested dataset (should match the requested period and the retention period from the original dataset).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.2/dpv/#StorageDuration   | String ([ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)) | `"P6M"`, `"P24M"`, `"P60M"`, `"P120M"` or `"Undefined"` |
----

## events[]

**Description:** It is a list of objects that describes each status and its timestamp of the negotiation process **for each of the datasets**. The statuses follow the [IEEE P7012 vocabulary](https://w3c.github.io/dpv/2.1/standards/p7012/#vocab-status).


### userId
**Description:** Refers to the unique identifier of the user that performed the action described in the event.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid | String| "b728d03e-c983-4322-8a46-2bf126b403de" |


### eventId
**Description:** The unique identifier corresponding to the event, i.e., to the action taking place.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid | String |  b728d03e-c983-4322-8a46-2bf126b403de|

### status
**Description:** The status of the agreement corresponding to the event. Additional statuses can be created, such as "UserNotified", "TimeOut", etc.

- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementNegotiationRequested
- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementRefused
- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementAccepted
- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementNegotiationTerminated

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementNegotiationStatus | String | `AgreementNegotiationRequested`, `AgreementAccepted`, `AgreementRefused` and `AgreementNegotiationTerminated`|

### timestamp
**Description:** The exact timestamp of the event.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTimes https://schema.org/DateTime | DateTime | "2025-10-14T11:00:00Z" |

----
# events[]

**Description:** It is a list of objects (events) that describes events in the general document and its timestamp of the negotiation process. The statuses follow the [IEEE P7012 vocabulary](https://w3c.github.io/dpv/2.1/standards/p7012/#vocab-status). Each object has 3 attributes: userId, eventId and status.


## userId
**Description:** Refers to the unique identifier of the user that performed the action described in the event.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid | String| "b728d03e-c983-4322-8a46-2bf126b403de" |


## eventId
**Description:** The unique identifier corresponding to the action taking place.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid | String |  b728d03e-c983-4322-8a46-2bf126b403de|

## status
**Description:** The status of the agreement corresponding to the event. 

- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementNegotiationRequested
- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementRefused
- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementAccepted
- https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementNegotiationTerminated

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://w3c.github.io/dpv/2.1/standards/p7012/#AgreementNegotiationStatus | String | `AgreementNegotiationRequested`, `AgreementAccepted`, `AgreementRefused` and `AgreementNegotiationTerminated`|

## timestamp
**Description:** The exact timestamp of the event.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTimes https://schema.org/DateTime | DateTime | "2025-10-14T11:00:00Z" |

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

**Description:** The exact timestamp of when the agreement was signed.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Boolean   | Boolean | True or False |


# timestamp

**Description:** The exact timestamp of when the document is created.
| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime   | DateTime | 2025-10-15T14:23:00Z |


# Example
**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "@context": "https://datalog.es/",
  "@type": "DataSharingAgreement",
  "@id": "b728d03e-c983-4322-8a46-2bf126b403de",

  "userId": "a1111111-b222-cccc-dddd-eeeeeeeeeeee",
  "controllerId": "b2222222-c333-dddd-eeee-ffffffffffff",
  "requestId": "c3333333-d444-eeee-ffff-111111111111",
  "previousDSA":"d534073333-d444-eeee-ffff-111111111111",
  "datasets": [
    {
      "datasetId": "d4444444-e555-ffff-1111-222222222222",
      "DSCId": "b728d03e-c983-4322-8a46-2bf126b403de",
      "ownerId": "a1111111-b222-cccc-dddd-eeeeeeeeeeee",
      "retentionPeriod": "P12M",
      "events": [
         {
        "userId": "a1111111-b222-cccc-dddd-eeeeeeeeeeee",
        "eventId": "e5555555-f666-1111-2222-333333333333",
        "status": "AgreementNegotiationRequested",
        "timestamp": "2025-10-14T10:00:00Z"
        },
        {...}
      ]
    }
  ],

  "events": [
    {
      "userId": "a1111111-b222-cccc-dddd-eeeeeeeeeeee",
      "eventId": "e5555555-f666-1111-2222-333333333333",
      "status": "AgreementNegotiationRequested",
      "timestamp": "2025-10-14T10:00:00Z"
    },
    {...}
  ],

  "Signature": {
    "proof": "z6MkiTBz1ymuepAQ4HEHYSF1H8quG5GLVVQR3djdX3mDooWp",
    "timestamp": "2025-10-15T14:23:00Z",
    "valid":True
  },

  "timestamp": "2025-10-15T14:23:00Z"
}

```

# Glossary



 
