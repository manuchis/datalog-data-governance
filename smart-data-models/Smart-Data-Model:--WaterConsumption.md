This document defines an extended set of descriptive and contextual attributes for the ConsumptionCost entity within the [Smart Data Models – Consumption domain](https://smart-data-models.github.io/dataModel.Consumption/ConsumptionPoint/). The entity ConsumptionCost represents a record or summary of resource consumption (electricity, water, gas, etc.) over a defined period. Each record is associated with a specific ConsumptionPoint and may include metadata about measurement, provider, and observed time interval.

# id
**Description**: A unique identifier for the Consumption Record.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

# type

**Description**:  NGSI entity type, in this case "WaterConsumption".

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://smartdatamodels.org/dataModel.Consumption/ConsumptionCost   | String       | WaterConsumption|

# dataProvider

**Description**: A unique identifier for the provider of the Consumption Record. This can refer to an organization, municipality, company, or individual responsible for the data.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://dictionary.mydata.org/prodserv/#uid   | String       | b728d03e-c983-4322-8a46-2bf126b403de                 |

# typeOfSupplyCode

**Description**: Descriptor of the mandatory supply type. Examples include building, commercial premises, offices, etc. Based on https://tramitesanonimos.cnmc.gob.es/tabla/62_TIPO_SUMINISTRO_CIE.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|"OF"|  

# consumerProfile

**Description**: Descriptor of the consumer profile, i.e., industrial or domestic. Based on https://tramitesanonimos.cnmc.gob.es/tabla/GAS_PERFIL_CONSUMO.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|"01"|  

# supplier

**Description**: TName of the company providing the resource or utility service (such as electricity, gas, or water). It refers to the supplier or commercial entity that bills or distributes the consumed resource.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|"Naturgy"|  

# supplierCode

**Description**: Alphanumeric code of length 4 that identifies the retailer (supplier) associated with the reported supply point. If no value exists, the field shall be left blank. In the case of a direct consumer in the market, if no REE code is available, the code “0000” shall be used. Based on https://www.esios.ree.es/es/descargas.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|"0522"|  

# timeInterval{}

## startTimestamp 
**Description**: Object that defines the billing period. Contains the attributes startTimestamp and endTimestamp.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime  | DateTime | "2025-10-14T11:00:00Z" | 

## endTimestamp

**Description**: Year corresponding to the consumption record.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime  | DateTime | "2025-10-14T11:00:00Z" |  

# dateCreated

**Description**: Timestamp when the entity was created in the system.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime  | DateTime | "2025-10-14T11:00:00Z" |    

# dateModified

**Description**: Timestamp of the last modification of this record.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime  | DateTime | "2025-10-14T11:00:00Z" |   

# typeOfLectureCode

**Description**: It can be real (R) or estimated (E).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text  | String | "R" or "E"  |


# billingPeriodCode

**Description**: Code indicating the billing period applicable to the supply point (e.g., monthly or bimonthly). Based on: https://tramitesanonimos.cnmc.gob.es/tabla/108_PERIODO_FACTURACION.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text | String | "01" |  

# maxFlow

**Description**: Object indicating the maximum water flow rate that can pass through or be measured at the supply point (e.g., the rated capacity of the water meter or the maximum design flow of the installation).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number| Number| 3  |
| https://schema.org/Unit| String | "m3/h"|

# minFlow

**Description**: Object indicating the minimum detectable or measurable water flow rate at the supply point. It represents the lower operational limit of the water meter, below which the measurement accuracy is not guaranteed.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number| Number| 3  |
| https://schema.org/Unit| Number| "m3/h" |

# description

**Description**: Further description of the Consumption Record.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text  | String | "Water consumption record for September 2025"   

# consumptionAndCost[]

**Description**: List of consumption readings recorded during the specified period.
Each object in the array represents a single measurement of the consumed resource (e.g., electricity, gas, or water) captured at a specific timestamp.
For example, if water consumption is measured every 15 minutes, the array will contain one object per quarter-hour interval — each including the consumption value, measurement unit, timestamp, and the cost and currency associated with that reading.

## timestamp

**Description**: Datetime when the consumption reading was captured.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/DateTime  | DateTime | "2025-10-14T11:00:00Z" |

## consumption

**Description**: Object containing the value and unit of measured consumption data for a specific resource type.

### value 

**Description**: Numerical value representing the amount of resource consumed during the measurement interval.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number| Number| 0.54 |  

### unit

**Description**: Measurement unit used for the consumption value (e.g., kWh for electricity, m³ for gas or water).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|  "m3/h" |  

## cost

**Description**: Object containing the value and the currency of the total price of the resource consumed in the defined period.

### value

**Description**: Monetary cost corresponding to the consumption recorded in this reading.

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Number| Number| 0.134 | 

### currency 

**Description**: Currency used for the unit price of the consumption value, following the [ISO 4217 standard](https://www.iso.org/iso-4217-currency-codes.html).

| @type         | Expected Type        | Example value(s)     |
| ------------- | -------------        | -------------        |
| https://schema.org/Text| String|  "EUR" |  

# Example

**Description:** Example encoded as [JSON-LD](https://en.wikipedia.org/wiki/JSON-LD) in a HTML script tag.

```
{
  "id": "b728d03e-c983-4322-8a46-2bf126b403de",
  "type": "WaterConsumption",
  "dataProvider": "Ajuntament de Barcelona",
  "supplier": "Aigües de Barcelona",
  "consumptionPoint": "g109d03e-c983-4322-8a46-2bf126b403de",
  "month": 9,
  "year": 2025,
  "dateCreated": "2025-10-14T11:00:00Z",
  "dateModified": "2025-10-20T12:00:00Z",
  "description": "Water consumption record for September 2025",
  "consumptionAndCost": [
    {
      "timestamp": "2025-10-23T00:00:00Z",
      "consumption": {
        "value": 0.54,
        "unit": "m3"
      },
      "cost": {
        "value": 0.081,
        "currency": "EUR"
      }
    },
    {
      "timestamp": "2025-10-23T01:00:00Z",
      "consumption": {
        "value": 0.48,
        "unit": "m3"
      },
      "cost": {
        "value": 0.072,
        "currency": "EUR"
      }
    },
    {
      "timestamp": "2025-10-23T02:00:00Z",
      "consumption": {
        "value": 0.60,
        "unit": "m3"
      },
      "cost": {
        "value": 0.090,
        "currency": "EUR"
      }
    }
  ],
  "@context": [
    "https://smartdatamodels.github.io/dataModel.Consumption/context.jsonld"
  ]
}
```

