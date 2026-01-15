This document describes an observation of meteorological variables captured in a station in a concrete moment. It is based on the Smart Data Model [WeatherObserved](https://github.com/smart-data-models/dataModel.Weather/tree/adf1dd5918da36980208a0a46ed76c81fba91ea5).

# id
**Description**: A unique identifier for the document, in this case, WeatherObserved.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


# type
**Description**: Type of NGSI entity, in this case WeatherObserved.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://github.com/smart-data-models/dataModel.Weather   | String       | WeatherObserved |

# stationCode
**Description**:  A unique identifier for the Station where the measurement was done.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

# wheatherObservations[]

## variableName
**Description**: Name of the variable being measured. See `nom_variable` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-variables-meteorol-giques/4fb2-n3yi/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-variables-meteorol-giques/4fb2-n3yi/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String   |        "C6"          |

## variableCode
**Description**: 2-digit numerical code identifying the measured meteorological variable (e.g., temperature, humidity, wind speed). See `codi_variable` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/data_preview). 

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer  |        33 |

## lectureValue 
**Description**: Numeric value obtained in the measurement. See `valor_lectura` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/data_preview)

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number |  Number|     91 |

## lectureUnit
**Description**: Unit of the measurement (e.g., °C, %, m/s). See `unitat` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-variables-meteorol-giques/4fb2-n3yi/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-variables-meteorol-giques/4fb2-n3yi/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text|  String |     "%"|

## observationType
**Description**: Type of measurement, such as instantaneous, mean, maximum, or minimum. See `codi_tipus_var` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-variables-meteorol-giques/4fb2-n3yi/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-variables-meteorol-giques/4fb2-n3yi/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text|  String |     "DAT"|

## temporalBase
**Description**: Time interval or frequency considered when obtaining the measurement. It can be HO (hourly) or SH (half-hourly). See `codi_base` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text|  String |     "HO" or "SH"|

## validityStatus
**Description**: Quality or validation status of the measurement. The possible values are: empty (the validation process has not been initiated), "T" (the validation process has been initiated, but not finished) and "V" (data has been validated). See `codi_estat` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data) and example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text|  String     |   "", "T" or "V"     |

## lectureTimestamp
**Description**: Exact timestamp in which the variable was measured. See data_lectura at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data) 

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime | DateTime | "2025-10-14T11:00:00Z" |

## extremeValueTimestamp

**Description**: Exact timestamp in which the the extreme value was measured. It only applies whenever an extreme value is measured, the value of the timestamp is empty otherwise. See `data_extrem` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data) and example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime | DateTime | "2025-10-14T11:00:00Z" |

# Example

**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "id": "WeatherObserved:b728d03e-c983-4322-8a46-2bf126b403de",
  "type": "WeatherObserved",
  "stationCode": "ST08019",
  "weatherObservations": [
    {
      "variableName": "Relative Humidity",
      "variableCode": 33,
      "lectureValue": 91.2,
      "lectureUnit": "%",
      "observationType": "DAT",
      "temporalBase": "HO",
      "validityStatus": "V",
      "lectureTimestamp": "2025-10-14T11:00:00Z",
      "extremeValueTimestamp": ""
    }
  ],
  "@context": [
    "https://smartdatamodels.github.io/dataModel.Weather/WeatherObserved/context.jsonld"
  ]
}

```
