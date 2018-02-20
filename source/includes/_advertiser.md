# Advertisers

## Create an Advertiser

```shell
curl "https://leasedesk.ptchr-dev.nl/api/v1/advertiser
    -X POST
    -H "Authorization: <your_access_token>"
    -H "Content-Type: application/json"
    -H "Accept: application/json"
    --data {
        "advertiser_id": "test_124",
        "name": "Autobedrijf Janssen",
        "street": "Stationstraat",
        "number": "10",
        "number_extra": "a",
        "zipcode": "1234AB",
        "city": "Maastricht",
        "country": "Nederland",
        "phone": "+31 40 123 45 67",
        "email": "info@autobedrijfjassen.nl",
        "web": "http://autobedrijfjanssen.nl",
    }
```

> The above command returns JSON structured like this:

```json
{
    "data": {
        "id": 1,
        "advertiser_id": "test_124",
        "name": "Autobedrijf Janssen",
        "street": "Stationstraat",
        "number": "10",
        "number_extra": "a",
        "zipcode": "1234AB",
        "city": "Maastricht",
        "country": "Nederland",
        "phone": "+31 40 123 45 67",
        "email": "info@autobedrijfjassen.nl",
        "web": "http://autobedrijfjanssen.nl",
        "created_at": "20-02-2018 11:26:12",
        "updated_at": "20-02-2018 11:26:12"
    }
}
```

This endpoint creates a new Advertiser.

<aside class="warning">Make sure you send the json payload as raw body data to the endpoint.</aside>

### HTTP Request

`POST https://leasedesk.ptchr-dev.nl/api/v1/advertiser/`

### Raw Body Parameters (JSON)

Parameter | Description | Required | Validation Rules
--------- | ----------- | -------- | ----------------
advertiser_id | The ID of the advertiser as it's in your own system | yes | *none*
name | Name of the Advertiser | yes | *none*
street | Street of the Advertiser | no | *max 255 chars*
number | Housenumber of the Advertiser | no | *max 255 chars*
number_extra | Housenumber addition | no | *max 255 chars*
zipcode | Postalcode of the Advertiser | no | *max 255 chars*
city | City of the Advertiser | no | *max 255 chars*
county | Country of the Advertiser | no | *max 255 chars*
phone | Phone number of the Advertiser | no | *max 255 chars*
email | E-mailaddress of the Advertiser| no | *valid e-mailaddress*
web | Website address of the Advertiser | no | *valid URL*

## Update an Advertiser

```shell
curl "https://leasedesk.ptchr-dev.nl/api/v1/advertiser/<ID>
    -X POST
    -H "Authorization: <your_access_token>"
    -H "Content-Type: application/json"
    -H "Accept: application/json"
    --data {
        "advertiser_id": "test_124",
        "name": "Autobedrijf Nieuw",
        "street": "Stationstraat",
        "number": "10",
        "number_extra": "a",
        "zipcode": "1234AB",
        "city": "Maastricht",
        "country": "Nederland",
        "phone": "+31 40 123 45 67",
        "email": "info@autobedrijfjassen.nl",
        "web": "http://autobedrijfjanssen.nl",
    }
```

> The above command returns JSON structured like this:

```json
{
    "data": {
        "id": 1,
        "advertiser_id": "test_124",
        "name": "Autobedrijf Nieuw",
        "street": "Stationstraat",
        "number": "10",
        "number_extra": "a",
        "zipcode": "1234AB",
        "city": "Maastricht",
        "country": "Nederland",
        "phone": "+31 40 123 45 67",
        "email": "info@autobedrijfjassen.nl",
        "web": "http://autobedrijfjanssen.nl",
        "created_at": "20-02-2018 11:26:12",
        "updated_at": "20-02-2018 11:26:12"
    }
}
```

This endpoint updates an existing Advertiser.

<aside class="warning">Make sure you send the json payload as raw body data to the endpoint.</aside>

### HTTP Request

`PUT https://leasedesk.ptchr-dev.nl/api/v1/advertiser/`

### Raw Body Parameters (JSON)

Parameter | Description | Required | Validation Rules
--------- | ----------- | -------- | ----------------
advertiser_id | The ID of the advertiser as it's in your own system | yes | *none*
name | Name of the Advertiser | yes | *none*
street | Street of the Advertiser | no | *max 255 chars*
number | Housenumber of the Advertiser | no | *max 255 chars*
number_extra | Housenumber addition | no | *max 255 chars*
zipcode | Postalcode of the Advertiser | no | *max 255 chars*
city | City of the Advertiser | no | *max 255 chars*
county | Country of the Advertiser | no | *max 255 chars*
phone | Phone number of the Advertiser | no | *max 255 chars*
email | E-mailaddress of the Advertiser| no | *valid e-mailaddress*
web | Website address of the Advertiser | no | *valid URL*

## Get All Advertisers

```shell
curl "https://leasedesk.ptchr-dev.nl/api/v1/advertiser"
  -H "Authorization: <your_access_token>"
```

> The above command returns JSON structured like this:

```json
{
    "data": [
        {
            "id": 1,
            "advertiser_id": "test_124",
            "name": "Autobedrijf Janssen",
            "street": "Stationstraat",
            "number": "10",
            "number_extra": "a",
            "zipcode": "1234AB",
            "city": "Maastricht",
            "country": "Nederland",
            "phone": "+31 40 123 45 67",
            "email": "info@autobedrijfjassen.nl",
            "web": "http://autobedrijfjanssen.nl",
            "created_at": "20-02-2018 09:47:22",
            "updated_at": "20-02-2018 09:47:22"
        },
        {
            "id": 2,
            "advertiser_id": "test_123",
            "name": "Autobedrijf Peters",
            "street": "Helmweg",
            "number": "7",
            "number_extra": "",
            "zipcode": "9876XZ",
            "city": "Hengelo",
            "country": "Nederland",
            "phone": "+31 40 987 65 43",
            "email": "info@autobedrijfpeters.nl",
            "web": "http://autobedrijfpeters.nl",
            "created_at": "20-02-2018 09:47:22",
            "updated_at": "20-02-2018 09:47:22"
        },
    ]
}
```

This endpoint retrieves all advertisers created by the currently authenticated client.

### HTTP Request

`GET https://leasedesk.ptchr-dev.nl/api/v1/advertiser`

### Query Parameters

None

<aside class="success">
Remember — don't forget to authenticate!
</aside>

## Get a Specific Advertiser

```shell
curl "https://leasedesk.ptchr-dev.nl/api/v1/advertiser/1"
  -H "Authorization: <your_access_token>"
```

> The above command returns JSON structured like this:

```json
{
    "data": {
        "id": 1,
        "advertiser_id": "test_124",
        "name": "Autobedrijf Janssen",
        "street": "Stationstraat",
        "number": "10",
        "number_extra": "a",
        "zipcode": "1234AB",
        "city": "Maastricht",
        "country": "Nederland",
        "phone": "+31 40 123 45 67",
        "email": "info@autobedrijfjassen.nl",
        "web": "http://autobedrijfjanssen.nl",
        "created_at": "20-02-2018 09:47:22",
        "updated_at": "20-02-2018 09:47:22"
    }
}
```

This endpoint retrieves a specific advertiser.

<aside class="warning">If you try to get an advertiser that wasn't added by your client a HTTP error will be returned.</aside>

### HTTP Request

`GET https://leasedesk.ptchr-dev.nl/api/v1/advertiser/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the advertiser to retrieve

## Delete a Specific Advertiser

```shell
curl "https://leasedesk.ptchr-dev.nl/api/v1/advertiser/1"
  -X DELETE
  -H "Authorization: <your_access_token>"
```

> The above command returns JSON structured like this:

```json
[]
```

This endpoint deletes a specific Advertiser.

<aside class="warning">The JSON response will be empty, when the Advertiser is deleted succesfully a HTTP 200 OK response will be returned.</aside>

### HTTP Request

`DELETE https://leasedesk.ptchr-dev.nl/api/v1/advertiser/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Advertiser to delete