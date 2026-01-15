This document describes the basic data of a Weather Station, such as location and height. It is base on [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/about_data).

# id
**Description**: A unique identifier for the document, in this case, StationPoint.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |


# type
**Description**: Type of NGSI entity, in this case StationPoint.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data | String       | StationPoint |

# stationCode 

**Description**: 2-character alphanumerical code of the station where the values for the meteorological variable(s) were measured. See `codi_estacio` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Dades-meteorol-giques-de-la-XEMA/nzvn-apee/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String       |     "VF"            |

# locationPoint{}

**Description**: Geographic location of the weather station using GeoJSON Point. See `geocoded_column` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/GeoCoordinates| Object |    `{"type": "Point", "coordinates": [2.15, 41.39]}` |

# height

**Description**: Altitude of the station location above sea level, in meters. See `altitud` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number | Integer |   122 |

# municipalityName

**Description**: Name of the municipality where the station is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String       |     "Barcelona"  |

# municipalityCode

**Description**: Official municipality administrative code. See `codi_municipi` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|     250117           |

# regionName

**Description**: Region where the station is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String       |     "Noguera"  |

# regionCode

**Description**: Code identifying the region where the station is located. See `codi_comarca` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String   |     "33"             | 

# provinceName

**Description**: Province name where the station is located.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String       |     "Lleida"  |

# provinceCode

**Description**: Code identifying the province where the station is located. See `codi_provincia` at [XEMA standards](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/about_data) and the example values at [XEMA data](https://analisi.transparenciacatalunya.cat/Medi-Ambient/Metadades-estacions-meteorol-giques-autom-tiques/yqwd-vj5e/data_preview).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text   | String       |     "25"  |

# Example

**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "id": "StationPoint:b728d03e-c983-4322-8a46-2bf126b403de",
  "type": "StationPoint",
  "stationCode": "VF",
  "locationPoint": {
    "type": "Point",
    "coordinates": [0.8762, 42.0303]
  },
  "height": 122,
  "municipalityName": "Vilanova de Meià",
  "municipalityCode": "252434",
  "regionName": "Noguera",
  "regionCode": "33",
  "provinceName": "Lleida",
  "provinceCode": "25",
  "@context": [
    "https://smartdatamodels.github.io/dataModel.Weather/WeatherStation/context.jsonld"
  ]
}

```
