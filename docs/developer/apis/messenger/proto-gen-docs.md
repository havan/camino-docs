# Valldemossa Protocol
<a name="top"></a>




<a name="tcm_messages_holiday_home-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/messages/holiday_home.proto

<figure>
<img class="zoom" src="/img/holiday_home.proto.dot.svg"/>
<figcaption align = "center"><b>Fig.1:</b> HolidayHome Messages</figcaption>
</figure>



<a name="tcm-messages-HolidayHomeSearchRequest"></a>

### HolidayHomeSearchRequest
### HolidayHomeSearchRequest Message Type

![HolidayHomeSearchRequestDiagram](http://localhost:3000/img/holiday_home.proto.dot.svg)

The `HolidayHomeSearchRequest` message type facilitates the request for holiday
home searches within the platform. This message encompasses a variety of
attributes essential for a refined search experience:

- **header (tcm.protobuf.Header)**: This mandatory field contains metadata for
the message, including API version, an informative message string, and both
sender and receiver wallet addresses.
- **external_session_id (string)**: An identifier for external sessions, aiding
in tracking and continuity across sessions.
- **enrichment (string)**: Enables additional contextual information to be added
to the search request.
- **currency (string)**: Specifies the desired currency for the transaction.
- **language (string)**: Indicates the preferred language for communication.
- **market (string)**: Describes the target market or audience segment for the
search.
- **include_on_request (string)**: Provides a specifier for any additional
inclusion criteria.
- **include_combinations (string)**: Indicates if combinations of search
criteria should be included in results.
- **geo_location (tcm.protobuf.GeoLocation)**: An object representing
geographical coordinates or area to refine the search within a certain location.
- **free_text (string)**: Allows users to input open-text search criteria or
notes.
- **speech_request (string)**: **[FIXME]** A field which is currently a string
but might need reconsideration. It appears to be intended to capture
speech-based search requests, suggesting it might be more appropriate as a
boolean.
- **filters (repeated tcm.protobuf.Filter)**: A list of filter objects to refine
the search based on specific criteria or categories.
- **homes (repeated tcm.protobuf.HolidayHome)**: Allows the inclusion of
specific holiday homes in the search request, possibly for comparison or as part
of a wishlist.

Developers leveraging this message type should ensure proper validation and
handling, especially considering fields that are still under review, like
`speech_request`.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header | [tcm.protobuf.Header](#tcm-protobuf-Header) |  | Message Header Contains api version, message info string, sender &amp; receiver wallet addresses |
| external_session_id | [string](#string) |  |  |
| enrichment | [string](#string) |  |  |
| currency | [string](#string) |  |  |
| language | [string](#string) |  |  |
| market | [string](#string) |  |  |
| include_on_request | [string](#string) |  |  |
| include_combinations | [string](#string) |  |  |
| geo_location | [tcm.protobuf.GeoLocation](#tcm-protobuf-GeoLocation) |  | Geo Location |
| free_text | [string](#string) |  |  |
| speech_request | [string](#string) |  | FIXME: String? Should this be a boolean? |
| filters | [tcm.protobuf.Filter](#tcm-protobuf-Filter) | repeated |  |
| homes | [tcm.protobuf.HolidayHome](#tcm-protobuf-HolidayHome) | repeated |  |






<a name="tcm-messages-HolidayHomeSearchResponse"></a>

### HolidayHomeSearchResponse
Holiday Home Search Response


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header | [tcm.protobuf.Header](#tcm-protobuf-Header) |  | Message Header Contains api version, message info string, sender &amp; receiver wallet addresses |
| context | [string](#string) |  |  |
| errors | [string](#string) |  |  |
| warnings | [string](#string) |  |  |
| supplier_code | [string](#string) |  |  |
| external_session_id | [string](#string) |  |  |
| search_id | [string](#string) |  |  |





 

 

 

 



<a name="tcm_messages_network_fee-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/messages/network_fee.proto

<figure>
<img class="zoom" src="/img/network_fee.proto.dot.svg"/>
<figcaption align = "center"><b>Fig.2:</b> NetworkFee Messages</figcaption>
</figure>



<a name="tcm-messages-NetworkFeeRequest"></a>

### NetworkFeeRequest
Network fee request message


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header | [tcm.protobuf.Header](#tcm-protobuf-Header) |  | Message Header Contains api version, message info string, sender &amp; receiver wallet addresses |
| block_height | [int64](#int64) |  | Why does the request needs a block height? |






<a name="tcm-messages-NetworkFeeResponse"></a>

### NetworkFeeResponse
Network fee response message
FIXME: Shouldn&#39;t we need block height here?


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header | [tcm.protobuf.Header](#tcm-protobuf-Header) |  | Message Header Contains api version, message info string, sender &amp; receiver wallet addresses |
| network_fee | [int64](#int64) |  | This should be in nCAM, better readability and also we can use integer |
| currency | [string](#string) |  | Do we need this? Isn&#39;t the network fee always in CAM/nCAM? |





 

 

 

 



<a name="tcm_messages_ping-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/messages/ping.proto

<figure>
<img class="zoom" src="/img/ping.proto.dot.svg"/>
<figcaption align = "center"><b>Fig.3:</b> Ping Messages</figcaption>
</figure>



<a name="tcm-messages-PingRequest"></a>

### PingRequest
FIXME: IMO, Ping requests and reponses should include a timestamp?


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header | [tcm.protobuf.Header](#tcm-protobuf-Header) |  | Message Header Contains api version, message info string, sender &amp; receiver wallet addresses |
| ping_message | [string](#string) |  | Ping message |






<a name="tcm-messages-PingResponse"></a>

### PingResponse
FIXME: Ping request &amp; reponse messages looks same, do we need two different
messages?


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| header | [tcm.protobuf.Header](#tcm-protobuf-Header) |  | Message Header Contains api version, message info string, sender &amp; receiver wallet addresses |
| ping_message | [string](#string) |  | Ping message |





 

 

 

 



<a name="tcm_protobuf_coordinate-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/coordinate.proto



<a name="tcm-protobuf-Coordinate"></a>

### Coordinate
Coordinate


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| longitude | [double](#double) |  |  |
| latitude | [double](#double) |  |  |





 

 

 

 



<a name="tcm_protobuf_currency-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/currency.proto


 


<a name="tcm-protobuf-Currency"></a>

### Currency
## Currency list of ISO 4217 standard

### First 20 currencies are the most traded currencies in the world

This is done to optimize the size of the protobuf message

- List test
- Line 2
1. Sub Line 3 Lorem ipsum
2. Sub Line 4 Lorem ipsum
3. Sub Line 5 Lorem ipsum
- Back to first level

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Placeholder or unspecified currency |
| AUD | 1 | Australian dollar |
| BRL | 2 | Brazilian real |
| CAD | 3 | Canadian dollar |
| CHF | 4 | Swiss franc |
| CNY | 5 | Renminbi (China) |
| EUR | 6 | Euro |
| GBP | 7 | British pound |
| HKD | 8 | Hong Kong dollar |
| IDR | 9 | Indonesian rupiah |
| INR | 10 | Indian rupee |
| JPY | 11 | Japanese yen |
| KRW | 12 | South Korean won |
| MXN | 13 | Mexican peso |
| NOK | 14 | Norwegian krone |
| RUB | 15 | Russian ruble |
| SAR | 16 | Saudi riyal |
| SEK | 17 | Swedish krona |
| SGD | 18 | Singapore dollar |
| TRY | 19 | Turkish lira |
| USD | 20 | United States dollar |
| AED | 21 | United Arab Emirates dirham |
| AFN | 22 | Afghan afghani |
| ALL | 23 | Albanian lek |
| AMD | 24 | Armenian dram |
| ANG | 25 | Netherlands Antillean guilder |
| AOA | 26 | Angolan kwanza |
| ARS | 27 | Argentine peso |
| AWG | 28 | Aruban florin |
| AZN | 29 | Azerbaijani manat |
| BAM | 30 | Bosnia and Herzegovina convertible mark |
| BBD | 31 | Barbados dollar |
| BDT | 32 | Bangladeshi taka |
| BGN | 33 | Bulgarian lev |
| BHD | 34 | Bahraini dinar |
| BIF | 35 | Burundian franc |
| BMD | 36 | Bermudian dollar |
| BND | 37 | Brunei dollar |
| BOB | 38 | Bolivian boliviano |
| BSD | 39 | Bahamian dollar |
| BTN | 40 | Bhutanese ngultrum |
| BWP | 41 | Botswana pula |
| BYN | 42 | Belarusian ruble |
| BZD | 43 | Belize dollar |
| CDF | 44 | Congolese franc |
| CLP | 45 | Chilean peso |
| COP | 46 | Colombian peso |
| CRC | 47 | Costa Rican colón |
| CUC | 48 | Cuban convertible peso |
| CUP | 49 | Cuban peso |
| CVE | 50 | Cape Verdean escudo |
| CZK | 51 | Czech koruna |
| DJF | 52 | Djiboutian franc |
| DKK | 53 | Danish krone |
| DOP | 54 | Dominican peso |
| DZD | 55 | Algerian dinar |
| EGP | 56 | Egyptian pound |
| ERN | 57 | Eritrean nakfa |
| ETB | 58 | Ethiopian birr |
| FJD | 59 | Fijian dollar |
| FKP | 60 | Falkland Islands pound |
| GEL | 61 | Georgian lari |
| GHS | 62 | Ghanaian cedi |
| GIP | 63 | Gibraltar pound |
| GMD | 64 | Gambian dalasi |
| GNF | 65 | Guinean franc |
| GTQ | 66 | Guatemalan quetzal |
| GYD | 67 | Guyanese dollar |
| HNL | 68 | Honduran lempira |
| HRK | 69 | Croatian kuna |
| HTG | 70 | Haitian gourde |
| HUF | 71 | Hungarian forint |
| ILS | 72 | Israeli new shekel |
| IQD | 73 | Iraqi dinar |
| IRR | 74 | Iranian rial |
| ISK | 75 | Icelandic króna |
| JMD | 76 | Jamaican dollar |
| JOD | 77 | Jordanian dinar |
| KES | 78 | Kenyan shilling |
| KGS | 79 | Kyrgyzstani som |
| KHR | 80 | Cambodian riel |
| KMF | 81 | Comoro franc |
| KPW | 82 | North Korean won |
| KWD | 83 | Kuwaiti dinar |
| KYD | 84 | Cayman Islands dollar |
| KZT | 85 | Kazakhstani tenge |
| LAK | 86 | Lao kip |
| LBP | 87 | Lebanese pound |
| LKR | 88 | Sri Lanka rupee |
| LRD | 89 | Liberian dollar |
| LSL | 90 | Lesotho loti |
| LYD | 91 | Libyan dinar |
| MAD | 92 | Moroccan dirham |
| MDL | 93 | Moldovan leu |
| MGA | 94 | Malagasy ariary |
| MKD | 95 | Macedonian denar |
| MMK | 96 | Myanmar kyat |
| MNT | 97 | Mongolian tögrög |
| MOP | 98 | Macanese pataca |
| MRU | 99 | Mauritanian ouguiya |
| MUR | 100 | Mauritian rupee |
| MVR | 101 | Maldivian rufiyaa |
| MWK | 102 | Malawian kwacha |
| MYR | 103 | Malaysian ringgit |
| MZN | 104 | Mozambican metical |
| NAD | 105 | Namibian dollar |
| NGN | 106 | Nigerian naira |
| NIO | 107 | Nicaraguan córdoba |
| NPR | 108 | Nepalese rupee |
| NZD | 109 | New Zealand dollar |
| OMR | 110 | Omani rial |
| PAB | 111 | Panamanian balboa |
| PEN | 112 | Peruvian sol |
| PGK | 113 | Papua New Guinean kina |
| PHP | 114 | Philippine peso |
| PKR | 115 | Pakistani rupee |
| PLN | 116 | Polish złoty |
| PYG | 117 | Paraguayan guaraní |
| QAR | 118 | Qatari riyal |
| RON | 119 | Romanian leu |
| RSD | 120 | Serbian dinar |
| RWF | 121 | Rwandan franc |
| SBD | 122 | Solomon Islands dollar |
| SCR | 123 | Seychellois rupee |
| SDG | 124 | Sudanese pound |
| SHP | 125 | Saint Helena pound |
| SLL | 126 | Sierra Leonean leone |
| SOS | 127 | Somali shilling |
| SRD | 128 | Surinamese dollar |
| SSP | 129 | South Sudanese pound |
| STN | 130 | São Tomé and Príncipe dobra |
| SVC | 131 | Salvadoran colón |
| SYP | 132 | Syrian pound |
| SZL | 133 | Swazi lilangeni |
| THB | 134 | Thai baht |
| TJS | 135 | Tajikistani somoni |
| TMT | 136 | Turkmenistan manat |
| TND | 137 | Tunisian dinar |
| TOP | 138 | Tongan paʻanga |
| TTD | 139 | Trinidad and Tobago dollar |
| TWD | 140 | New Taiwan dollar |
| TZS | 141 | Tanzanian shilling |
| UAH | 142 | Ukrainian hryvnia |
| UGX | 143 | Ugandan shilling |
| UYU | 144 | Uruguayan peso |
| UZS | 145 | Uzbekistani soʻm |
| VND | 146 | Vietnamese đồng |
| VUV | 147 | Vanuatu vatu |
| WST | 148 | Samoan tālā |
| XAF | 149 | Central African CFA franc |
| XCD | 150 | East Caribbean dollar |
| XOF | 151 | West African CFA franc |
| XPF | 152 | CFP franc |
| YER | 153 | Yemeni rial |
| ZAR | 154 | South African rand |
| ZMW | 155 | Zambian kwacha |


 

 

 



<a name="tcm_protobuf_date-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/date.proto



<a name="tcm-protobuf-Date"></a>

### Date
# Date Message

--- START MARKDOWN TEST ---

# Markdown Features

## Headers

# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6

## Text Emphasis

Italic* or _Italic_

*Bold** or __Bold__

*_Bold and Italic_** or ***Bold and Italic***

~~Strikethrough~~

## Lists

### Unordered
Does not work with asterisk (*) and also seems like sub lists are not supported.

- Item 1
- Item 2
- Sub-item 2.1
- Sub-item 2.2

### Ordered
1. First item
2. Second item
3. Third item

## Links

[Chain4Travel AG](https://chain4travel.com//)

## Images

![C4TxHexens](https://api.strapi.camino.network//uploads/22976_c_0_0_1200_675_w_800_h_450_49e8683ec1.webp)

## Blockquotes

&gt; This is a blockquote.

## Inline Code

Here is `inline code`.

## Code Blocks

```python
print(&#34;Hello, World!&#34;)
```

## Tables

| Header 1 | Header 2 |
|----------|----------|
| Row1Col1 | Row1Col2 |
| Row2Col1 | Row2Col2 |

## Horizontal Rule

---

## Task Lists

- [x] Completed task
- [ ] Incomplete task

## Line Breaks

First line.
Second line.

--- END MARKDOWN TEST ---


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| year | [int32](#int32) |  |  |
| month | [int32](#int32) |  |  |
| day | [int32](#int32) |  |  |





 

 

 

 



<a name="tcm_protobuf_distance-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/distance.proto



<a name="tcm-protobuf-Distance"></a>

### Distance
Distance with unit


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| value | [int32](#int32) |  |  |
| distance_unit | [DistanceUnit](#tcm-protobuf-DistanceUnit) |  |  |





 


<a name="tcm-protobuf-DistanceUnit"></a>

### DistanceUnit
Distance Unit

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNSPECIFIED | 0 |  |
| METERS | 1 |  |
| KILOMETERS | 2 |  |
| MILES | 3 |  |
| FEET | 4 |  |


 

 

 



<a name="tcm_protobuf_filter-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/filter.proto



<a name="tcm-protobuf-Filter"></a>

### Filter
Filter


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| filter_code | [string](#string) |  |  |
| filter_description | [string](#string) |  |  |
| drv_globaltypes | [string](#string) | repeated | FIXME: How many global types are there? Can this be an enum? |





 

 

 

 



<a name="tcm_protobuf_geo_location-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/geo_location.proto



<a name="tcm-protobuf-GeoCircle"></a>

### GeoCircle
Geo Circle


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| center | [Coordinate](#tcm-protobuf-Coordinate) |  |  |
| radius | [Distance](#tcm-protobuf-Distance) |  |  |






<a name="tcm-protobuf-GeoLocation"></a>

### GeoLocation
Geo Location Message
Describes a geo location with location codes, geo circle, geo polygon, and
geo tree.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| location_codes | [LocationCodes](#tcm-protobuf-LocationCodes) |  |  |
| geo_circle | [GeoCircle](#tcm-protobuf-GeoCircle) |  |  |
| geo_polygon | [GeoPolygon](#tcm-protobuf-GeoPolygon) |  |  |
| geo_tree | [GeoTree](#tcm-protobuf-GeoTree) |  |  |






<a name="tcm-protobuf-GeoPolygon"></a>

### GeoPolygon
Geo Polygon


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| points | [Coordinate](#tcm-protobuf-Coordinate) | repeated | GPS points of the polygon |






<a name="tcm-protobuf-GeoTree"></a>

### GeoTree
Geo Tree


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| country | [string](#string) |  |  |
| region | [string](#string) |  |  |
| city_or_resort | [string](#string) |  |  |






<a name="tcm-protobuf-LocationCodes"></a>

### LocationCodes
Location Codes


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| location_codes | [string](#string) | repeated | List of location codes |





 

 

 

 



<a name="tcm_protobuf_holiday_home-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/holiday_home.proto



<a name="tcm-protobuf-HolidayHome"></a>

### HolidayHome
Holiday Home


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| rate_plan | [string](#string) |  |  |
| travel_period | [TravelPeriod](#tcm-protobuf-TravelPeriod) |  | Travel period |
| travellers | [Traveller](#tcm-protobuf-Traveller) | repeated | Travellers |





 

 

 

 



<a name="tcm_protobuf_tcm_message-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/tcm_message.proto



<a name="tcm-protobuf-Header"></a>

### Header
TCM Message Header

FIXME: Using version as a single int32 seems logical in my opinion. Less size
and simple.
FIXME: Do we really need the &#34;info&#34; field?


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| version | [int32](#int32) |  | API Version |
| info | [string](#string) |  | Message info FIXME: This field was named as &#34;title&#34; in initial json files. |
| sender | [string](#string) |  | The requestor&#39;s wallet address |
| receiver | [string](#string) | repeated | Receiver wallet addresses FIXME: How does the multiple receiver wallet&#39;s work? |





 

 

 

 



<a name="tcm_protobuf_travel_period-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/travel_period.proto



<a name="tcm-protobuf-TravelPeriod"></a>

### TravelPeriod
Travel Period


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| start_date | [Date](#tcm-protobuf-Date) |  |  |
| end_date | [Date](#tcm-protobuf-Date) |  |  |
| flexible | [bool](#bool) |  | FIXME: Boolean? |
| los_from_nights | [int32](#int32) |  |  |
| los_to_nights | [int32](#int32) |  |  |





 

 

 

 



<a name="tcm_protobuf_traveller-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## tcm/protobuf/traveller.proto



<a name="tcm-protobuf-Traveller"></a>

### Traveller
Traveller


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [TravellerType](#tcm-protobuf-TravellerType) |  | Traveller type from enum below |
| age | [int32](#int32) |  | Age FIXME: Do we need both age &amp; birthdate? (Protobuf fields are optional, so we can keep it also) |
| birthdate | [Date](#tcm-protobuf-Date) |  | Birthdate |
| nationality | [string](#string) |  | FIXME: An enum for this field will reduce the message size. |





 


<a name="tcm-protobuf-TravellerType"></a>

### TravellerType
Traveller Type

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNSPECIFIED_T | 0 |  |
| ADULT | 1 |  |
| CHILD | 2 |  |
| INFANT | 3 |  |
| SENIOR | 4 |  |


 

 

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

