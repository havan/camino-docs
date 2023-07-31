---
sidebar_position: 4
title: TCM Messages
description: Touristic Cryptographic Messenger (TCM) Messages
---

# TCM Messages

## helloWorld

### Example Request JSON

```json
{
  "fromPublicKey": "1234",
  "toPublicKey": "5678",
  "message": "Hello World"
}
```

### Example Schema Protobuff

```bash
syntax = "proto3";
message HelloWorld {
	string fromPublicKey = 1;
	string toPublicKey = 2;
	string message = 3;
}
```

### Example Response

```json
{
  "fromPublicKey": "5678",
  "toPublicKey": "1234",
  "message": "Hello World received"
}
```

## distributor.search.hotelSearch

### Example Request JSON

```json
{
  "openapi": "3.0.1",
  "info": {
    "title": "Hotel search request",
    "version": "v1"
  },
  "paths": "/distributor/search",
  "publicKeySender": "X-camino1qa7tak7x342atlktum3v3s6634hnq20lh526kq",
  "hotelSearchRequest": {
    "enrichment": "none",
    "currency": "EUR",
    "language": "de",
    "market": "german",
    "location": {
      "code": ["AESPMI1234", "AESPMI5678", "AESPMI9999"],
      "geoCircle": {
        "center": {
          "longitude": "12.493336",
          "latitude": "41.889957"
        },
        "radius": "3000",
        "radiusUnit": "meters"
      },
      "geoPolygon": {
        "points": [
          {
            "index": "1",
            "longitude": "13.91591",
            "latitude": "34.52034"
          },
          {
            "index": "2",
            "longitude": "13.91581",
            "latitude": "34.52024"
          },
          {
            "index": "3",
            "longitude": "13.91571",
            "latitude": "34.52014"
          },
          {
            "index": "4",
            "longitude": "13.91561",
            "latitude": "34.52004"
          }
        ]
      },
      "country": "Spain",
      "region": "Mallorca",
      "cityOrResort": "Palma"
    },
    "freetext": "",
    "speachRequest": "",
    "rooms": [
      {
        "id": "1",
        "room": "RMSDDBSV00",
        "ratePlan": "P0R00",
        "travelPeriod": {
          "startDate": "01-05-2023",
          "endDate": "30-06-2023",
          "flexible": "yes",
          "losFromNights": "7",
          "losToNights": "10"
        },
        "travellers": {
          "nationality": "german",
          "adults": "2",
          "children": "2",
          "ages": ["9", "6"]
        }
      }
    ]
  }
}
```

### JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2019-09/schema",
  "$id": "http://example.com/example.json",
  "type": "object",
  "default": {},
  "title": "Root Schema",
  "required": [
    "openapi",
    "info",
    "paths",
    "publicKeySender",
    "hotelSearchRequest"
  ],
  "properties": {
    "openapi": {
      "type": "string",
      "default": "",
      "title": "The openapi Schema",
      "examples": ["3.0.1"]
    },
    "info": {
      "type": "object",
      "default": {},
      "title": "The info Schema",
      "required": ["title", "version"],
      "properties": {
        "title": {
          "type": "string",
          "default": "",
          "title": "The title Schema",
          "examples": ["Hotel search request"]
        },
        "version": {
          "type": "string",
          "default": "",
          "title": "The version Schema",
          "examples": ["v1"]
        }
      },
      "examples": [
        {
          "title": "Hotel search request",
          "version": "v1"
        }
      ]
    },
    "paths": {
      "type": "string",
      "default": "",
      "title": "The paths Schema",
      "examples": ["/distributor/search"]
    },
    "publicKeySender": {
      "type": "string",
      "default": "",
      "title": "The publicKeySender Schema",
      "examples": ["X-camino1qa7tak7x342atlktum3v3s6634hnq20lh526kq"]
    },
    "hotelSearchRequest": {
      "type": "object",
      "default": {},
      "title": "The hotelSearchRequest Schema",
      "required": [
        "enrichment",
        "currency",
        "language",
        "market",
        "location",
        "freetext",
        "speachRequest",
        "rooms"
      ],
      "properties": {
        "enrichment": {
          "type": "string",
          "default": "",
          "title": "The enrichment Schema",
          "examples": ["none"]
        },
        "currency": {
          "type": "string",
          "default": "",
          "title": "The currency Schema",
          "examples": ["EUR"]
        },
        "language": {
          "type": "string",
          "default": "",
          "title": "The language Schema",
          "examples": ["de"]
        },
        "market": {
          "type": "string",
          "default": "",
          "title": "The market Schema",
          "examples": ["german"]
        },
        "location": {
          "type": "object",
          "default": {},
          "title": "The location Schema",
          "required": [
            "code",
            "geoCircle",
            "geoPolygon",
            "country",
            "region",
            "cityOrResort"
          ],
          "properties": {
            "code": {
              "type": "array",
              "default": [],
              "title": "The code Schema",
              "items": {
                "type": "string",
                "title": "A Schema",
                "examples": ["AESPMI1234", "AESPMI5678", "AESPMI9999"]
              },
              "examples": [["AESPMI1234", "AESPMI5678", "AESPMI9999"]]
            },
            "geoCircle": {
              "type": "object",
              "default": {},
              "title": "The geoCircle Schema",
              "required": ["center", "radius", "radiusUnit"],
              "properties": {
                "center": {
                  "type": "object",
                  "default": {},
                  "title": "The center Schema",
                  "required": ["longitude", "latitude"],
                  "properties": {
                    "longitude": {
                      "type": "string",
                      "default": "",
                      "title": "The longitude Schema",
                      "examples": ["12.493336"]
                    },
                    "latitude": {
                      "type": "string",
                      "default": "",
                      "title": "The latitude Schema",
                      "examples": ["41.889957"]
                    }
                  },
                  "examples": [
                    {
                      "longitude": "12.493336",
                      "latitude": "41.889957"
                    }
                  ]
                },
                "radius": {
                  "type": "string",
                  "default": "",
                  "title": "The radius Schema",
                  "examples": ["3000"]
                },
                "radiusUnit": {
                  "type": "string",
                  "default": "",
                  "title": "The radiusUnit Schema",
                  "examples": ["meters"]
                }
              },
              "examples": [
                {
                  "center": {
                    "longitude": "12.493336",
                    "latitude": "41.889957"
                  },
                  "radius": "3000",
                  "radiusUnit": "meters"
                }
              ]
            },
            "geoPolygon": {
              "type": "object",
              "default": {},
              "title": "The geoPolygon Schema",
              "required": ["points"],
              "properties": {
                "points": {
                  "type": "array",
                  "default": [],
                  "title": "The points Schema",
                  "items": {
                    "type": "object",
                    "title": "A Schema",
                    "required": ["index", "longitude", "latitude"],
                    "properties": {
                      "index": {
                        "type": "string",
                        "title": "The index Schema",
                        "examples": ["1", "2", "3", "4"]
                      },
                      "longitude": {
                        "type": "string",
                        "title": "The longitude Schema",
                        "examples": [
                          "13.91591",
                          "13.91581",
                          "13.91571",
                          "13.91561"
                        ]
                      },
                      "latitude": {
                        "type": "string",
                        "title": "The latitude Schema",
                        "examples": [
                          "34.52034",
                          "34.52024",
                          "34.52014",
                          "34.52004"
                        ]
                      }
                    },
                    "examples": [
                      {
                        "index": "1",
                        "longitude": "13.91591",
                        "latitude": "34.52034"
                      },
                      {
                        "index": "2",
                        "longitude": "13.91581",
                        "latitude": "34.52024"
                      },
                      {
                        "index": "3",
                        "longitude": "13.91571",
                        "latitude": "34.52014"
                      },
                      {
                        "index": "4",
                        "longitude": "13.91561",
                        "latitude": "34.52004"
                      }
                    ]
                  },
                  "examples": [
                    [
                      {
                        "index": "1",
                        "longitude": "13.91591",
                        "latitude": "34.52034"
                      },
                      {
                        "index": "2",
                        "longitude": "13.91581",
                        "latitude": "34.52024"
                      },
                      {
                        "index": "3",
                        "longitude": "13.91571",
                        "latitude": "34.52014"
                      },
                      {
                        "index": "4",
                        "longitude": "13.91561",
                        "latitude": "34.52004"
                      }
                    ]
                  ]
                }
              },
              "examples": [
                {
                  "points": [
                    {
                      "index": "1",
                      "longitude": "13.91591",
                      "latitude": "34.52034"
                    },
                    {
                      "index": "2",
                      "longitude": "13.91581",
                      "latitude": "34.52024"
                    },
                    {
                      "index": "3",
                      "longitude": "13.91571",
                      "latitude": "34.52014"
                    },
                    {
                      "index": "4",
                      "longitude": "13.91561",
                      "latitude": "34.52004"
                    }
                  ]
                }
              ]
            },
            "country": {
              "type": "string",
              "default": "",
              "title": "The country Schema",
              "examples": ["Spain"]
            },
            "region": {
              "type": "string",
              "default": "",
              "title": "The region Schema",
              "examples": ["Mallorca"]
            },
            "cityOrResort": {
              "type": "string",
              "default": "",
              "title": "The cityOrResort Schema",
              "examples": ["Palma"]
            }
          },
          "examples": [
            {
              "code": ["AESPMI1234", "AESPMI5678", "AESPMI9999"],
              "geoCircle": {
                "center": {
                  "longitude": "12.493336",
                  "latitude": "41.889957"
                },
                "radius": "3000",
                "radiusUnit": "meters"
              },
              "geoPolygon": {
                "points": [
                  {
                    "index": "1",
                    "longitude": "13.91591",
                    "latitude": "34.52034"
                  },
                  {
                    "index": "2",
                    "longitude": "13.91581",
                    "latitude": "34.52024"
                  },
                  {
                    "index": "3",
                    "longitude": "13.91571",
                    "latitude": "34.52014"
                  },
                  {
                    "index": "4",
                    "longitude": "13.91561",
                    "latitude": "34.52004"
                  }
                ]
              },
              "country": "Spain",
              "region": "Mallorca",
              "cityOrResort": "Palma"
            }
          ]
        },
        "freetext": {
          "type": "string",
          "default": "",
          "title": "The freetext Schema",
          "examples": [""]
        },
        "speachRequest": {
          "type": "string",
          "default": "",
          "title": "The speachRequest Schema",
          "examples": [""]
        },
        "rooms": {
          "type": "array",
          "default": [],
          "title": "The rooms Schema",
          "items": {
            "type": "object",
            "default": {},
            "title": "A Schema",
            "required": [
              "id",
              "room",
              "ratePlan",
              "travelPeriod",
              "travellers"
            ],
            "properties": {
              "id": {
                "type": "string",
                "default": "",
                "title": "The id Schema",
                "examples": ["1"]
              },
              "room": {
                "type": "string",
                "default": "",
                "title": "The room Schema",
                "examples": ["RMSDDBSV00"]
              },
              "ratePlan": {
                "type": "string",
                "default": "",
                "title": "The ratePlan Schema",
                "examples": ["P0R00"]
              },
              "travelPeriod": {
                "type": "object",
                "default": {},
                "title": "The travelPeriod Schema",
                "required": [
                  "startDate",
                  "endDate",
                  "flexible",
                  "losFromNights",
                  "losToNights"
                ],
                "properties": {
                  "startDate": {
                    "type": "string",
                    "default": "",
                    "title": "The startDate Schema",
                    "examples": ["01-05-2023"]
                  },
                  "endDate": {
                    "type": "string",
                    "default": "",
                    "title": "The endDate Schema",
                    "examples": ["30-06-2023"]
                  },
                  "flexible": {
                    "type": "string",
                    "default": "",
                    "title": "The flexible Schema",
                    "examples": ["yes"]
                  },
                  "losFromNights": {
                    "type": "string",
                    "default": "",
                    "title": "The losFromNights Schema",
                    "examples": ["7"]
                  },
                  "losToNights": {
                    "type": "string",
                    "default": "",
                    "title": "The losToNights Schema",
                    "examples": ["10"]
                  }
                },
                "examples": [
                  {
                    "startDate": "01-05-2023",
                    "endDate": "30-06-2023",
                    "flexible": "yes",
                    "losFromNights": "7",
                    "losToNights": "10"
                  }
                ]
              },
              "travellers": {
                "type": "object",
                "default": {},
                "title": "The travellers Schema",
                "required": ["nationality", "adults", "children", "ages"],
                "properties": {
                  "nationality": {
                    "type": "string",
                    "default": "",
                    "title": "The nationality Schema",
                    "examples": ["german"]
                  },
                  "adults": {
                    "type": "string",
                    "default": "",
                    "title": "The adults Schema",
                    "examples": ["2"]
                  },
                  "children": {
                    "type": "string",
                    "default": "",
                    "title": "The children Schema",
                    "examples": ["2"]
                  },
                  "ages": {
                    "type": "array",
                    "default": [],
                    "title": "The ages Schema",
                    "items": {
                      "type": "string",
                      "title": "A Schema",
                      "examples": ["9", "6"]
                    },
                    "examples": [["9", "6"]]
                  }
                },
                "examples": [
                  {
                    "nationality": "german",
                    "adults": "2",
                    "children": "2",
                    "ages": ["9", "6"]
                  }
                ]
              }
            },
            "examples": [
              {
                "id": "1",
                "room": "RMSDDBSV00",
                "ratePlan": "P0R00",
                "travelPeriod": {
                  "startDate": "01-05-2023",
                  "endDate": "30-06-2023",
                  "flexible": "yes",
                  "losFromNights": "7",
                  "losToNights": "10"
                },
                "travellers": {
                  "nationality": "german",
                  "adults": "2",
                  "children": "2",
                  "ages": ["9", "6"]
                }
              }
            ]
          },
          "examples": [
            [
              {
                "id": "1",
                "room": "RMSDDBSV00",
                "ratePlan": "P0R00",
                "travelPeriod": {
                  "startDate": "01-05-2023",
                  "endDate": "30-06-2023",
                  "flexible": "yes",
                  "losFromNights": "7",
                  "losToNights": "10"
                },
                "travellers": {
                  "nationality": "german",
                  "adults": "2",
                  "children": "2",
                  "ages": ["9", "6"]
                }
              }
            ]
          ]
        }
      },
      "examples": [
        {
          "enrichment": "none",
          "currency": "EUR",
          "language": "de",
          "market": "german",
          "location": {
            "code": ["AESPMI1234", "AESPMI5678", "AESPMI9999"],
            "geoCircle": {
              "center": {
                "longitude": "12.493336",
                "latitude": "41.889957"
              },
              "radius": "3000",
              "radiusUnit": "meters"
            },
            "geoPolygon": {
              "points": [
                {
                  "index": "1",
                  "longitude": "13.91591",
                  "latitude": "34.52034"
                },
                {
                  "index": "2",
                  "longitude": "13.91581",
                  "latitude": "34.52024"
                },
                {
                  "index": "3",
                  "longitude": "13.91571",
                  "latitude": "34.52014"
                },
                {
                  "index": "4",
                  "longitude": "13.91561",
                  "latitude": "34.52004"
                }
              ]
            },
            "country": "Spain",
            "region": "Mallorca",
            "cityOrResort": "Palma"
          },
          "freetext": "",
          "speachRequest": "",
          "rooms": [
            {
              "id": "1",
              "room": "RMSDDBSV00",
              "ratePlan": "P0R00",
              "travelPeriod": {
                "startDate": "01-05-2023",
                "endDate": "30-06-2023",
                "flexible": "yes",
                "losFromNights": "7",
                "losToNights": "10"
              },
              "travellers": {
                "nationality": "german",
                "adults": "2",
                "children": "2",
                "ages": ["9", "6"]
              }
            }
          ]
        }
      ]
    }
  },
  "examples": [
    {
      "openapi": "3.0.1",
      "info": {
        "title": "Hotel search request",
        "version": "v1"
      },
      "paths": "/distributor/search",
      "publicKeySender": "X-camino1qa7tak7x342atlktum3v3s6634hnq20lh526kq",
      "hotelSearchRequest": {
        "enrichment": "none",
        "currency": "EUR",
        "language": "de",
        "market": "german",
        "location": {
          "code": ["AESPMI1234", "AESPMI5678", "AESPMI9999"],
          "geoCircle": {
            "center": {
              "longitude": "12.493336",
              "latitude": "41.889957"
            },
            "radius": "3000",
            "radiusUnit": "meters"
          },
          "geoPolygon": {
            "points": [
              {
                "index": "1",
                "longitude": "13.91591",
                "latitude": "34.52034"
              },
              {
                "index": "2",
                "longitude": "13.91581",
                "latitude": "34.52024"
              },
              {
                "index": "3",
                "longitude": "13.91571",
                "latitude": "34.52014"
              },
              {
                "index": "4",
                "longitude": "13.91561",
                "latitude": "34.52004"
              }
            ]
          },
          "country": "Spain",
          "region": "Mallorca",
          "cityOrResort": "Palma"
        },
        "freetext": "",
        "speachRequest": "",
        "rooms": [
          {
            "id": "1",
            "room": "RMSDDBSV00",
            "ratePlan": "P0R00",
            "travelPeriod": {
              "startDate": "01-05-2023",
              "endDate": "30-06-2023",
              "flexible": "yes",
              "losFromNights": "7",
              "losToNights": "10"
            },
            "travellers": {
              "nationality": "german",
              "adults": "2",
              "children": "2",
              "ages": ["9", "6"]
            }
          }
        ]
      }
    }
  ]
}
```

### Protobuff Schema

```
syntax = "proto3";

message SomeMessage {

    message Info {
        string title = 1;
        string version = 2;
    }

    message Center {
        string longitude = 1;
        string latitude = 2;
    }

    message Geocircle {
        Center center = 1;
        string radius = 2;
        string radiusUnit = 3;
    }

    message Points {
        string index = 1;
        string longitude = 2;
        string latitude = 3;
    }

    message Geopolygon {
        repeated Points points = 1;
    }

    message Location {
        repeated string code = 1;
        Geocircle geoCircle = 2;
        Geopolygon geoPolygon = 3;
        string country = 4;
        string region = 5;
        string cityOrResort = 6;
    }

    message Travelperiod {
        string startDate = 1;
        string endDate = 2;
        string flexible = 3;
        string losFromNights = 4;
        string losToNights = 5;
    }

    message Travellers {
        string nationality = 1;
        string adults = 2;
        string children = 3;
        repeated string ages = 4;
    }

    message Rooms {
        string id = 1;
        string room = 2;
        string ratePlan = 3;
        Travelperiod travelPeriod = 4;
        Travellers travellers = 5;
    }

    message Hotelsearchrequest {
        string enrichment = 1;
        string currency = 2;
        string language = 3;
        string market = 4;
        Location location = 5;
        string freetext = 6;
        string speachRequest = 7;
        repeated Rooms rooms = 8;
    }

    string openapi = 1;
    Info info = 2;
    string paths = 3;
    string publicKeySender = 4;
    Hotelsearchrequest hotelSearchRequest = 5;
}
```

### Example Response

```
{
	...
}
```
