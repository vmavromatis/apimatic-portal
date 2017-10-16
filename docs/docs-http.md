# 

**`API Version:`** `1.0`

APItude complete postman collection, with both BookingAPI & ContentAPI. You have the full details of our API in our developer portal:
https://developer.hotelbeds.com/docs?hotel



## Base URL

The base URL for this API is `http://example.com/hotel-api`









# <a name="api_reference"></a>API Reference

* [Post booking operations](#post_booking_operations)
* [Booking](#booking)
* [CheckRate](#check_rate)
* [Availability](#availability)
* [Misc](#misc)

## <a name="post_booking_operations"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Post booking operations") Post booking operations


### <a name="booking_list"></a>![Endpoint: ](https://apidocs.io/img/method.png "BookingList") BookingList


**`GET`** `/1.0/bookings`

> *Tags:*  ``` Skips Authentication ``` 

> BookingList




#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| start | datetime |  ``` Required ```  | TODO: Add a parameter description | `2017-08-15` | 
| end | datetime |  ``` Required ```  | TODO: Add a parameter description | `2017-09-10` | 
| filterType | string |  ``` Required ```  | TODO: Add a parameter description | `CREATION` | 
| status | string |  ``` Required ```  | TODO: Add a parameter description | `ALL` | 
| from | number |  ``` Required ```  | TODO: Add a parameter description | `1` | 
| to | number |  ``` Required ```  | TODO: Add a parameter description | `25` | 

#### Request Headers
>Accept=application/json;
>Api-key={{Api-key}};
>X-Signature={{X-Signature}};

#### Responses
**200**


### <a name="booking_cancellation"></a>![Endpoint: ](https://apidocs.io/img/method.png "BookingCancellation") BookingCancellation


**`DELETE`** `/1.0/bookings/{booking_reference}`

> *Tags:*  ``` Skips Authentication ``` 

> BookingCancellation




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| booking_reference | string |  ``` Required ```  | TODO: Add a parameter description | `"booking_reference"` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| -------------------------------- |
| cancellationFlag | string |  ``` Required ```  | TODO: Add a parameter description | `"cancellationFlag"` | 
| language | string |  ``` Required ```  | TODO: Add a parameter description | `"language"` | 

#### Request Headers
>Accept="Accept";
>Api-key="Api-key";
>X-Signature="X-Signature";

#### Responses
**200**


### <a name="booking_change"></a>![Endpoint: ](https://apidocs.io/img/method.png "BookingChange") BookingChange


**`PUT`** `/1.0/bookings/{booking_reference}`

> *Tags:*  ``` Skips Authentication ``` 

> BookingChange




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| booking_reference | string |  ``` Required ```  | TODO: Add a parameter description | `"booking_reference"` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Api-key="Api-key";
>X-Signature="X-Signature";
>Accept-Encoding="Accept-Encoding";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [BookingChangeRequest](#booking_change_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "mode": "SIMULATION",
  "booking": {
    "reference": "52-1274417",
    "clientReference": "INTEGRATIONAGENCY",
    "creationDate": "2017-08-31",
    "status": "CONFIRMED",
    "modificationPolicies": {
      "cancellation": true,
      "modification": true
    },
    "creationUser": "wuupfvswdqfz342cejxfv3ku",
    "holder": {
      "name": "INTEGRATIONTESTFIRSTNAME",
      "surname": "INTEGRATIONTESTLASTNAME"
    },
    "hotel": {
      "checkOut": "2017-09-20",
      "checkIn": "2017-09-15",
      "code": 1,
      "name": "Villa Dorada",
      "categoryCode": "3EST",
      "categoryName": "3 STARS",
      "destinationCode": "SAL",
      "destinationName": "Salou Area / Costa Dorada",
      "zoneCode": 10,
      "zoneName": "Salou",
      "latitude": "41.06865947991072",
      "longitude": "1.1524744666303377",
      "rooms": [
        {
          "status": "CONFIRMED",
          "id": 1,
          "code": "DBT.ST-3",
          "name": "Double or Twin MONOPARENTAL 1 ADULT 2 CHILDREN",
          "paxes": [
            {
              "roomId": 1,
              "type": "AD",
              "name": "First Adult Name",
              "surname": "Surname"
            },
            {
              "roomId": 1,
              "type": "CH",
              "age": 6,
              "name": "Second Child Name"
            },
            {
              "roomId": 1,
              "type": "CH",
              "age": 5,
              "name": "First Child Name"
            }
          ],
          "rates": [
            {
              "rateClass": "NOR",
              "net": "302.26",
              "rateComments": "1x Double or Twin Estimated total amount of taxes & fees for this booking: 2.50 Euro   payable on arrival  \r. Car park NO   . Key Collection 14:00 \u0013 00:00. Check-in hour 14:00 \u0013 00:00. . This rate is not applicable to Spain, Italy & Portugal market/country or passport holders otherwise the reservation will not be accepted or supplement fees can be charged on arrival.",
              "paymentType": "AT_WEB",
              "packaging": false,
              "boardCode": "RO",
              "boardName": "ROOM ONLY",
              "cancellationPolicies": [
                {
                  "amount": "141.00",
                  "from": "2017-09-14T21:59:00+00:00"
                },
                {
                  "amount": "70.50",
                  "from": "2017-09-12T21:59:00+00:00"
                }
              ],
              "rooms": 1,
              "adults": 1,
              "children": 2
            }
          ]
        }
      ],
      "totalNet": "302.26",
      "currency": "EUR",
      "supplier": {
        "name": "HOTELBEDS PRODUCT,S.L.U.",
        "vatNumber": "ESB38877676"
      }
    },
    "totalNet": 302.26,
    "pendingAmount": 302.26,
    "currency": "EUR"
  }
}
``` 

#### Responses
**200** 


 *Example Body* (**[BookingChangeResponse](#booking_change_response)**) 

```
{
  "auditData": {
    "processTime": "3089",
    "timestamp": "2017-08-31 15:44:45.703",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "23c542efb2ca3c1642f5f0d87c6c410b81c52ee3",
    "token": "46b59f25-9ea3-4824-a679-e10352d5787b",
    "internal": "null||||0|0||||||||||||0||||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "booking": {
    "reference": "258-555202",
    "clientReference": "INTEGRATIONAGENCY",
    "creationDate": "2017-08-31",
    "status": "CONFIRMED",
    "modificationPolicies": {
      "cancellation": true,
      "modification": true
    },
    "creationUser": "wuupfvswdqfz342cejxfv3ku",
    "holder": {
      "name": "INTEGRATIONTESTFIRSTNAME",
      "surname": "INTEGRATIONTESTLASTNAME"
    },
    "hotel": {
      "checkOut": "2017-11-15",
      "checkIn": "2017-11-14",
      "code": 424819,
      "name": "America Do Sul",
      "categoryCode": "3EST",
      "categoryName": "3 STARS",
      "destinationCode": "SAO",
      "destinationName": "Sao Paulo",
      "zoneCode": 1,
      "zoneName": "Sao Paulo - City",
      "latitude": "-23.540438",
      "longitude": "-46.642541",
      "rooms": [
        {
          "status": "CONFIRMED",
          "id": 1,
          "code": "DBL.ST",
          "name": "DOUBLE STANDARD",
          "paxes": [
            {
              "roomId": 1,
              "type": "AD",
              "name": "Second Adult Name"
            },
            {
              "roomId": 1,
              "type": "AD",
              "name": "First Adult Name"
            }
          ],
          "rates": [
            {
              "rateClass": "NOR",
              "net": "34.02",
              "rateComments": "Car park NO   . Check-in hour 14:00 \u0013 14:00. ",
              "paymentType": "AT_WEB",
              "packaging": false,
              "boardCode": "BB",
              "boardName": "BED AND BREAKFAST",
              "cancellationPolicies": [
                {
                  "amount": "34.02",
                  "from": "2017-11-11T02:59:00+00:00"
                }
              ],
              "rooms": 1,
              "adults": 2,
              "children": 0
            }
          ]
        }
      ],
      "totalNet": "34.02",
      "currency": "USD",
      "supplier": {
        "name": "ADVANTOS BRASIL OPERADORA DE TURISMO, LTDA",
        "vatNumber": "BR16847249000177"
      }
    },
    "totalNet": 34.02,
    "pendingAmount": 34.02,
    "currency": "USD"
  }
}
```


### <a name="booking_detail"></a>![Endpoint: ](https://apidocs.io/img/method.png "BookingDetail") BookingDetail


**`GET`** `/1.0/bookings/{booking_reference}`

> *Tags:*  ``` Skips Authentication ``` 

> BookingDetail




#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ----------------------------------- |
| booking_reference | string |  ``` Required ```  | TODO: Add a parameter description | `"booking_reference"` | 

#### Request Headers
>Accept="Accept";
>Api-key="Api-key";
>X-Signature="X-Signature";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="booking"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Booking") Booking


### <a name="booking"></a>![Endpoint: ](https://apidocs.io/img/method.png "Booking") Booking


**`POST`** `/1.2/bookings`

> *Tags:*  ``` Skips Authentication ``` 

> Booking




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Api-key={{Api-key}};
>X-Signature={{X-Signature}};
>Accept-Encoding=gzip;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [BookingRequest](#booking_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "holder": {
    "name": "IntegrationTestFirstName",
    "surname": "IntegrationTestLastName"
  },
  "rooms": [
    {
      "rateKey": "20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731",
      "paxes": [
        {
          "roomId": "1",
          "type": "AD",
          "name": "Adult Name"
        }
      ]
    }
  ],
  "clientReference": "IntegrationAgency"
}
``` 

#### Responses
**200** 


 *Example Body* (**[BookingResponse](#booking_response)**) 

```
{
  "auditData": {
    "processTime": "796",
    "timestamp": "2017-08-31 15:40:40.244",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "23c542efb2ca3c1642f5f0d87c6c410b81c52ee3",
    "token": "45f63673-32b7-493f-88af-3f2a060273fc",
    "internal": "0|AB4947E0B997444E92BDD56C969894111520|BR|05|1|3|||||||AT_WEB||||R|9|2|1~2~2~0||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "booking": {
    "reference": "258-555202",
    "clientReference": "INTEGRATIONAGENCY",
    "creationDate": "2017-08-31",
    "status": "CONFIRMED",
    "modificationPolicies": {
      "cancellation": true,
      "modification": true
    },
    "creationUser": "wuupfvswdqfz342cejxfv3ku",
    "holder": {
      "name": "INTEGRATIONTESTFIRSTNAME",
      "surname": "INTEGRATIONTESTLASTNAME"
    },
    "hotel": {
      "checkOut": "2017-11-15",
      "checkIn": "2017-11-14",
      "code": 424819,
      "name": "America Do Sul",
      "categoryCode": "3EST",
      "categoryName": "3 STARS",
      "destinationCode": "SAO",
      "destinationName": "Sao Paulo",
      "zoneCode": 1,
      "zoneName": "Sao Paulo - City",
      "latitude": "-23.540438",
      "longitude": "-46.642541",
      "rooms": [
        {
          "status": "CONFIRMED",
          "id": 1,
          "code": "DBL.ST",
          "name": "DOUBLE STANDARD",
          "paxes": [
            {
              "roomId": 1,
              "type": "AD",
              "name": "First Adult Name"
            },
            {
              "roomId": 1,
              "type": "AD",
              "name": "Second Adult Name"
            },
            {
              "roomId": 2,
              "type": "AD",
              "name": "Third Adult Name"
            },
            {
              "roomId": 2,
              "type": "AD",
              "name": "Fourth Adult Name"
            }
          ],
          "rates": [
            {
              "rateClass": "NOR",
              "net": "68.04",
              "rateComments": "Car park NO   . Check-in hour 14:00 \u0013 14:00. ",
              "paymentType": "AT_WEB",
              "packaging": false,
              "boardCode": "BB",
              "boardName": "BED AND BREAKFAST",
              "cancellationPolicies": [
                {
                  "amount": "68.04",
                  "from": "2017-11-11T02:59:00+00:00"
                }
              ],
              "rooms": 2,
              "adults": 2,
              "children": 0
            }
          ]
        }
      ],
      "totalNet": "68.04",
      "currency": "USD",
      "supplier": {
        "name": "ADVANTOS BRASIL OPERADORA DE TURISMO, LTDA",
        "vatNumber": "BR16847249000177"
      }
    },
    "totalNet": 68.04,
    "pendingAmount": 68.04,
    "currency": "USD"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="check_rate"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "CheckRate") CheckRate


### <a name="check_rate"></a>![Endpoint: ](https://apidocs.io/img/method.png "CheckRate") CheckRate


**`POST`** `/1.0/checkrates`

> *Tags:*  ``` Skips Authentication ``` 

> CheckRate




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Api-key={{Api-key}};
>X-Signature={{X-Signature}};
>Accept-Encoding=gzip;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [CheckRateRequest](#check_rate_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "rooms": [
    {
      "rateKey": "20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544"
    }
  ]
}
``` 

#### Responses
**200** 


 *Example Body* (**[CheckRateResponse](#check_rate_response)**) 

```
{
  "auditData": {
    "processTime": "31",
    "timestamp": "2017-08-30 15:50:31.772",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "4c0c21f7a3982f3ad0cf88b921c4e04e7c36861f",
    "token": "9db694ae-82c0-4f49-9c5d-307a823e961f",
    "internal": "null|85AA606B40DC4C8DA2EB70ADEF1FB4E51545|||0|1|||||||||||R|1|1|||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotel": {
    "checkOut": "2017-12-20",
    "checkIn": "2017-12-19",
    "code": 106753,
    "name": "Wingate By Wyndham Orlando International Airport",
    "categoryCode": "3EST",
    "categoryName": "3 STARS",
    "destinationCode": "MCO",
    "destinationName": "Orlando Area - Florida - FL",
    "zoneCode": 2,
    "zoneName": "Orlando International Airport",
    "latitude": "28.4626",
    "longitude": "-81.308",
    "rooms": [
      {
        "code": "DBL.2Q",
        "name": "DOUBLE TWO QUEEN BEDS",
        "rates": [
          {
            "rateKey": "20171219|20171220|W|235|106753|DBL.2Q|COM|DB||1~3~1|2|N@85AA606B40DC4C8DA2EB70ADEF1FB4E51545",
            "rateClass": "NOR",
            "rateType": "BOOKABLE",
            "net": "104.84",
            "rateComments": "The person whose name is on the reservation must be at least 21 years of age to check in.. Rollaway beds are available based upon availability for an additional fee, payable locally.. Resort fee has been waived for Hotelbeds guests..  . .  .  YES Car park NO.Car park YES FEE: NO.",
            "paymentType": "AT_WEB",
            "packaging": false,
            "boardCode": "DB",
            "boardName": "BUFFET BREAKFAST",
            "cancellationPolicies": [
              {
                "amount": "104.84",
                "from": "2017-12-16T04:59:00+00:00"
              }
            ],
            "rateBreakDown": {
              "rateDiscounts": [
                {
                  "code": "XP",
                  "name": "EXTRA PERSON",
                  "amount": "-95.64"
                }
              ]
            },
            "rooms": 1,
            "adults": 3,
            "children": 1,
            "childrenAges": "2",
            "offers": [
              {
                "code": "9008",
                "name": "Extra bed discount",
                "amount": "-95.64"
              }
            ]
          }
        ]
      }
    ],
    "totalNet": "104.84",
    "currency": "USD"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="availability"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Availability") Availability


### <a name="other_filters"></a>![Endpoint: ](https://apidocs.io/img/method.png "Other filters") Other filters


**`POST`** `/1.0/hotels`

> *Tags:*  ``` Skips Authentication ``` 

> Other filters




#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Api-key={{Api-key}};
>X-Signature={{X-Signature}};
>Accept-Encoding=gzip;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| [Other filtersRequest](#other_filters_request) |  ``` Required ```  | TODO: Add description | 

 *Example Body* 
``` 
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "filter": {
    "minRate": 100.0,
    "maxRate": 1700.0,
    "minCategory": 3,
    "maxCategory": 5,
    "maxRooms": 3,
    "maxRatesPerRoom": 3,
    "paymentType": "AT_HOTEL",
    "packaging": true,
    "hotelPackage": "YES",
    "contract": "CG-FIT B2B"
  }
}
``` 

#### Responses
**200** 


 *Example Body* (**[Other filtersResponse](#other_filters_response)**) 

```
{
  "auditData": {
    "processTime": "94",
    "timestamp": "2017-09-08 12:47:16.646",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "23c542efb2ca3c1642f5f0d87c6c410b81c52ee3",
    "token": "9536f01d-d2b6-40bf-ac8b-b7b8567b28cf",
    "internal": "0||BR|01|1|2||||||||||||1||1~1~1~0||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotels": {
    "hotels": [
      {
        "code": 186629,
        "name": "K+K Hotel Picasso",
        "categoryCode": "4EST",
        "categoryName": "4 STARS",
        "destinationCode": "BCN",
        "destinationName": "Barcelona",
        "zoneCode": 8,
        "zoneName": "El Born",
        "latitude": "41.386763",
        "longitude": "2.183858",
        "rooms": [
          {
            "code": "DBL.AS",
            "name": "DOUBLE CLASSIC",
            "rates": [
              {
                "paymentType": "AT_WEB",
                "boardCode": "BB",
                "boardName": "BED AND BREAKFAST",
                "rooms": 1,
                "adults": 1,
                "children": 0,
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|102|186629|DBL.AS|CG-FIT B2B|BB||1~1~0||N@6A20D3E64C4445CAB51E27C08DBEF84B1247",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "1162.65",
                    "allotment": 1,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|102|186629|DBL.AS|CG-FIT B2B|BB||1~1~0||N@6A20D3E64C4445CAB51E27C08DBEF84B1247",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "1162.65",
                    "allotment": 1,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  }
                ]
              }
            ]
          }
        ],
        "minRate": "1162.65",
        "maxRate": "1162.65",
        "currency": "EUR"
      }
    ],
    "checkIn": "2017-09-15",
    "total": 1,
    "checkOut": "2017-09-20"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="misc"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Misc") Misc


### <a name="0._status"></a>![Endpoint: ](https://apidocs.io/img/method.png "0. Status") 0. Status


**`GET`** `/1.0/status`

> *Tags:*  ``` Skips Authentication ``` 

> 0. Status




#### Request Headers
>Accept=application/json;
>Api-key={{Api-key}};
>X-Signature={{X-Signature}};

#### Responses
**200**


[Back to API Reference](#api_reference)

# <a name="models"></a> Models

### List of Models

* [BookingChangeResponse](#booking_change_response)
* [Hotel108](#hotel108)
* [Booking105](#booking105)
* [BookingChangeRequest](#booking_change_request)
* [Rate101](#rate101)
* [Hotel98](#hotel98)
* [Booking](#booking)
* [BookingResponse](#booking_response)
* [Rate84](#rate84)
* [Hotel](#hotel)
* [CheckRateResponse](#check_rate_response)
* [Hotels74](#hotels74)
* [Filter](#filter)
* [Rate63](#rate63)
* [Hotels61](#hotels61)
* [Hotels30](#hotels30)
* [Availability by geolocationResponse](#availability_by_geolocation_response)
* [Hotels19](#hotels19)
* [Availability by destinationResponse](#availability_by_destination_response)
* [Rate](#rate)
* [Supplier](#supplier)
* [Paxis100](#paxis100)
* [ModificationPolicies](#modification_policies)
* [Paxis](#paxis)
* [Rooms91](#rooms91)
* [Holder](#holder)
* [RateDiscount](#rate_discount)
* [Hotels7](#hotels7)
* [Rooms83](#rooms83)
* [CheckRateRequest](#check_rate_request)
* [Rooms75](#rooms75)
* [Rooms62](#rooms62)
* [Boards](#boards)
* [Rooms](#rooms)
* [Room31](#room31)
* [Room20](#room20)
* [Stay13](#stay13)
* [Offer](#offer)
* [CancellationPolicy](#cancellation_policy)
* [Room](#room)
* [Occupancy](#occupancy)
* [Stay](#stay)
* [Availability by hotel codeRequest](#availability_by_hotel_code_request)
* [RateBreakDown](#rate_break_down)
* [Rooms79](#rooms79)
* [Keywords](#keywords)
* [Destination](#destination)
* [Hotels](#hotels)
* [Filter by accommodation typeRequest](#filter_by_accommodation_type_request)
* [Filter by keywordRequest](#filter_by_keyword_request)
* [Filter by room typeRequest](#filter_by_room_type_request)
* [Rate32](#rate32)
* [Hotels29](#hotels29)
* [Geolocation](#geolocation)
* [Availability by geolocationRequest](#availability_by_geolocation_request)
* [ShiftRate](#shift_rate)
* [Rate21](#rate21)
* [Hotels18](#hotels18)
* [Availability by destinationRequest](#availability_by_destination_request)
* [Hotels6](#hotels6)
* [AuditData](#audit_data)
* [Availability by hotel codeResponse](#availability_by_hotel_code_response)
* [Review](#review)
* [Filter by review ratingRequest](#filter_by_review_rating_request)
* [Filter by board codeRequest](#filter_by_board_code_request)
* [Paxis110](#paxis110)
* [Rooms109](#rooms109)
* [Rooms99](#rooms99)
* [BookingRequest](#booking_request)
* [Hotels73](#hotels73)
* [Other filtersResponse](#other_filters_response)
* [Other filtersRequest](#other_filters_request)
* [Hotels60](#hotels60)
* [Filter by review ratingResponse](#filter_by_review_rating_response)
## <a name="booking_change_response"></a>![Type: ](https://apidocs.io/img/method.png "BookingChangeResponse") BookingChangeResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| booking | [Booking](#booking) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "3089",
    "timestamp": "2017-08-31 15:44:45.703",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "23c542efb2ca3c1642f5f0d87c6c410b81c52ee3",
    "token": "46b59f25-9ea3-4824-a679-e10352d5787b",
    "internal": "null||||0|0||||||||||||0||||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "booking": {
    "reference": "258-555202",
    "clientReference": "INTEGRATIONAGENCY",
    "creationDate": "2017-08-31",
    "status": "CONFIRMED",
    "modificationPolicies": {
      "cancellation": true,
      "modification": true
    },
    "creationUser": "wuupfvswdqfz342cejxfv3ku",
    "holder": {
      "name": "INTEGRATIONTESTFIRSTNAME",
      "surname": "INTEGRATIONTESTLASTNAME"
    },
    "hotel": {
      "checkOut": "2017-11-15",
      "checkIn": "2017-11-14",
      "code": 424819,
      "name": "America Do Sul",
      "categoryCode": "3EST",
      "categoryName": "3 STARS",
      "destinationCode": "SAO",
      "destinationName": "Sao Paulo",
      "zoneCode": 1,
      "zoneName": "Sao Paulo - City",
      "latitude": "-23.540438",
      "longitude": "-46.642541",
      "rooms": [
        {
          "status": "CONFIRMED",
          "id": 1,
          "code": "DBL.ST",
          "name": "DOUBLE STANDARD",
          "paxes": [
            {
              "roomId": 1,
              "type": "AD",
              "name": "Second Adult Name"
            },
            {
              "roomId": 1,
              "type": "AD",
              "name": "First Adult Name"
            }
          ],
          "rates": [
            {
              "rateClass": "NOR",
              "net": "34.02",
              "rateComments": "Car park NO   . Check-in hour 14:00 \u0013 14:00. ",
              "paymentType": "AT_WEB",
              "packaging": false,
              "boardCode": "BB",
              "boardName": "BED AND BREAKFAST",
              "cancellationPolicies": [
                {
                  "amount": "34.02",
                  "from": "2017-11-11T02:59:00+00:00"
                }
              ],
              "rooms": 1,
              "adults": 2,
              "children": 0
            }
          ]
        }
      ],
      "totalNet": "34.02",
      "currency": "USD",
      "supplier": {
        "name": "ADVANTOS BRASIL OPERADORA DE TURISMO, LTDA",
        "vatNumber": "BR16847249000177"
      }
    },
    "totalNet": 34.02,
    "pendingAmount": 34.02,
    "currency": "USD"
  }
}
```



## <a name="hotel108"></a>![Type: ](https://apidocs.io/img/method.png "Hotel108") Hotel108



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms109](#rooms109) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| totalNet | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 
| supplier | [Supplier](#supplier) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "checkOut": "checkOut",
  "checkIn": "checkIn",
  "code": 165,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 165,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "status": "status",
      "id": 165,
      "code": "code",
      "name": "name",
      "paxes": [
        {
          "roomId": 165,
          "type": "type",
          "name": "name",
          "surname": "surname",
          "age": 165
        }
      ],
      "rates": [
        {
          "rateClass": "rateClass",
          "net": "net",
          "rateComments": "rateComments",
          "paymentType": "paymentType",
          "packaging": true,
          "boardCode": "boardCode",
          "boardName": "boardName",
          "cancellationPolicies": [
            {
              "amount": "amount",
              "from": "from"
            }
          ],
          "rooms": 165,
          "adults": 165,
          "children": 165
        }
      ]
    }
  ],
  "totalNet": "totalNet",
  "currency": "currency",
  "supplier": {
    "name": "name",
    "vatNumber": "vatNumber"
  }
}
```



## <a name="booking105"></a>![Type: ](https://apidocs.io/img/method.png "Booking105") Booking105



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| reference | string |  ``` Required ```  | TODO: Add a property description | 
| clientReference | string |  ``` Required ```  | TODO: Add a property description | 
| creationDate | string |  ``` Required ```  | TODO: Add a property description | 
| status | string |  ``` Required ```  | TODO: Add a property description | 
| modificationPolicies | [ModificationPolicies](#modification_policies) |  ``` Required ```  | TODO: Add a property description | 
| creationUser | string |  ``` Required ```  | TODO: Add a property description | 
| holder | [Holder](#holder) |  ``` Required ```  | TODO: Add a property description | 
| hotel | [Hotel108](#hotel108) |  ``` Required ```  | TODO: Add a property description | 
| totalNet | precision |  ``` Required ```  | TODO: Add a property description | 
| pendingAmount | precision |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "reference": "reference",
  "clientReference": "clientReference",
  "creationDate": "creationDate",
  "status": "status",
  "modificationPolicies": {
    "cancellation": true,
    "modification": true
  },
  "creationUser": "creationUser",
  "holder": {
    "name": "name",
    "surname": "surname"
  },
  "hotel": {
    "checkOut": "checkOut",
    "checkIn": "checkIn",
    "code": 165,
    "name": "name",
    "categoryCode": "categoryCode",
    "categoryName": "categoryName",
    "destinationCode": "destinationCode",
    "destinationName": "destinationName",
    "zoneCode": 165,
    "zoneName": "zoneName",
    "latitude": "latitude",
    "longitude": "longitude",
    "rooms": [
      {
        "status": "status",
        "id": 165,
        "code": "code",
        "name": "name",
        "paxes": [
          {
            "roomId": 165,
            "type": "type",
            "name": "name",
            "surname": "surname",
            "age": 165
          }
        ],
        "rates": [
          {
            "rateClass": "rateClass",
            "net": "net",
            "rateComments": "rateComments",
            "paymentType": "paymentType",
            "packaging": true,
            "boardCode": "boardCode",
            "boardName": "boardName",
            "cancellationPolicies": [
              {
                "amount": "amount",
                "from": "from"
              }
            ],
            "rooms": 165,
            "adults": 165,
            "children": 165
          }
        ]
      }
    ],
    "totalNet": "totalNet",
    "currency": "currency",
    "supplier": {
      "name": "name",
      "vatNumber": "vatNumber"
    }
  },
  "totalNet": 165.934083431928,
  "pendingAmount": 165.934083431928,
  "currency": "currency"
}
```



## <a name="booking_change_request"></a>![Type: ](https://apidocs.io/img/method.png "BookingChangeRequest") BookingChangeRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| mode | string |  ``` Required ```  | TODO: Add a property description | 
| booking | [Booking105](#booking105) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "mode": "SIMULATION",
  "booking": {
    "reference": "52-1274417",
    "clientReference": "INTEGRATIONAGENCY",
    "creationDate": "2017-08-31",
    "status": "CONFIRMED",
    "modificationPolicies": {
      "cancellation": true,
      "modification": true
    },
    "creationUser": "wuupfvswdqfz342cejxfv3ku",
    "holder": {
      "name": "INTEGRATIONTESTFIRSTNAME",
      "surname": "INTEGRATIONTESTLASTNAME"
    },
    "hotel": {
      "checkOut": "2017-09-20",
      "checkIn": "2017-09-15",
      "code": 1,
      "name": "Villa Dorada",
      "categoryCode": "3EST",
      "categoryName": "3 STARS",
      "destinationCode": "SAL",
      "destinationName": "Salou Area / Costa Dorada",
      "zoneCode": 10,
      "zoneName": "Salou",
      "latitude": "41.06865947991072",
      "longitude": "1.1524744666303377",
      "rooms": [
        {
          "status": "CONFIRMED",
          "id": 1,
          "code": "DBT.ST-3",
          "name": "Double or Twin MONOPARENTAL 1 ADULT 2 CHILDREN",
          "paxes": [
            {
              "roomId": 1,
              "type": "AD",
              "name": "First Adult Name",
              "surname": "Surname"
            },
            {
              "roomId": 1,
              "type": "CH",
              "age": 6,
              "name": "Second Child Name"
            },
            {
              "roomId": 1,
              "type": "CH",
              "age": 5,
              "name": "First Child Name"
            }
          ],
          "rates": [
            {
              "rateClass": "NOR",
              "net": "302.26",
              "rateComments": "1x Double or Twin Estimated total amount of taxes & fees for this booking: 2.50 Euro   payable on arrival  \r. Car park NO   . Key Collection 14:00 \u0013 00:00. Check-in hour 14:00 \u0013 00:00. . This rate is not applicable to Spain, Italy & Portugal market/country or passport holders otherwise the reservation will not be accepted or supplement fees can be charged on arrival.",
              "paymentType": "AT_WEB",
              "packaging": false,
              "boardCode": "RO",
              "boardName": "ROOM ONLY",
              "cancellationPolicies": [
                {
                  "amount": "141.00",
                  "from": "2017-09-14T21:59:00+00:00"
                },
                {
                  "amount": "70.50",
                  "from": "2017-09-12T21:59:00+00:00"
                }
              ],
              "rooms": 1,
              "adults": 1,
              "children": 2
            }
          ]
        }
      ],
      "totalNet": "302.26",
      "currency": "EUR",
      "supplier": {
        "name": "HOTELBEDS PRODUCT,S.L.U.",
        "vatNumber": "ESB38877676"
      }
    },
    "totalNet": 302.26,
    "pendingAmount": 302.26,
    "currency": "EUR"
  }
}
```



## <a name="rate101"></a>![Type: ](https://apidocs.io/img/method.png "Rate101") Rate101



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateClass | string |  ``` Required ```  | TODO: Add a property description | 
| net | string |  ``` Required ```  | TODO: Add a property description | 
| rateComments | string |  ``` Required ```  | TODO: Add a property description | 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| packaging | boolean |  ``` Required ```  | TODO: Add a property description | 
| boardCode | string |  ``` Required ```  | TODO: Add a property description | 
| boardName | string |  ``` Required ```  | TODO: Add a property description | 
| cancellationPolicies | [CancellationPolicy](#cancellation_policy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "rateClass": "rateClass",
  "net": "net",
  "rateComments": "rateComments",
  "paymentType": "paymentType",
  "packaging": true,
  "boardCode": "boardCode",
  "boardName": "boardName",
  "cancellationPolicies": [
    {
      "amount": "amount",
      "from": "from"
    }
  ],
  "rooms": 165,
  "adults": 165,
  "children": 165
}
```



## <a name="hotel98"></a>![Type: ](https://apidocs.io/img/method.png "Hotel98") Hotel98



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms99](#rooms99) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| totalNet | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 
| supplier | [Supplier](#supplier) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "checkOut": "checkOut",
  "checkIn": "checkIn",
  "code": 165,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 165,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "status": "status",
      "id": 165,
      "code": "code",
      "name": "name",
      "paxes": [
        {
          "roomId": 165,
          "type": "type",
          "name": "name"
        }
      ],
      "rates": [
        {
          "rateClass": "rateClass",
          "net": "net",
          "rateComments": "rateComments",
          "paymentType": "paymentType",
          "packaging": true,
          "boardCode": "boardCode",
          "boardName": "boardName",
          "cancellationPolicies": [
            {
              "amount": "amount",
              "from": "from"
            }
          ],
          "rooms": 165,
          "adults": 165,
          "children": 165
        }
      ]
    }
  ],
  "totalNet": "totalNet",
  "currency": "currency",
  "supplier": {
    "name": "name",
    "vatNumber": "vatNumber"
  }
}
```



## <a name="booking"></a>![Type: ](https://apidocs.io/img/method.png "Booking") Booking



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| reference | string |  ``` Required ```  | TODO: Add a property description | 
| clientReference | string |  ``` Required ```  | TODO: Add a property description | 
| creationDate | string |  ``` Required ```  | TODO: Add a property description | 
| status | string |  ``` Required ```  | TODO: Add a property description | 
| modificationPolicies | [ModificationPolicies](#modification_policies) |  ``` Required ```  | TODO: Add a property description | 
| creationUser | string |  ``` Required ```  | TODO: Add a property description | 
| holder | [Holder](#holder) |  ``` Required ```  | TODO: Add a property description | 
| hotel | [Hotel98](#hotel98) |  ``` Required ```  | TODO: Add a property description | 
| totalNet | precision |  ``` Required ```  | TODO: Add a property description | 
| pendingAmount | precision |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "reference": "reference",
  "clientReference": "clientReference",
  "creationDate": "creationDate",
  "status": "status",
  "modificationPolicies": {
    "cancellation": true,
    "modification": true
  },
  "creationUser": "creationUser",
  "holder": {
    "name": "name",
    "surname": "surname"
  },
  "hotel": {
    "checkOut": "checkOut",
    "checkIn": "checkIn",
    "code": 165,
    "name": "name",
    "categoryCode": "categoryCode",
    "categoryName": "categoryName",
    "destinationCode": "destinationCode",
    "destinationName": "destinationName",
    "zoneCode": 165,
    "zoneName": "zoneName",
    "latitude": "latitude",
    "longitude": "longitude",
    "rooms": [
      {
        "status": "status",
        "id": 165,
        "code": "code",
        "name": "name",
        "paxes": [
          {
            "roomId": 165,
            "type": "type",
            "name": "name"
          }
        ],
        "rates": [
          {
            "rateClass": "rateClass",
            "net": "net",
            "rateComments": "rateComments",
            "paymentType": "paymentType",
            "packaging": true,
            "boardCode": "boardCode",
            "boardName": "boardName",
            "cancellationPolicies": [
              {
                "amount": "amount",
                "from": "from"
              }
            ],
            "rooms": 124,
            "adults": 124,
            "children": 124
          }
        ]
      }
    ],
    "totalNet": "totalNet",
    "currency": "currency",
    "supplier": {
      "name": "name",
      "vatNumber": "vatNumber"
    }
  },
  "totalNet": 124.210910205362,
  "pendingAmount": 124.210910205362,
  "currency": "currency"
}
```



## <a name="booking_response"></a>![Type: ](https://apidocs.io/img/method.png "BookingResponse") BookingResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| booking | [Booking](#booking) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "796",
    "timestamp": "2017-08-31 15:40:40.244",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "23c542efb2ca3c1642f5f0d87c6c410b81c52ee3",
    "token": "45f63673-32b7-493f-88af-3f2a060273fc",
    "internal": "0|AB4947E0B997444E92BDD56C969894111520|BR|05|1|3|||||||AT_WEB||||R|9|2|1~2~2~0||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "booking": {
    "reference": "258-555202",
    "clientReference": "INTEGRATIONAGENCY",
    "creationDate": "2017-08-31",
    "status": "CONFIRMED",
    "modificationPolicies": {
      "cancellation": true,
      "modification": true
    },
    "creationUser": "wuupfvswdqfz342cejxfv3ku",
    "holder": {
      "name": "INTEGRATIONTESTFIRSTNAME",
      "surname": "INTEGRATIONTESTLASTNAME"
    },
    "hotel": {
      "checkOut": "2017-11-15",
      "checkIn": "2017-11-14",
      "code": 424819,
      "name": "America Do Sul",
      "categoryCode": "3EST",
      "categoryName": "3 STARS",
      "destinationCode": "SAO",
      "destinationName": "Sao Paulo",
      "zoneCode": 1,
      "zoneName": "Sao Paulo - City",
      "latitude": "-23.540438",
      "longitude": "-46.642541",
      "rooms": [
        {
          "status": "CONFIRMED",
          "id": 1,
          "code": "DBL.ST",
          "name": "DOUBLE STANDARD",
          "paxes": [
            {
              "roomId": 1,
              "type": "AD",
              "name": "First Adult Name"
            },
            {
              "roomId": 1,
              "type": "AD",
              "name": "Second Adult Name"
            },
            {
              "roomId": 2,
              "type": "AD",
              "name": "Third Adult Name"
            },
            {
              "roomId": 2,
              "type": "AD",
              "name": "Fourth Adult Name"
            }
          ],
          "rates": [
            {
              "rateClass": "NOR",
              "net": "68.04",
              "rateComments": "Car park NO   . Check-in hour 14:00 \u0013 14:00. ",
              "paymentType": "AT_WEB",
              "packaging": false,
              "boardCode": "BB",
              "boardName": "BED AND BREAKFAST",
              "cancellationPolicies": [
                {
                  "amount": "68.04",
                  "from": "2017-11-11T02:59:00+00:00"
                }
              ],
              "rooms": 2,
              "adults": 2,
              "children": 0
            }
          ]
        }
      ],
      "totalNet": "68.04",
      "currency": "USD",
      "supplier": {
        "name": "ADVANTOS BRASIL OPERADORA DE TURISMO, LTDA",
        "vatNumber": "BR16847249000177"
      }
    },
    "totalNet": 68.04,
    "pendingAmount": 68.04,
    "currency": "USD"
  }
}
```



## <a name="rate84"></a>![Type: ](https://apidocs.io/img/method.png "Rate84") Rate84



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateKey | string |  ``` Required ```  | TODO: Add a property description | 
| rateClass | string |  ``` Required ```  | TODO: Add a property description | 
| rateType | string |  ``` Required ```  | TODO: Add a property description | 
| net | string |  ``` Required ```  | TODO: Add a property description | 
| rateComments | string |  ``` Required ```  | TODO: Add a property description | 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| packaging | boolean |  ``` Required ```  | TODO: Add a property description | 
| boardCode | string |  ``` Required ```  | TODO: Add a property description | 
| boardName | string |  ``` Required ```  | TODO: Add a property description | 
| cancellationPolicies | [CancellationPolicy](#cancellation_policy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| rateBreakDown | [RateBreakDown](#rate_break_down) |  ``` Required ```  | TODO: Add a property description | 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 
| childrenAges | string |  ``` Required ```  | TODO: Add a property description | 
| offers | [Offer](#offer) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "rateKey": "rateKey",
  "rateClass": "rateClass",
  "rateType": "rateType",
  "net": "net",
  "rateComments": "rateComments",
  "paymentType": "paymentType",
  "packaging": false,
  "boardCode": "boardCode",
  "boardName": "boardName",
  "cancellationPolicies": [
    {
      "amount": "amount",
      "from": "from"
    }
  ],
  "rateBreakDown": {
    "rateDiscounts": [
      {
        "code": "code",
        "name": "name",
        "amount": "amount"
      }
    ]
  },
  "rooms": 124,
  "adults": 124,
  "children": 124,
  "childrenAges": "childrenAges",
  "offers": [
    {
      "code": "code",
      "name": "name",
      "amount": "amount"
    }
  ]
}
```



## <a name="hotel"></a>![Type: ](https://apidocs.io/img/method.png "Hotel") Hotel



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms83](#rooms83) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| totalNet | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "checkOut": "checkOut",
  "checkIn": "checkIn",
  "code": 124,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 124,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "code": "code",
      "name": "name",
      "rates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "rateComments": "rateComments",
          "paymentType": "paymentType",
          "packaging": false,
          "boardCode": "boardCode",
          "boardName": "boardName",
          "cancellationPolicies": [
            {
              "amount": "amount",
              "from": "from"
            }
          ],
          "rateBreakDown": {
            "rateDiscounts": [
              {
                "code": "code",
                "name": "name",
                "amount": "amount"
              }
            ]
          },
          "rooms": 124,
          "adults": 124,
          "children": 124,
          "childrenAges": "childrenAges",
          "offers": [
            {
              "code": "code",
              "name": "name",
              "amount": "amount"
            }
          ]
        }
      ]
    }
  ],
  "totalNet": "totalNet",
  "currency": "currency"
}
```



## <a name="check_rate_response"></a>![Type: ](https://apidocs.io/img/method.png "CheckRateResponse") CheckRateResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| hotel | [Hotel](#hotel) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "31",
    "timestamp": "2017-08-30 15:50:31.772",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "4c0c21f7a3982f3ad0cf88b921c4e04e7c36861f",
    "token": "9db694ae-82c0-4f49-9c5d-307a823e961f",
    "internal": "null|85AA606B40DC4C8DA2EB70ADEF1FB4E51545|||0|1|||||||||||R|1|1|||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotel": {
    "checkOut": "2017-12-20",
    "checkIn": "2017-12-19",
    "code": 106753,
    "name": "Wingate By Wyndham Orlando International Airport",
    "categoryCode": "3EST",
    "categoryName": "3 STARS",
    "destinationCode": "MCO",
    "destinationName": "Orlando Area - Florida - FL",
    "zoneCode": 2,
    "zoneName": "Orlando International Airport",
    "latitude": "28.4626",
    "longitude": "-81.308",
    "rooms": [
      {
        "code": "DBL.2Q",
        "name": "DOUBLE TWO QUEEN BEDS",
        "rates": [
          {
            "rateKey": "20171219|20171220|W|235|106753|DBL.2Q|COM|DB||1~3~1|2|N@85AA606B40DC4C8DA2EB70ADEF1FB4E51545",
            "rateClass": "NOR",
            "rateType": "BOOKABLE",
            "net": "104.84",
            "rateComments": "The person whose name is on the reservation must be at least 21 years of age to check in.. Rollaway beds are available based upon availability for an additional fee, payable locally.. Resort fee has been waived for Hotelbeds guests..  . .  .  YES Car park NO.Car park YES FEE: NO.",
            "paymentType": "AT_WEB",
            "packaging": false,
            "boardCode": "DB",
            "boardName": "BUFFET BREAKFAST",
            "cancellationPolicies": [
              {
                "amount": "104.84",
                "from": "2017-12-16T04:59:00+00:00"
              }
            ],
            "rateBreakDown": {
              "rateDiscounts": [
                {
                  "code": "XP",
                  "name": "EXTRA PERSON",
                  "amount": "-95.64"
                }
              ]
            },
            "rooms": 1,
            "adults": 3,
            "children": 1,
            "childrenAges": "2",
            "offers": [
              {
                "code": "9008",
                "name": "Extra bed discount",
                "amount": "-95.64"
              }
            ]
          }
        ]
      }
    ],
    "totalNet": "104.84",
    "currency": "USD"
  }
}
```



## <a name="hotels74"></a>![Type: ](https://apidocs.io/img/method.png "Hotels74") Hotels74



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms75](#rooms75) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| minRate | string |  ``` Required ```  | TODO: Add a property description | 
| maxRate | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": 124,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 124,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "code": "code",
      "name": "name",
      "rates": [
        {
          "paymentType": "paymentType",
          "boardCode": "boardCode",
          "boardName": "boardName",
          "rooms": 124,
          "adults": 124,
          "children": 124,
          "shiftRates": [
            {
              "rateKey": "rateKey",
              "rateClass": "rateClass",
              "rateType": "rateType",
              "net": "net",
              "allotment": 124,
              "checkIn": "checkIn",
              "checkOut": "checkOut"
            }
          ]
        }
      ]
    }
  ],
  "minRate": "minRate",
  "maxRate": "maxRate",
  "currency": "currency"
}
```



## <a name="filter"></a>![Type: ](https://apidocs.io/img/method.png "Filter") Filter



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| minRate | precision |  ``` Required ```  | TODO: Add a property description | 
| maxRate | precision |  ``` Required ```  | TODO: Add a property description | 
| minCategory | number |  ``` Required ```  | TODO: Add a property description | 
| maxCategory | number |  ``` Required ```  | TODO: Add a property description | 
| maxRooms | number |  ``` Required ```  | TODO: Add a property description | 
| maxRatesPerRoom | number |  ``` Required ```  | TODO: Add a property description | 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| packaging | boolean |  ``` Required ```  | TODO: Add a property description | 
| hotelPackage | string |  ``` Required ```  | TODO: Add a property description | 
| contract | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "minRate": 124.210910205362,
  "maxRate": 124.210910205362,
  "minCategory": 124,
  "maxCategory": 124,
  "maxRooms": 124,
  "maxRatesPerRoom": 124,
  "paymentType": "paymentType",
  "packaging": false,
  "hotelPackage": "hotelPackage",
  "contract": "contract"
}
```



## <a name="rate63"></a>![Type: ](https://apidocs.io/img/method.png "Rate63") Rate63



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateKey | string |  ``` Required ```  | TODO: Add a property description | 
| rateClass | string |  ``` Required ```  | TODO: Add a property description | 
| rateType | string |  ``` Required ```  | TODO: Add a property description | 
| net | string |  ``` Required ```  | TODO: Add a property description | 
| allotment | number |  ``` Required ```  | TODO: Add a property description | 
| rateCommentsId | string |  ``` Required ```  | TODO: Add a property description | 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| packaging | boolean |  ``` Required ```  | TODO: Add a property description | 
| boardCode | string |  ``` Required ```  | TODO: Add a property description | 
| boardName | string |  ``` Required ```  | TODO: Add a property description | 
| cancellationPolicies | [CancellationPolicy](#cancellation_policy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 
| childrenAges | string |  ``` Required ```  | TODO: Add a property description | 
| shiftRates | [ShiftRate](#shift_rate) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "rateKey": "rateKey",
  "rateClass": "rateClass",
  "rateType": "rateType",
  "net": "net",
  "allotment": 124,
  "rateCommentsId": "rateCommentsId",
  "paymentType": "paymentType",
  "packaging": false,
  "boardCode": "boardCode",
  "boardName": "boardName",
  "cancellationPolicies": [
    {
      "amount": "amount",
      "from": "from"
    }
  ],
  "rooms": 124,
  "adults": 124,
  "children": 124,
  "childrenAges": "childrenAges",
  "shiftRates": [
    {
      "rateKey": "rateKey",
      "rateClass": "rateClass",
      "rateType": "rateType",
      "net": "net",
      "allotment": 124,
      "checkIn": "checkIn",
      "checkOut": "checkOut"
    }
  ]
}
```



## <a name="hotels61"></a>![Type: ](https://apidocs.io/img/method.png "Hotels61") Hotels61



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms62](#rooms62) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| minRate | string |  ``` Required ```  | TODO: Add a property description | 
| maxRate | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": 124,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 124,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "code": "code",
      "name": "name",
      "rates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "allotment": 124,
          "rateCommentsId": "rateCommentsId",
          "paymentType": "paymentType",
          "packaging": false,
          "boardCode": "boardCode",
          "boardName": "boardName",
          "cancellationPolicies": [
            {
              "amount": "amount",
              "from": "from"
            }
          ],
          "rooms": 124,
          "adults": 124,
          "children": 124,
          "childrenAges": "childrenAges",
          "shiftRates": [
            {
              "rateKey": "rateKey",
              "rateClass": "rateClass",
              "rateType": "rateType",
              "net": "net",
              "allotment": 124,
              "checkIn": "checkIn",
              "checkOut": "checkOut"
            }
          ]
        }
      ]
    }
  ],
  "minRate": "minRate",
  "maxRate": "maxRate",
  "currency": "currency"
}
```



## <a name="hotels30"></a>![Type: ](https://apidocs.io/img/method.png "Hotels30") Hotels30



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Room31](#room31) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| minRate | string |  ``` Required ```  | TODO: Add a property description | 
| maxRate | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": 124,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 124,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "code": "code",
      "name": "name",
      "rates": [
        {
          "paymentType": "paymentType",
          "boardCode": "boardCode",
          "boardName": "boardName",
          "rooms": 124,
          "adults": 124,
          "children": 124,
          "shiftRates": [
            {
              "rateKey": "rateKey",
              "rateClass": "rateClass",
              "rateType": "rateType",
              "net": "net",
              "allotment": 124,
              "checkIn": "checkIn",
              "checkOut": "checkOut"
            }
          ]
        }
      ]
    }
  ],
  "minRate": "minRate",
  "maxRate": "maxRate",
  "currency": "currency"
}
```



## <a name="availability_by_geolocation_response"></a>![Type: ](https://apidocs.io/img/method.png "Availability by geolocationResponse") Availability by geolocationResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| hotels | [Hotels29](#hotels29) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "39",
    "timestamp": "2017-08-30 10:49:48.506",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "4c0c21f7a3982f3ad0cf88b921c4e04e7c36861f",
    "token": "b72133e7-533c-4b06-b2cf-4ccc2af4695d",
    "internal": "0||BR|11|1|3||||||||||||1||1~1~4~0||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotels": {
    "hotels": [
      {
        "code": 3562,
        "name": "Silken Monumental Naranco",
        "categoryCode": "4EST",
        "categoryName": "4 STARS",
        "destinationCode": "OVD",
        "destinationName": "Asturias",
        "zoneCode": 10,
        "zoneName": "Oviedo",
        "latitude": "43.364624",
        "longitude": "-5.863767",
        "rooms": [
          {
            "code": "FAM.C4",
            "name": "FAMILY ROOM CAPACITY 4",
            "rates": [
              {
                "paymentType": "AT_WEB",
                "boardCode": "RO",
                "boardName": "ROOM ONLY",
                "rooms": 1,
                "adults": 4,
                "children": 0,
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|102|3562|FAM.C4|CG-BARFAMILIAR|RO||1~4~0||N@93C5F027D9C04F3AB6392149BFF8ED211049",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "525.42",
                    "allotment": 1,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  }
                ]
              },
              {
                "paymentType": "AT_WEB",
                "boardCode": "BB",
                "boardName": "BED AND BREAKFAST",
                "rooms": 1,
                "adults": 4,
                "children": 0,
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|102|3562|FAM.C4|CG-BARHDFAMILIA|BB||1~4~0||N@93C5F027D9C04F3AB6392149BFF8ED211049",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "693.57",
                    "allotment": 1,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  }
                ]
              },
              {
                "paymentType": "AT_WEB",
                "boardCode": "DB",
                "boardName": "BUFFET BREAKFAST",
                "rooms": 1,
                "adults": 4,
                "children": 0,
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|102|3562|FAM.C4|CG-BARFAMILIAR|DB||1~4~0||N@93C5F027D9C04F3AB6392149BFF8ED211049",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "735.62",
                    "allotment": 1,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  }
                ]
              }
            ]
          }
        ],
        "minRate": "525.42",
        "maxRate": "735.62",
        "currency": "EUR"
      }
    ],
    "checkIn": "2017-09-15",
    "total": 1,
    "checkOut": "2017-09-20"
  }
}
```



## <a name="hotels19"></a>![Type: ](https://apidocs.io/img/method.png "Hotels19") Hotels19



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Room20](#room20) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| minRate | string |  ``` Required ```  | TODO: Add a property description | 
| maxRate | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": 124,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 124,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "code": "code",
      "name": "name",
      "rates": [
        {
          "paymentType": "paymentType",
          "boardCode": "boardCode",
          "boardName": "boardName",
          "rooms": 124,
          "adults": 124,
          "children": 124,
          "childrenAges": "childrenAges",
          "shiftRates": [
            {
              "rateKey": "rateKey",
              "rateClass": "rateClass",
              "rateType": "rateType",
              "net": "net",
              "allotment": 124,
              "checkIn": "checkIn",
              "checkOut": "checkOut"
            }
          ]
        }
      ]
    }
  ],
  "minRate": "minRate",
  "maxRate": "maxRate",
  "currency": "currency"
}
```



## <a name="availability_by_destination_response"></a>![Type: ](https://apidocs.io/img/method.png "Availability by destinationResponse") Availability by destinationResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| hotels | [Hotels18](#hotels18) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "1923",
    "timestamp": "2017-08-30 11:41:49.175",
    "requestHost": "52.49.114.253",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "4c0c21f7a3982f3ad0cf88b921c4e04e7c36861f",
    "token": "9d9f4f43-0ce3-4ad2-891b-f0be9546aeab",
    "internal": "0||BR|03|1|6||||||||||||9||1~1~1~1||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotels": {
    "hotels": [
      {
        "code": 180687,
        "name": "Mission Inn Resort & Club",
        "categoryCode": "4EST",
        "categoryName": "4 STARS",
        "destinationCode": "MCO",
        "destinationName": "Orlando Area - Florida - FL",
        "zoneCode": 1,
        "zoneName": "Howey-In-The-Hills",
        "latitude": "28.725834",
        "longitude": "-81.781937",
        "rooms": [
          {
            "code": "SUI.CB",
            "name": "SUITE CLUB",
            "rates": [
              {
                "paymentType": "AT_WEB",
                "boardCode": "RO",
                "boardName": "ROOM ONLY",
                "rooms": 1,
                "adults": 1,
                "children": 1,
                "childrenAges": "4",
                "shiftRates": [
                  {
                    "rateKey": "20170917|20170922|W|235|180687|SUI.CB|STA|RO||1~1~1|4|N@37816A28834447B2A657B306E5A953531141",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "664.52",
                    "allotment": 176,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  }
                ]
              },
              {
                "paymentType": "AT_WEB",
                "boardCode": "DB",
                "boardName": "BUFFET BREAKFAST",
                "rooms": 1,
                "adults": 1,
                "children": 1,
                "childrenAges": "4",
                "shiftRates": [
                  {
                    "rateKey": "20170917|20170922|W|235|180687|SUI.CB|STA|DB||1~1~1|4|N@37816A28834447B2A657B306E5A953531141",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "846.92",
                    "allotment": 176,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  }
                ]
              }
            ]
          },
          {
            "code": "DBL.DX",
            "name": "DOUBLE DELUXE",
            "rates": [
              {
                "paymentType": "AT_WEB",
                "boardCode": "RO",
                "boardName": "ROOM ONLY",
                "rooms": 1,
                "adults": 1,
                "children": 1,
                "childrenAges": "4",
                "shiftRates": [
                  {
                    "rateKey": "20170917|20170922|W|235|180687|DBL.DX|STA|RO||1~1~1|4|N@37816A28834447B2A657B306E5A953531141",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "707.60",
                    "allotment": 176,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  }
                ]
              },
              {
                "paymentType": "AT_WEB",
                "boardCode": "DB",
                "boardName": "BUFFET BREAKFAST",
                "rooms": 1,
                "adults": 1,
                "children": 1,
                "childrenAges": "4",
                "shiftRates": [
                  {
                    "rateKey": "20170917|20170922|W|235|180687|DBL.DX|STA|DB||1~1~1|4|N@37816A28834447B2A657B306E5A953531141",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "890.00",
                    "allotment": 176,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  }
                ]
              }
            ]
          },
          {
            "code": "VIL.B2-1",
            "name": "VILLA TWO BEDROOMS VILLA SANTA CRUZ",
            "rates": [
              {
                "paymentType": "AT_WEB",
                "boardCode": "RO",
                "boardName": "ROOM ONLY",
                "rooms": 1,
                "adults": 1,
                "children": 1,
                "childrenAges": "4",
                "shiftRates": [
                  {
                    "rateKey": "20170917|20170922|W|235|180687|VIL.B2-1|STA|RO||1~1~1|4|N@37816A28834447B2A657B306E5A953531141",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "1815.15",
                    "allotment": 176,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  }
                ]
              },
              {
                "paymentType": "AT_WEB",
                "boardCode": "DB",
                "boardName": "BUFFET BREAKFAST",
                "rooms": 1,
                "adults": 1,
                "children": 1,
                "childrenAges": "4",
                "shiftRates": [
                  {
                    "rateKey": "20170917|20170922|W|235|180687|VIL.B2-1|STA|DB||1~1~1|4|N@37816A28834447B2A657B306E5A953531141",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "1997.55",
                    "allotment": 176,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  }
                ]
              }
            ]
          }
        ],
        "minRate": "664.52",
        "maxRate": "1997.55",
        "currency": "USD"
      }
    ],
    "checkIn": "2017-09-15",
    "total": 1,
    "checkOut": "2017-09-20"
  }
}
```



## <a name="rate"></a>![Type: ](https://apidocs.io/img/method.png "Rate") Rate



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateKey | string |  ``` Required ```  | TODO: Add a property description | 
| rateClass | string |  ``` Required ```  | TODO: Add a property description | 
| rateType | string |  ``` Required ```  | TODO: Add a property description | 
| net | string |  ``` Required ```  | TODO: Add a property description | 
| allotment | number |  ``` Required ```  | TODO: Add a property description | 
| rateCommentsId | string |  ``` Required ```  | TODO: Add a property description | 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| packaging | boolean |  ``` Required ```  | TODO: Add a property description | 
| boardCode | string |  ``` Required ```  | TODO: Add a property description | 
| boardName | string |  ``` Required ```  | TODO: Add a property description | 
| cancellationPolicies | [CancellationPolicy](#cancellation_policy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 
| childrenAges | string |  ``` Required ```  | TODO: Add a property description | 
| offers | [Offer](#offer) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "rateKey": "rateKey",
  "rateClass": "rateClass",
  "rateType": "rateType",
  "net": "net",
  "allotment": 124,
  "rateCommentsId": "rateCommentsId",
  "paymentType": "paymentType",
  "packaging": false,
  "boardCode": "boardCode",
  "boardName": "boardName",
  "cancellationPolicies": [
    {
      "amount": "amount",
      "from": "from"
    }
  ],
  "rooms": 124,
  "adults": 124,
  "children": 124,
  "childrenAges": "childrenAges",
  "offers": [
    {
      "code": "code",
      "name": "name",
      "amount": "amount"
    }
  ]
}
```



## <a name="supplier"></a>![Type: ](https://apidocs.io/img/method.png "Supplier") Supplier



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| vatNumber | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "name": "name",
  "vatNumber": "vatNumber"
}
```



## <a name="paxis100"></a>![Type: ](https://apidocs.io/img/method.png "Paxis100") Paxis100



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| roomId | number |  ``` Required ```  | TODO: Add a property description | 
| type | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "roomId": 215,
  "type": "type",
  "name": "name"
}
```



## <a name="modification_policies"></a>![Type: ](https://apidocs.io/img/method.png "ModificationPolicies") ModificationPolicies



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| cancellation | boolean |  ``` Required ```  | TODO: Add a property description | 
| modification | boolean |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "cancellation": true,
  "modification": true
}
```



## <a name="paxis"></a>![Type: ](https://apidocs.io/img/method.png "Paxis") Paxis



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| roomId | string |  ``` Required ```  | TODO: Add a property description | 
| type | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "roomId": "roomId",
  "type": "type",
  "name": "name"
}
```



## <a name="rooms91"></a>![Type: ](https://apidocs.io/img/method.png "Rooms91") Rooms91



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateKey | string |  ``` Required ```  | TODO: Add a property description | 
| paxes | [Paxis](#paxis) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "rateKey": "rateKey",
  "paxes": [
    {
      "roomId": "roomId",
      "type": "type",
      "name": "name"
    }
  ]
}
```



## <a name="holder"></a>![Type: ](https://apidocs.io/img/method.png "Holder") Holder



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| surname | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "name": "name",
  "surname": "surname"
}
```



## <a name="rate_discount"></a>![Type: ](https://apidocs.io/img/method.png "RateDiscount") RateDiscount



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| amount | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "amount": "amount"
}
```



## <a name="hotels7"></a>![Type: ](https://apidocs.io/img/method.png "Hotels7") Hotels7



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | number |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| categoryCode | string |  ``` Required ```  | TODO: Add a property description | 
| categoryName | string |  ``` Required ```  | TODO: Add a property description | 
| destinationCode | string |  ``` Required ```  | TODO: Add a property description | 
| destinationName | string |  ``` Required ```  | TODO: Add a property description | 
| zoneCode | number |  ``` Required ```  | TODO: Add a property description | 
| zoneName | string |  ``` Required ```  | TODO: Add a property description | 
| latitude | string |  ``` Required ```  | TODO: Add a property description | 
| longitude | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Room](#room) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| minRate | string |  ``` Required ```  | TODO: Add a property description | 
| maxRate | string |  ``` Required ```  | TODO: Add a property description | 
| currency | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": 215,
  "name": "name",
  "categoryCode": "categoryCode",
  "categoryName": "categoryName",
  "destinationCode": "destinationCode",
  "destinationName": "destinationName",
  "zoneCode": 215,
  "zoneName": "zoneName",
  "latitude": "latitude",
  "longitude": "longitude",
  "rooms": [
    {
      "code": "code",
      "name": "name",
      "rates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "allotment": 215,
          "rateCommentsId": "rateCommentsId",
          "paymentType": "paymentType",
          "packaging": true,
          "boardCode": "boardCode",
          "boardName": "boardName",
          "cancellationPolicies": [
            {
              "amount": "amount",
              "from": "from"
            }
          ],
          "rooms": 215,
          "adults": 215,
          "children": 215,
          "childrenAges": "childrenAges",
          "offers": [
            {
              "code": "code",
              "name": "name",
              "amount": "amount"
            }
          ]
        }
      ]
    }
  ],
  "minRate": "minRate",
  "maxRate": "maxRate",
  "currency": "currency"
}
```



## <a name="rooms83"></a>![Type: ](https://apidocs.io/img/method.png "Rooms83") Rooms83



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| rates | [Rate84](#rate84) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "rates": [
    {
      "rateKey": "rateKey",
      "rateClass": "rateClass",
      "rateType": "rateType",
      "net": "net",
      "rateComments": "rateComments",
      "paymentType": "paymentType",
      "packaging": true,
      "boardCode": "boardCode",
      "boardName": "boardName",
      "cancellationPolicies": [
        {
          "amount": "amount",
          "from": "from"
        }
      ],
      "rateBreakDown": {
        "rateDiscounts": [
          {
            "code": "code",
            "name": "name",
            "amount": "amount"
          }
        ]
      },
      "rooms": 215,
      "adults": 215,
      "children": 215,
      "childrenAges": "childrenAges",
      "offers": [
        {
          "code": "code",
          "name": "name",
          "amount": "amount"
        }
      ]
    }
  ]
}
```



## <a name="check_rate_request"></a>![Type: ](https://apidocs.io/img/method.png "CheckRateRequest") CheckRateRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rooms | [Rooms79](#rooms79) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "rooms": [
    {
      "rateKey": "20171115|20171120|W|52|1|SGL.ST|CG-EXT LONG RO|RO||1~1~0||N@A8921A639A0D46D88735806D109FA6E81544"
    }
  ]
}
```



## <a name="rooms75"></a>![Type: ](https://apidocs.io/img/method.png "Rooms75") Rooms75



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| rates | [Rate32](#rate32) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "rates": [
    {
      "paymentType": "paymentType",
      "boardCode": "boardCode",
      "boardName": "boardName",
      "rooms": 215,
      "adults": 215,
      "children": 215,
      "shiftRates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "allotment": 215,
          "checkIn": "checkIn",
          "checkOut": "checkOut"
        }
      ]
    }
  ]
}
```



## <a name="rooms62"></a>![Type: ](https://apidocs.io/img/method.png "Rooms62") Rooms62



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| rates | [Rate63](#rate63) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "rates": [
    {
      "rateKey": "rateKey",
      "rateClass": "rateClass",
      "rateType": "rateType",
      "net": "net",
      "allotment": 215,
      "rateCommentsId": "rateCommentsId",
      "paymentType": "paymentType",
      "packaging": true,
      "boardCode": "boardCode",
      "boardName": "boardName",
      "cancellationPolicies": [
        {
          "amount": "amount",
          "from": "from"
        }
      ],
      "rooms": 215,
      "adults": 215,
      "children": 215,
      "childrenAges": "childrenAges",
      "shiftRates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "allotment": 215,
          "checkIn": "checkIn",
          "checkOut": "checkOut"
        }
      ]
    }
  ]
}
```



## <a name="boards"></a>![Type: ](https://apidocs.io/img/method.png "Boards") Boards



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| included | boolean |  ``` Required ```  | TODO: Add a property description | 
| board | string |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "included": true,
  "board": [
    "board"
  ]
}
```



## <a name="rooms"></a>![Type: ](https://apidocs.io/img/method.png "Rooms") Rooms



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| included | boolean |  ``` Required ```  | TODO: Add a property description | 
| room | string |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "included": true,
  "room": [
    "room"
  ]
}
```



## <a name="room31"></a>![Type: ](https://apidocs.io/img/method.png "Room31") Room31



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| rates | [Rate32](#rate32) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "rates": [
    {
      "paymentType": "paymentType",
      "boardCode": "boardCode",
      "boardName": "boardName",
      "rooms": 215,
      "adults": 215,
      "children": 215,
      "shiftRates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "allotment": 215,
          "checkIn": "checkIn",
          "checkOut": "checkOut"
        }
      ]
    }
  ]
}
```



## <a name="room20"></a>![Type: ](https://apidocs.io/img/method.png "Room20") Room20



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| rates | [Rate21](#rate21) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "rates": [
    {
      "paymentType": "paymentType",
      "boardCode": "boardCode",
      "boardName": "boardName",
      "rooms": 215,
      "adults": 215,
      "children": 215,
      "childrenAges": "childrenAges",
      "shiftRates": [
        {
          "rateKey": "rateKey",
          "rateClass": "rateClass",
          "rateType": "rateType",
          "net": "net",
          "allotment": 215,
          "checkIn": "checkIn",
          "checkOut": "checkOut"
        }
      ]
    }
  ]
}
```



## <a name="stay13"></a>![Type: ](https://apidocs.io/img/method.png "Stay13") Stay13



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 
| shiftDays | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "checkIn": "checkIn",
  "checkOut": "checkOut",
  "shiftDays": "shiftDays"
}
```



## <a name="offer"></a>![Type: ](https://apidocs.io/img/method.png "Offer") Offer



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| amount | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "amount": "amount"
}
```



## <a name="cancellation_policy"></a>![Type: ](https://apidocs.io/img/method.png "CancellationPolicy") CancellationPolicy



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| amount | string |  ``` Required ```  | TODO: Add a property description | 
| from | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "amount": "amount",
  "from": "from"
}
```



## <a name="room"></a>![Type: ](https://apidocs.io/img/method.png "Room") Room



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| rates | [Rate](#rate) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code",
  "name": "name",
  "rates": [
    {
      "rateKey": "rateKey",
      "rateClass": "rateClass",
      "rateType": "rateType",
      "net": "net",
      "allotment": 215,
      "rateCommentsId": "rateCommentsId",
      "paymentType": "paymentType",
      "packaging": true,
      "boardCode": "boardCode",
      "boardName": "boardName",
      "cancellationPolicies": [
        {
          "amount": "amount",
          "from": "from"
        }
      ],
      "rooms": 215,
      "adults": 215,
      "children": 215,
      "childrenAges": "childrenAges",
      "offers": [
        {
          "code": "code",
          "name": "name",
          "amount": "amount"
        }
      ]
    }
  ]
}
```



## <a name="occupancy"></a>![Type: ](https://apidocs.io/img/method.png "Occupancy") Occupancy



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "rooms": 215,
  "adults": 215,
  "children": 215
}
```



## <a name="stay"></a>![Type: ](https://apidocs.io/img/method.png "Stay") Stay



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "checkIn": "checkIn",
  "checkOut": "checkOut"
}
```



## <a name="availability_by_hotel_code_request"></a>![Type: ](https://apidocs.io/img/method.png "Availability by hotel codeRequest") Availability by hotel codeRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay](#stay) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  }
}
```



## <a name="rate_break_down"></a>![Type: ](https://apidocs.io/img/method.png "RateBreakDown") RateBreakDown



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateDiscounts | [RateDiscount](#rate_discount) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "rateDiscounts": [
    {
      "code": "code",
      "name": "name",
      "amount": "amount"
    }
  ]
}
```



## <a name="rooms79"></a>![Type: ](https://apidocs.io/img/method.png "Rooms79") Rooms79



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateKey | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "rateKey": "rateKey"
}
```



## <a name="keywords"></a>![Type: ](https://apidocs.io/img/method.png "Keywords") Keywords



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| keyword | number |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "keyword": [
    215
  ]
}
```



## <a name="destination"></a>![Type: ](https://apidocs.io/img/method.png "Destination") Destination



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| code | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "code": "code"
}
```



## <a name="hotels"></a>![Type: ](https://apidocs.io/img/method.png "Hotels") Hotels



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| hotel | number |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "hotel": [
    215
  ]
}
```



## <a name="filter_by_accommodation_type_request"></a>![Type: ](https://apidocs.io/img/method.png "Filter by accommodation typeRequest") Filter by accommodation typeRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 
| accommodations | string |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "accommodations": [
    "HOTEL",
    "HOSTEL"
  ]
}
```



## <a name="filter_by_keyword_request"></a>![Type: ](https://apidocs.io/img/method.png "Filter by keywordRequest") Filter by keywordRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 
| keywords | [Keywords](#keywords) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "keywords": {
    "keyword": [
      34,
      38,
      100
    ]
  }
}
```



## <a name="filter_by_room_type_request"></a>![Type: ](https://apidocs.io/img/method.png "Filter by room typeRequest") Filter by room typeRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms](#rooms) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 2,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "rooms": {
    "included": true,
    "room": [
      "DBT.ST"
    ]
  }
}
```



## <a name="rate32"></a>![Type: ](https://apidocs.io/img/method.png "Rate32") Rate32



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| boardCode | string |  ``` Required ```  | TODO: Add a property description | 
| boardName | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 
| shiftRates | [ShiftRate](#shift_rate) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "paymentType": "paymentType",
  "boardCode": "boardCode",
  "boardName": "boardName",
  "rooms": 215,
  "adults": 215,
  "children": 215,
  "shiftRates": [
    {
      "rateKey": "rateKey",
      "rateClass": "rateClass",
      "rateType": "rateType",
      "net": "net",
      "allotment": 215,
      "checkIn": "checkIn",
      "checkOut": "checkOut"
    }
  ]
}
```



## <a name="hotels29"></a>![Type: ](https://apidocs.io/img/method.png "Hotels29") Hotels29



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| hotels | [Hotels30](#hotels30) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| total | number |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "hotels": [
    {
      "code": 215,
      "name": "name",
      "categoryCode": "categoryCode",
      "categoryName": "categoryName",
      "destinationCode": "destinationCode",
      "destinationName": "destinationName",
      "zoneCode": 215,
      "zoneName": "zoneName",
      "latitude": "latitude",
      "longitude": "longitude",
      "rooms": [
        {
          "code": "code",
          "name": "name",
          "rates": [
            {
              "paymentType": "paymentType",
              "boardCode": "boardCode",
              "boardName": "boardName",
              "rooms": 215,
              "adults": 215,
              "children": 215,
              "shiftRates": [
                {
                  "rateKey": "rateKey",
                  "rateClass": "rateClass",
                  "rateType": "rateType",
                  "net": "net",
                  "allotment": 215,
                  "checkIn": "checkIn",
                  "checkOut": "checkOut"
                }
              ]
            }
          ]
        }
      ],
      "minRate": "minRate",
      "maxRate": "maxRate",
      "currency": "currency"
    }
  ],
  "checkIn": "checkIn",
  "total": 215,
  "checkOut": "checkOut"
}
```



## <a name="geolocation"></a>![Type: ](https://apidocs.io/img/method.png "Geolocation") Geolocation



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| latitude | precision |  ``` Required ```  | TODO: Add a property description | 
| longitude | precision |  ``` Required ```  | TODO: Add a property description | 
| radius | number |  ``` Required ```  | TODO: Add a property description | 
| unit | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "latitude": 215.706192097024,
  "longitude": 215.706192097024,
  "radius": 215,
  "unit": "unit"
}
```



## <a name="availability_by_geolocation_request"></a>![Type: ](https://apidocs.io/img/method.png "Availability by geolocationRequest") Availability by geolocationRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| geolocation | [Geolocation](#geolocation) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "geolocation": {
    "latitude": 39.57119,
    "longitude": 2.6466339999999491,
    "radius": 20,
    "unit": "km"
  }
}
```



## <a name="shift_rate"></a>![Type: ](https://apidocs.io/img/method.png "ShiftRate") ShiftRate



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| rateKey | string |  ``` Required ```  | TODO: Add a property description | 
| rateClass | string |  ``` Required ```  | TODO: Add a property description | 
| rateType | string |  ``` Required ```  | TODO: Add a property description | 
| net | string |  ``` Required ```  | TODO: Add a property description | 
| allotment | number |  ``` Required ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "rateKey": "rateKey",
  "rateClass": "rateClass",
  "rateType": "rateType",
  "net": "net",
  "allotment": 215,
  "checkIn": "checkIn",
  "checkOut": "checkOut"
}
```



## <a name="rate21"></a>![Type: ](https://apidocs.io/img/method.png "Rate21") Rate21



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| paymentType | string |  ``` Required ```  | TODO: Add a property description | 
| boardCode | string |  ``` Required ```  | TODO: Add a property description | 
| boardName | string |  ``` Required ```  | TODO: Add a property description | 
| rooms | number |  ``` Required ```  | TODO: Add a property description | 
| adults | number |  ``` Required ```  | TODO: Add a property description | 
| children | number |  ``` Required ```  | TODO: Add a property description | 
| childrenAges | string |  ``` Required ```  | TODO: Add a property description | 
| shiftRates | [ShiftRate](#shift_rate) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "paymentType": "paymentType",
  "boardCode": "boardCode",
  "boardName": "boardName",
  "rooms": 215,
  "adults": 215,
  "children": 215,
  "childrenAges": "childrenAges",
  "shiftRates": [
    {
      "rateKey": "rateKey",
      "rateClass": "rateClass",
      "rateType": "rateType",
      "net": "net",
      "allotment": 215,
      "checkIn": "checkIn",
      "checkOut": "checkOut"
    }
  ]
}
```



## <a name="hotels18"></a>![Type: ](https://apidocs.io/img/method.png "Hotels18") Hotels18



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| hotels | [Hotels19](#hotels19) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| total | number |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "hotels": [
    {
      "code": 215,
      "name": "name",
      "categoryCode": "categoryCode",
      "categoryName": "categoryName",
      "destinationCode": "destinationCode",
      "destinationName": "destinationName",
      "zoneCode": 215,
      "zoneName": "zoneName",
      "latitude": "latitude",
      "longitude": "longitude",
      "rooms": [
        {
          "code": "code",
          "name": "name",
          "rates": [
            {
              "paymentType": "paymentType",
              "boardCode": "boardCode",
              "boardName": "boardName",
              "rooms": 215,
              "adults": 215,
              "children": 215,
              "childrenAges": "childrenAges",
              "shiftRates": [
                {
                  "rateKey": "rateKey",
                  "rateClass": "rateClass",
                  "rateType": "rateType",
                  "net": "net",
                  "allotment": 215,
                  "checkIn": "checkIn",
                  "checkOut": "checkOut"
                }
              ]
            }
          ]
        }
      ],
      "minRate": "minRate",
      "maxRate": "maxRate",
      "currency": "currency"
    }
  ],
  "checkIn": "checkIn",
  "total": 173,
  "checkOut": "checkOut"
}
```



## <a name="availability_by_destination_request"></a>![Type: ](https://apidocs.io/img/method.png "Availability by destinationRequest") Availability by destinationRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| destination | [Destination](#destination) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "destination": {
    "code": "MCO"
  }
}
```



## <a name="hotels6"></a>![Type: ](https://apidocs.io/img/method.png "Hotels6") Hotels6



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| hotels | [Hotels7](#hotels7) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| total | number |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "hotels": [
    {
      "code": 173,
      "name": "name",
      "categoryCode": "categoryCode",
      "categoryName": "categoryName",
      "destinationCode": "destinationCode",
      "destinationName": "destinationName",
      "zoneCode": 173,
      "zoneName": "zoneName",
      "latitude": "latitude",
      "longitude": "longitude",
      "rooms": [
        {
          "code": "code",
          "name": "name",
          "rates": [
            {
              "rateKey": "rateKey",
              "rateClass": "rateClass",
              "rateType": "rateType",
              "net": "net",
              "allotment": 173,
              "rateCommentsId": "rateCommentsId",
              "paymentType": "paymentType",
              "packaging": true,
              "boardCode": "boardCode",
              "boardName": "boardName",
              "cancellationPolicies": [
                {
                  "amount": "amount",
                  "from": "from"
                }
              ],
              "rooms": 173,
              "adults": 173,
              "children": 173,
              "childrenAges": "childrenAges",
              "offers": [
                {
                  "code": "code",
                  "name": "name",
                  "amount": "amount"
                }
              ]
            }
          ]
        }
      ],
      "minRate": "minRate",
      "maxRate": "maxRate",
      "currency": "currency"
    }
  ],
  "checkIn": "checkIn",
  "total": 173,
  "checkOut": "checkOut"
}
```



## <a name="audit_data"></a>![Type: ](https://apidocs.io/img/method.png "AuditData") AuditData



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| processTime | string |  ``` Required ```  | TODO: Add a property description | 
| timestamp | string |  ``` Required ```  | TODO: Add a property description | 
| requestHost | string |  ``` Required ```  | TODO: Add a property description | 
| serverId | string |  ``` Required ```  | TODO: Add a property description | 
| environment | string |  ``` Required ```  | TODO: Add a property description | 
| release | string |  ``` Required ```  | TODO: Add a property description | 
| token | string |  ``` Required ```  | TODO: Add a property description | 
| internal | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "processTime": "processTime",
  "timestamp": "timestamp",
  "requestHost": "requestHost",
  "serverId": "serverId",
  "environment": "environment",
  "release": "release",
  "token": "token",
  "internal": "internal"
}
```



## <a name="availability_by_hotel_code_response"></a>![Type: ](https://apidocs.io/img/method.png "Availability by hotel codeResponse") Availability by hotel codeResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| hotels | [Hotels6](#hotels6) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "33",
    "timestamp": "2017-08-29 18:08:10.034",
    "requestHost": "212.170.239.110",
    "serverId": "sa3RKSJACHXE79K.env#PL",
    "environment": "[int]",
    "release": "4c0c21f7a3982f3ad0cf88b921c4e04e7c36861f",
    "token": "b578cb37-fa88-405d-899b-b9514a15aedb",
    "internal": "0|9984AA31D1D140DEBA333FA7C03598D21808|BR|06|1|1||||||||||||1||1~1~3~1||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotels": {
    "hotels": [
      {
        "code": 106753,
        "name": "Wingate By Wyndham Orlando International Airport",
        "categoryCode": "3EST",
        "categoryName": "3 STARS",
        "destinationCode": "MCO",
        "destinationName": "Orlando Area - Florida - FL",
        "zoneCode": 2,
        "zoneName": "Orlando International Airport",
        "latitude": "28.4626",
        "longitude": "-81.308",
        "rooms": [
          {
            "code": "DBL.2Q",
            "name": "DOUBLE TWO QUEEN BEDS",
            "rates": [
              {
                "rateKey": "20171219|20171220|W|235|106753|DBL.2Q|COM|DB||1~3~1|2|N@9984AA31D1D140DEBA333FA7C03598D21808",
                "rateClass": "NOR",
                "rateType": "BOOKABLE",
                "net": "104.84",
                "allotment": 5,
                "rateCommentsId": "235|38397|0",
                "paymentType": "AT_WEB",
                "packaging": false,
                "boardCode": "DB",
                "boardName": "BUFFET BREAKFAST",
                "cancellationPolicies": [
                  {
                    "amount": "104.84",
                    "from": "2017-12-16T04:59:00+00:00"
                  }
                ],
                "rooms": 1,
                "adults": 3,
                "children": 1,
                "childrenAges": "2",
                "offers": [
                  {
                    "code": "9008",
                    "name": "Extra bed discount",
                    "amount": "-95.64"
                  }
                ]
              }
            ]
          }
        ],
        "minRate": "104.84",
        "maxRate": "104.84",
        "currency": "USD"
      }
    ],
    "checkIn": "2017-12-19",
    "total": 1,
    "checkOut": "2017-12-20"
  }
}
```



## <a name="review"></a>![Type: ](https://apidocs.io/img/method.png "Review") Review



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| type | string |  ``` Required ```  | TODO: Add a property description | 
| maxRate | number |  ``` Required ```  | TODO: Add a property description | 
| minRate | number |  ``` Required ```  | TODO: Add a property description | 
| minReviewCount | number |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "type": "type",
  "maxRate": 173,
  "minRate": 173,
  "minReviewCount": 173
}
```



## <a name="filter_by_review_rating_request"></a>![Type: ](https://apidocs.io/img/method.png "Filter by review ratingRequest") Filter by review ratingRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 
| reviews | [Review](#review) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "reviews": [
    {
      "type": "HOTELBEDS",
      "maxRate": 5,
      "minRate": 1,
      "minReviewCount": 3
    }
  ]
}
```



## <a name="filter_by_board_code_request"></a>![Type: ](https://apidocs.io/img/method.png "Filter by board codeRequest") Filter by board codeRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 
| boards | [Boards](#boards) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "boards": {
    "included": true,
    "board": [
      "RO",
      "BB"
    ]
  }
}
```



## <a name="paxis110"></a>![Type: ](https://apidocs.io/img/method.png "Paxis110") Paxis110



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| roomId | number |  ``` Required ```  | TODO: Add a property description | 
| type | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| surname | string |  ``` Optional ```  | TODO: Add a property description | 
| age | number |  ``` Optional ```  | TODO: Add a property description | 



#### Example
```
{
  "roomId": 173,
  "type": "type",
  "name": "name",
  "surname": "surname",
  "age": 173
}
```



## <a name="rooms109"></a>![Type: ](https://apidocs.io/img/method.png "Rooms109") Rooms109



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| status | string |  ``` Required ```  | TODO: Add a property description | 
| id | number |  ``` Required ```  | TODO: Add a property description | 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| paxes | [Paxis110](#paxis110) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| rates | [Rate101](#rate101) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "status": "status",
  "id": 173,
  "code": "code",
  "name": "name",
  "paxes": [
    {
      "roomId": 173,
      "type": "type",
      "name": "name",
      "surname": "surname",
      "age": 173
    }
  ],
  "rates": [
    {
      "rateClass": "rateClass",
      "net": "net",
      "rateComments": "rateComments",
      "paymentType": "paymentType",
      "packaging": true,
      "boardCode": "boardCode",
      "boardName": "boardName",
      "cancellationPolicies": [
        {
          "amount": "amount",
          "from": "from"
        }
      ],
      "rooms": 173,
      "adults": 173,
      "children": 173
    }
  ]
}
```



## <a name="rooms99"></a>![Type: ](https://apidocs.io/img/method.png "Rooms99") Rooms99



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| status | string |  ``` Required ```  | TODO: Add a property description | 
| id | number |  ``` Required ```  | TODO: Add a property description | 
| code | string |  ``` Required ```  | TODO: Add a property description | 
| name | string |  ``` Required ```  | TODO: Add a property description | 
| paxes | [Paxis100](#paxis100) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| rates | [Rate101](#rate101) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 



#### Example
```
{
  "status": "status",
  "id": 173,
  "code": "code",
  "name": "name",
  "paxes": [
    {
      "roomId": 173,
      "type": "type",
      "name": "name"
    }
  ],
  "rates": [
    {
      "rateClass": "rateClass",
      "net": "net",
      "rateComments": "rateComments",
      "paymentType": "paymentType",
      "packaging": true,
      "boardCode": "boardCode",
      "boardName": "boardName",
      "cancellationPolicies": [
        {
          "amount": "amount",
          "from": "from"
        }
      ],
      "rooms": 173,
      "adults": 173,
      "children": 173
    }
  ]
}
```



## <a name="booking_request"></a>![Type: ](https://apidocs.io/img/method.png "BookingRequest") BookingRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| holder | [Holder](#holder) |  ``` Required ```  | TODO: Add a property description | 
| rooms | [Rooms91](#rooms91) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| clientReference | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "holder": {
    "name": "IntegrationTestFirstName",
    "surname": "IntegrationTestLastName"
  },
  "rooms": [
    {
      "rateKey": "20171115|20171120|W|52|1|DBL.ST|ID_B2B_25|RO|EM4TIES|1~1~0||N@1884739731",
      "paxes": [
        {
          "roomId": "1",
          "type": "AD",
          "name": "Adult Name"
        }
      ]
    }
  ],
  "clientReference": "IntegrationAgency"
}
```



## <a name="hotels73"></a>![Type: ](https://apidocs.io/img/method.png "Hotels73") Hotels73



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| hotels | [Hotels74](#hotels74) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| total | number |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "hotels": [
    {
      "code": 173,
      "name": "name",
      "categoryCode": "categoryCode",
      "categoryName": "categoryName",
      "destinationCode": "destinationCode",
      "destinationName": "destinationName",
      "zoneCode": 173,
      "zoneName": "zoneName",
      "latitude": "latitude",
      "longitude": "longitude",
      "rooms": [
        {
          "code": "code",
          "name": "name",
          "rates": [
            {
              "paymentType": "paymentType",
              "boardCode": "boardCode",
              "boardName": "boardName",
              "rooms": 173,
              "adults": 173,
              "children": 173,
              "shiftRates": [
                {
                  "rateKey": "rateKey",
                  "rateClass": "rateClass",
                  "rateType": "rateType",
                  "net": "net",
                  "allotment": 173,
                  "checkIn": "checkIn",
                  "checkOut": "checkOut"
                }
              ]
            }
          ]
        }
      ],
      "minRate": "minRate",
      "maxRate": "maxRate",
      "currency": "currency"
    }
  ],
  "checkIn": "checkIn",
  "total": 173,
  "checkOut": "checkOut"
}
```



## <a name="other_filters_response"></a>![Type: ](https://apidocs.io/img/method.png "Other filtersResponse") Other filtersResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| hotels | [Hotels73](#hotels73) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "94",
    "timestamp": "2017-09-08 12:47:16.646",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "23c542efb2ca3c1642f5f0d87c6c410b81c52ee3",
    "token": "9536f01d-d2b6-40bf-ac8b-b7b8567b28cf",
    "internal": "0||BR|01|1|2||||||||||||1||1~1~1~0||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotels": {
    "hotels": [
      {
        "code": 186629,
        "name": "K+K Hotel Picasso",
        "categoryCode": "4EST",
        "categoryName": "4 STARS",
        "destinationCode": "BCN",
        "destinationName": "Barcelona",
        "zoneCode": 8,
        "zoneName": "El Born",
        "latitude": "41.386763",
        "longitude": "2.183858",
        "rooms": [
          {
            "code": "DBL.AS",
            "name": "DOUBLE CLASSIC",
            "rates": [
              {
                "paymentType": "AT_WEB",
                "boardCode": "BB",
                "boardName": "BED AND BREAKFAST",
                "rooms": 1,
                "adults": 1,
                "children": 0,
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|102|186629|DBL.AS|CG-FIT B2B|BB||1~1~0||N@6A20D3E64C4445CAB51E27C08DBEF84B1247",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "1162.65",
                    "allotment": 1,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|102|186629|DBL.AS|CG-FIT B2B|BB||1~1~0||N@6A20D3E64C4445CAB51E27C08DBEF84B1247",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "1162.65",
                    "allotment": 1,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  }
                ]
              }
            ]
          }
        ],
        "minRate": "1162.65",
        "maxRate": "1162.65",
        "currency": "EUR"
      }
    ],
    "checkIn": "2017-09-15",
    "total": 1,
    "checkOut": "2017-09-20"
  }
}
```



## <a name="other_filters_request"></a>![Type: ](https://apidocs.io/img/method.png "Other filtersRequest") Other filtersRequest



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| stay | [Stay13](#stay13) |  ``` Required ```  | TODO: Add a property description | 
| occupancies | [Occupancy](#occupancy) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| hotels | [Hotels](#hotels) |  ``` Required ```  | TODO: Add a property description | 
| filter | [Filter](#filter) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "stay": {
    "checkIn": "2017-11-15",
    "checkOut": "2017-11-20",
    "shiftDays": "2"
  },
  "occupancies": [
    {
      "rooms": 1,
      "adults": 1,
      "children": 0
    }
  ],
  "hotels": {
    "hotel": [
      1,
      271
    ]
  },
  "filter": {
    "minRate": 100.0,
    "maxRate": 1700.0,
    "minCategory": 3,
    "maxCategory": 5,
    "maxRooms": 3,
    "maxRatesPerRoom": 3,
    "paymentType": "AT_HOTEL",
    "packaging": true,
    "hotelPackage": "YES",
    "contract": "CG-FIT B2B"
  }
}
```



## <a name="hotels60"></a>![Type: ](https://apidocs.io/img/method.png "Hotels60") Hotels60



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| hotels | [Hotels61](#hotels61) |  ``` Required ```  ``` Collection ```  | TODO: Add a property description | 
| checkIn | string |  ``` Required ```  | TODO: Add a property description | 
| total | number |  ``` Required ```  | TODO: Add a property description | 
| checkOut | string |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "hotels": [
    {
      "code": 173,
      "name": "name",
      "categoryCode": "categoryCode",
      "categoryName": "categoryName",
      "destinationCode": "destinationCode",
      "destinationName": "destinationName",
      "zoneCode": 173,
      "zoneName": "zoneName",
      "latitude": "latitude",
      "longitude": "longitude",
      "rooms": [
        {
          "code": "code",
          "name": "name",
          "rates": [
            {
              "rateKey": "rateKey",
              "rateClass": "rateClass",
              "rateType": "rateType",
              "net": "net",
              "allotment": 173,
              "rateCommentsId": "rateCommentsId",
              "paymentType": "paymentType",
              "packaging": true,
              "boardCode": "boardCode",
              "boardName": "boardName",
              "cancellationPolicies": [
                {
                  "amount": "amount",
                  "from": "from"
                }
              ],
              "rooms": 173,
              "adults": 173,
              "children": 173,
              "childrenAges": "childrenAges",
              "shiftRates": [
                {
                  "rateKey": "rateKey",
                  "rateClass": "rateClass",
                  "rateType": "rateType",
                  "net": "net",
                  "allotment": 173,
                  "checkIn": "checkIn",
                  "checkOut": "checkOut"
                }
              ]
            }
          ]
        }
      ],
      "minRate": "minRate",
      "maxRate": "maxRate",
      "currency": "currency"
    }
  ],
  "checkIn": "checkIn",
  "total": 173,
  "checkOut": "checkOut"
}
```



## <a name="filter_by_review_rating_response"></a>![Type: ](https://apidocs.io/img/method.png "Filter by review ratingResponse") Filter by review ratingResponse



> TODO: Add a model description





| Name | Type | Tags | Description |
|-----------|------| ---- |-------------| 
| auditData | [AuditData](#audit_data) |  ``` Required ```  | TODO: Add a property description | 
| hotels | [Hotels60](#hotels60) |  ``` Required ```  | TODO: Add a property description | 



#### Example
```
{
  "auditData": {
    "processTime": "42",
    "timestamp": "2017-08-30 14:46:02.533",
    "requestHost": "212.170.239.110",
    "serverId": "sa37AUX3ROLBLIS.env#PL",
    "environment": "[int]",
    "release": "4c0c21f7a3982f3ad0cf88b921c4e04e7c36861f",
    "token": "1534a87d-c8a6-4e12-9de9-d01e46b3f3ac",
    "internal": "0|DCF3106D92A441F2918E1CEF9F65E2AF1446|BR|06|1|25||||||||||||1||1~1~2~1||0||0|wuupfvswdqfz342cejxfv3ku||"
  },
  "hotels": {
    "hotels": [
      {
        "code": 1,
        "name": "Villa Dorada",
        "categoryCode": "3EST",
        "categoryName": "3 STARS",
        "destinationCode": "SAL",
        "destinationName": "Salou Area / Costa Dorada",
        "zoneCode": 10,
        "zoneName": "Salou",
        "latitude": "41.06865947991072",
        "longitude": "1.1524744666303377",
        "rooms": [
          {
            "code": "DBT.ST-1",
            "name": "Double or Twin 2 ADULTS 1 CHILD",
            "rates": [
              {
                "rateKey": "20170915|20170920|W|52|1|DBT.ST-1|CG-EXT LONG RO|RO||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                "rateClass": "NOR",
                "rateType": "BOOKABLE",
                "net": "308.59",
                "allotment": 50,
                "rateCommentsId": "52|83709|0",
                "paymentType": "AT_WEB",
                "packaging": false,
                "boardCode": "RO",
                "boardName": "ROOM ONLY",
                "cancellationPolicies": [
                  {
                    "amount": "77.95",
                    "from": "2017-09-12T21:59:00+00:00"
                  },
                  {
                    "amount": "155.90",
                    "from": "2017-09-14T21:59:00+00:00"
                  }
                ],
                "rooms": 1,
                "adults": 2,
                "children": 1,
                "childrenAges": "2",
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|52|1|DBT.ST-1|CG-EXT LONG RO|RO||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "349.17",
                    "allotment": 50,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|52|1|DBT.ST-1|CG-EXT LONG RO|RO||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "328.88",
                    "allotment": 50,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  },
                  {
                    "rateKey": "20170917|20170922|W|52|1|DBT.ST-1|CG-EXT LONG RO|RO||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "288.30",
                    "allotment": 55,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  },
                  {
                    "rateKey": "20170916|20170921|W|52|1|DBT.ST-1|CG-EXT LONG RO|RO||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "288.30",
                    "allotment": 50,
                    "checkIn": "2017-09-16",
                    "checkOut": "2017-09-21"
                  }
                ]
              },
              {
                "rateKey": "20170915|20170920|W|52|1|DBT.ST-1|CG-EXT LONG BB|BB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                "rateClass": "NOR",
                "rateType": "BOOKABLE",
                "net": "319.29",
                "allotment": 50,
                "rateCommentsId": "52|83711|0",
                "paymentType": "AT_WEB",
                "packaging": false,
                "boardCode": "BB",
                "boardName": "BED AND BREAKFAST",
                "cancellationPolicies": [
                  {
                    "amount": "80.09",
                    "from": "2017-09-12T21:59:00+00:00"
                  },
                  {
                    "amount": "160.18",
                    "from": "2017-09-14T21:59:00+00:00"
                  }
                ],
                "rooms": 1,
                "adults": 2,
                "children": 1,
                "childrenAges": "2",
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|52|1|DBT.ST-1|CG-EXT LONG BB|BB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "359.87",
                    "allotment": 50,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|52|1|DBT.ST-1|CG-EXT LONG BB|BB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "339.58",
                    "allotment": 50,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  },
                  {
                    "rateKey": "20170917|20170922|W|52|1|DBT.ST-1|CG-EXT LONG BB|BB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "299.00",
                    "allotment": 55,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  },
                  {
                    "rateKey": "20170916|20170921|W|52|1|DBT.ST-1|CG-EXT LONG BB|BB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "299.00",
                    "allotment": 50,
                    "checkIn": "2017-09-16",
                    "checkOut": "2017-09-21"
                  }
                ]
              },
              {
                "rateKey": "20170915|20170920|W|52|1|DBT.ST-1|CG-EXT LONG HB|HB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                "rateClass": "NOR",
                "rateType": "BOOKABLE",
                "net": "340.64",
                "allotment": 50,
                "rateCommentsId": "52|83713|0",
                "paymentType": "AT_WEB",
                "packaging": false,
                "boardCode": "HB",
                "boardName": "HALF BOARD",
                "cancellationPolicies": [
                  {
                    "amount": "84.36",
                    "from": "2017-09-12T21:59:00+00:00"
                  },
                  {
                    "amount": "168.72",
                    "from": "2017-09-14T21:59:00+00:00"
                  }
                ],
                "rooms": 1,
                "adults": 2,
                "children": 1,
                "childrenAges": "2",
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|52|1|DBT.ST-1|CG-EXT LONG HB|HB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "381.22",
                    "allotment": 50,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|52|1|DBT.ST-1|CG-EXT LONG HB|HB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "360.93",
                    "allotment": 50,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  },
                  {
                    "rateKey": "20170917|20170922|W|52|1|DBT.ST-1|CG-EXT LONG HB|HB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "320.35",
                    "allotment": 55,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  },
                  {
                    "rateKey": "20170916|20170921|W|52|1|DBT.ST-1|CG-EXT LONG HB|HB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "320.35",
                    "allotment": 50,
                    "checkIn": "2017-09-16",
                    "checkOut": "2017-09-21"
                  }
                ]
              },
              {
                "rateKey": "20170915|20170920|W|52|1|DBT.ST-1|CG-EXT LONG FB|FB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                "rateClass": "NOR",
                "rateType": "BOOKABLE",
                "net": "426.08",
                "allotment": 50,
                "rateCommentsId": "52|83715|0",
                "paymentType": "AT_WEB",
                "packaging": false,
                "boardCode": "FB",
                "boardName": "FULL BOARD",
                "cancellationPolicies": [
                  {
                    "amount": "101.44",
                    "from": "2017-09-12T21:59:00+00:00"
                  },
                  {
                    "amount": "202.88",
                    "from": "2017-09-14T21:59:00+00:00"
                  }
                ],
                "rooms": 1,
                "adults": 2,
                "children": 1,
                "childrenAges": "2",
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|52|1|DBT.ST-1|CG-EXT LONG FB|FB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "466.64",
                    "allotment": 50,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|52|1|DBT.ST-1|CG-EXT LONG FB|FB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "446.36",
                    "allotment": 50,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  },
                  {
                    "rateKey": "20170917|20170922|W|52|1|DBT.ST-1|CG-EXT LONG FB|FB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "405.80",
                    "allotment": 55,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  },
                  {
                    "rateKey": "20170916|20170921|W|52|1|DBT.ST-1|CG-EXT LONG FB|FB||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "405.80",
                    "allotment": 50,
                    "checkIn": "2017-09-16",
                    "checkOut": "2017-09-21"
                  }
                ]
              },
              {
                "rateKey": "20170915|20170920|W|52|1|DBT.ST-1|CG-EXT LONG AI|AI||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                "rateClass": "NOR",
                "rateType": "BOOKABLE",
                "net": "575.54",
                "allotment": 50,
                "rateCommentsId": "52|83717|0",
                "paymentType": "AT_WEB",
                "packaging": false,
                "boardCode": "AI",
                "boardName": "ALL INCLUSIVE",
                "cancellationPolicies": [
                  {
                    "amount": "131.34",
                    "from": "2017-09-12T21:59:00+00:00"
                  },
                  {
                    "amount": "262.68",
                    "from": "2017-09-14T21:59:00+00:00"
                  }
                ],
                "rooms": 1,
                "adults": 2,
                "children": 1,
                "childrenAges": "2",
                "shiftRates": [
                  {
                    "rateKey": "20170913|20170918|W|52|1|DBT.ST-1|CG-EXT LONG AI|AI||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "616.12",
                    "allotment": 50,
                    "checkIn": "2017-09-13",
                    "checkOut": "2017-09-18"
                  },
                  {
                    "rateKey": "20170914|20170919|W|52|1|DBT.ST-1|CG-EXT LONG AI|AI||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "595.83",
                    "allotment": 50,
                    "checkIn": "2017-09-14",
                    "checkOut": "2017-09-19"
                  },
                  {
                    "rateKey": "20170917|20170922|W|52|1|DBT.ST-1|CG-EXT LONG AI|AI||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "555.25",
                    "allotment": 55,
                    "checkIn": "2017-09-17",
                    "checkOut": "2017-09-22"
                  },
                  {
                    "rateKey": "20170916|20170921|W|52|1|DBT.ST-1|CG-EXT LONG AI|AI||1~2~1|2|N@DCF3106D92A441F2918E1CEF9F65E2AF1446",
                    "rateClass": "NOR",
                    "rateType": "BOOKABLE",
                    "net": "555.25",
                    "allotment": 50,
                    "checkIn": "2017-09-16",
                    "checkOut": "2017-09-21"
                  }
                ]
              }
            ]
          }
        ],
        "minRate": "288.30",
        "maxRate": "616.12",
        "currency": "EUR"
      }
    ],
    "checkIn": "2017-09-15",
    "total": 1,
    "checkOut": "2017-09-20"
  }
}
```




