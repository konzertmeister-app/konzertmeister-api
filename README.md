# Konzertmeister-API
Public API documentation of the Konzertmeister platform

## Server URL

The Konzermeister Server is accessible at `https://rest.konzertmeister.app`

## Authentication of Requests

You need an API-Key in order to access the Konzertmeister API Endpoints. For now you have to contact
[Konzertmeister Support](mailto:support@konzertmeister.app) to get an API-KEY for your asscociation.

The Api-Key has a validty of 3 month and can be used for the Endpoints listed below.

### Request Headers

You have to set the following headers on all your requests to the Konzertmeister Server:

`X-KM-ORG-API-KEY: <API_KEY>`

`KM_CLIENT_VERSION: V_3_1`

`KM_CLIENT_TYPE: THIRD_PARTY`



## Data Types

* Datetime: we use `ISO_OFFSET_DATE_TIME` format
    * example: `2011-12-03T10:15:30+01:00`


## Get upcoming appointments

> `GET /api/v2/upcomingappointments?limit=10&types=1,2`

Query Paramters:

* limit: the maximum number of appointments that are returned. *optional - defaulted to 10*

* types: comma seperated list of the appointment types - *optional* - default is deliver all types*
    * 1: Rehearsal
    * 2: Concert
    * 3: Misc
    * 4: Rehearsal Request
    * 5: Concert Request


Repsonse Content-Type `application/json
---

```json
[
  {
      "id": 0,
      "name": "string",
      "description": "string",
      "start": "datetime",
      "end": "datetime",
      "attendanceLimit": 10,
      "publicSharingUrl": "URL",
      "typId": 1,
      "active": true
  }
]
```


