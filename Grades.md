## Grades

### Enrolled school years `GET /rest/v1/plaatsingen?[studentid]?`
<details><summary>Click to open</summary>
Fetches the school years the user is and was enrolled in. [studentid] is the student id.

#### Parameters

| Name          | Type      | Value                           |
|---------------|-----------|---------------------------------|
| Authorization | Header    | Bearer [access_token]           |
| leerling      | Parameter | [studentid]                     |
#### Returns
```json
{
    "items": [
        {
            "$type": "plaatsing.RPlaatsing",
            "links": [
                {
                    "id": 1234,
                    "rel": "self",
                    "type": "plaatsing.RPlaatsing",
                    "href": "https://api.somtoday.nl/rest/v1/plaatsingen/1234"
                }
            ],
            "permissions": [
                {
                    "full": "plaatsing.RPlaatsing:READ:INSTANCE(1234)",
                    "type": "plaatsing.RPlaatsing",
                    "operations": [
                        "READ"
                    ],
                    "instances": [
                        "INSTANCE(1234)"
                    ]
                }
            ],
            "additionalObjects": {},
            "UUID": "00000000-0000-0000-0000-000000000000",
            "vanafDatum": "2026-08-01",
            "totDatum": "2027-07-31",
            "leerling": {
                "links": [
                    {
                        "id": 1234,
                        "rel": "self",
                        "type": "leerling.RLeerlingPrimer",
                        "href": "https://api.somtoday.nl/rest/v1/leerlingen/1234"
                    }
                ],
                "permissions": [
                    {
                        "full": "leerling.RLeerlingPrimer:READ:INSTANCE(1234)",
                        "type": "leerling.RLeerlingPrimer",
                        "operations": [
                            "READ"
                        ],
                        "instances": [
                            "INSTANCE(1234)"
                        ]
                    }
                ],
                "additionalObjects": {},
                "UUID": "00000000-0000-0000-0000-000000000000",
                "leerlingnummer": 402638,
                "roepnaam": "Lenn",
                "achternaam": "Steenbergen",
                "pasfotoUrl": "https://api.somtoday.nl/rest/v1/pasfoto/0792a6e2-9833-45e8-b1eb-1498cf22f10d/AbC123dEf256gHi7890AbC123dEf256g"
            },
            "huidig": true,
            "stamgroepnaam": "h5c",
            "opleidingsnaam": "HAVO-EM",
            "leerjaar": 5,
            "schooljaar": {
                "$type": "onderwijsinrichting.RSchooljaar",
                "links": [
                    {
                        "id": 1234,
                        "rel": "self",
                        "type": "onderwijsinrichting.RSchooljaar",
                        "href": "https://api.somtoday.nl/rest/v1/schooljaren/1234"
                    }
                ],
                "permissions": [
                    {
                        "full": "onderwijsinrichting.RSchooljaar:READ:INSTANCE(1234)",
                        "type": "onderwijsinrichting.RSchooljaar",
                        "operations": [
                            "READ"
                        ],
                        "instances": [
                            "INSTANCE(1234)"
                        ]
                    }
                ],
                "additionalObjects": {},
                "naam": "2026/2027",
                "vanafDatum": "2026-08-01",
                "totDatum": "2027-07-31",
                "isHuidig": true
            },
            "vestiging": {
                "links": [
                    {
                        "id": 1234,
                        "rel": "self",
                        "type": "instelling.RVestiging",
                        "href": "https://api.somtoday.nl/rest/v1/vestigingen/1234"
                    }
                ],
                "permissions": [
                    {
                        "full": "instelling.RVestiging:READ:INSTANCE(1234)",
                        "type": "instelling.RVestiging",
                        "operations": [
                            "READ"
                        ],
                        "instances": [
                            "INSTANCE(1234)"
                        ]
                    }
                ],
                "additionalObjects": {},
                "naam": "Christelijk Lyceum",
                "UUID": "00000000-0000-0000-0000-000000000000",
                "uuid": "00000000-0000-0000-0000-000000000000"
            }
        }
    },
    ...
}
```
</details>


### Averages `GET /rest/v1/vakkeuzes/plaatsing/[id]/vakgemiddelden`
<details><summary>Click to open</summary>
Fetches the average grades of the student. [id] can be gotten from `GET /rest/v1/plaatsingen`

#### Parameters

| Name          | Type      | Value                           |
|---------------|-----------|---------------------------------|
| id            | URL       | [plaatsing id]                  |
| Authorization | Header    | Bearer [access_token]           |

#### Returns
```json
{
  "items": [       
         {
            "$type": "resultaten.RLeerlingVakGemiddelde",
            "vakkeuze": {
                "links": [
                    {
                        "id": 1234,
                        "rel": "self",
                        "type": "onderwijsinrichting.RVakkeuze",
                        "href": "https://api.somtoday.nl/rest/v1/vakkeuzes/1234"
                    }
                ],
                "permissions": [
                    {
                        "full": "onderwijsinrichting.RVakkeuze:READ:INSTANCE(1234)",
                        "type": "onderwijsinrichting.RVakkeuze",
                        "operations": [
                            "READ"
                        ],
                        "instances": [
                            "INSTANCE(1234)"
                        ]
                    }
                ],
                "additionalObjects": {},
                "vak": {
                    "links": [
                        {
                            "id": 1234,
                            "rel": "self",
                            "type": "onderwijsinrichting.RVak",
                            "href": "https://api.somtoday.nl/rest/v1/vakken/1234"
                        }
                    ],
                    "permissions": [
                        {
                            "full": "onderwijsinrichting.RVak:READ:INSTANCE(1234)",
                            "type": "onderwijsinrichting.RVak",
                            "operations": [
                                "READ"
                            ],
                            "instances": [
                                "INSTANCE(1234)"
                            ]
                        }
                    ],
                    "additionalObjects": {},
                    "afkorting": "cchavo",
                    "naam": "Combinatiecijfer HAVO",
                    "UUID": "0000000-0000-0000-0000-000000000000"
                },
                "leerling": {
                    "links": [
                        {
                            "id": 1234,
                            "rel": "self",
                            "type": "leerling.RLeerlingPrimer",
                            "href": "https://api.somtoday.nl/rest/v1/leerlingen/1234"
                        }
                    ],
                    "permissions": [
                        {
                            "full": "leerling.RLeerling:READ:INSTANCE(1234)",
                            "type": "leerling.RLeerling",
                            "operations": [
                                "READ"
                            ],
                            "instances": [
                                "INSTANCE(1234)"
                            ]
                        }
                    ],
                    "additionalObjects": {},
                    "UUID": "0000000-0000-0000-0000-000000000000",
                    "leerlingnummer": 402638,
                    "roepnaam": "Lenn",
                    "achternaam": "Steenbergen",
                    "pasfotoUrl": "https://api.somtoday.nl/rest/v1/pasfoto/0792a6e2-9833-45e8-b1eb-1498cf22f10d/AbC123dEf256gHi7890AbC123dEf256g"
                },
                "vrijstelling": false,
                "lichting": {
                    "$type": "onderwijsinrichting.RLichting",
                    "links": [
                        {
                            "id": 12345678901234,
                            "rel": "self",
                            "type": "onderwijsinrichting.RLichting",
                            "href": "https://api.somtoday.nl/rest/v1/lichtingen/12345678901234"
                        }
                    ],
                    "permissions": [
                        {
                            "full": "onderwijsinrichting.RLichting:READ:INSTANCE(12345678901234)",
                            "type": "onderwijsinrichting.RLichting",
                            "operations": [
                                "READ"
                            ],
                            "instances": [
                                "INSTANCE(12345678901234)"
                            ]
                        }
                    ],
                    "additionalObjects": {},
                    "naam": "HAVO 2025-2027",
                    "lichtingSchooljaren": [
                        {
                            "$type": "onderwijsinrichting.RLichtingSchooljaar",
                            "links": [
                                {
                                    "id": 14117081943561,
                                    "rel": "koppeling",
                                    "type": "onderwijsinrichting.RLichtingSchooljaar"
                                }
                            ],
                            "permissions": [],
                            "additionalObjects": {},
                            "schooljaar": {
                                "$type": "onderwijsinrichting.RSchooljaar",
                                "links": [
                                    {
                                        "id": 1234,
                                        "rel": "self",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "href": "https://api.somtoday.nl/rest/v1/schooljaren/1234"
                                    }
                                ],
                                "permissions": [
                                    {
                                        "full": "onderwijsinrichting.RSchooljaar:READ:INSTANCE(1234)",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "operations": [
                                            "READ"
                                        ],
                                        "instances": [
                                            "INSTANCE(1234)"
                                        ]
                                    }
                                ],
                                "additionalObjects": {},
                                "naam": "2025/2026",
                                "vanafDatum": "2025-08-01",
                                "totDatum": "2026-07-31",
                                "isHuidig": false
                            },
                            "leerjaar": 4,
                            "heeftExamendossier": true
                        },
                        {
                            "$type": "onderwijsinrichting.RLichtingSchooljaar",
                            "links": [
                                {
                                    "id": 14117081943562,
                                    "rel": "koppeling",
                                    "type": "onderwijsinrichting.RLichtingSchooljaar"
                                }
                            ],
                            "permissions": [],
                            "additionalObjects": {},
                            "schooljaar": {
                                "$type": "onderwijsinrichting.RSchooljaar",
                                "links": [
                                    {
                                        "id": 1234,
                                        "rel": "self",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "href": "https://api.somtoday.nl/rest/v1/schooljaren/1234"
                                    }
                                ],
                                "permissions": [
                                    {
                                        "full": "onderwijsinrichting.RSchooljaar:READ:INSTANCE(1234)",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "operations": [
                                            "READ"
                                        ],
                                        "instances": [
                                            "INSTANCE(1234)"
                                        ]
                                    }
                                ],
                                "additionalObjects": {},
                                "naam": "2026/2027",
                                "vanafDatum": "2026-08-01",
                                "totDatum": "2027-07-31",
                                "isHuidig": true
                            },
                            "leerjaar": 5,
                            "heeftExamendossier": true
                        }
                    ],
                    "onderwijssoort": {
                        "$type": "onderwijsinrichting.ROnderwijssoort",
                        "links": [
                            {
                                "id": 30516287,
                                "rel": "koppeling",
                                "type": "onderwijsinrichting.ROnderwijssoort"
                            }
                        ],
                        "permissions": [],
                        "additionalObjects": {},
                        "afkorting": "HAVO",
                        "isOnderbouw": false
                    },
                    "UUID": "0000000-0000-0000-0000-00000000"
                },
                "relevanteCijferLichting": {
                    "$type": "onderwijsinrichting.RLichting",
                    "links": [
                        {
                            "id": 12345678901234,
                            "rel": "self",
                            "type": "onderwijsinrichting.RLichting",
                            "href": "https://api.somtoday.nl/rest/v1/lichtingen/12345678901234"
                        }
                    ],
                    "permissions": [
                        {
                            "full": "onderwijsinrichting.RLichting:READ:INSTANCE(12345678901234)",
                            "type": "onderwijsinrichting.RLichting",
                            "operations": [
                                "READ"
                            ],
                            "instances": [
                                "INSTANCE(12345678901234)"
                            ]
                        }
                    ],
                    "additionalObjects": {},
                    "naam": "HAVO 2025-2027",
                    "lichtingSchooljaren": [
                        {
                            "$type": "onderwijsinrichting.RLichtingSchooljaar",
                            "links": [
                                {
                                    "id": 14117081943561,
                                    "rel": "koppeling",
                                    "type": "onderwijsinrichting.RLichtingSchooljaar"
                                }
                            ],
                            "permissions": [],
                            "additionalObjects": {},
                            "schooljaar": {
                                "$type": "onderwijsinrichting.RSchooljaar",
                                "links": [
                                    {
                                        "id": 1234,
                                        "rel": "self",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "href": "https://api.somtoday.nl/rest/v1/schooljaren/1234"
                                    }
                                ],
                                "permissions": [
                                    {
                                        "full": "onderwijsinrichting.RSchooljaar:READ:INSTANCE(1234)",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "operations": [
                                            "READ"
                                        ],
                                        "instances": [
                                            "INSTANCE(1234)"
                                        ]
                                    }
                                ],
                                "additionalObjects": {},
                                "naam": "2025/2026",
                                "vanafDatum": "2025-08-01",
                                "totDatum": "2026-07-31",
                                "isHuidig": false
                            },
                            "leerjaar": 4,
                            "heeftExamendossier": true
                        },
                        {
                            "$type": "onderwijsinrichting.RLichtingSchooljaar",
                            "links": [
                                {
                                    "id": 12345678901234,
                                    "rel": "koppeling",
                                    "type": "onderwijsinrichting.RLichtingSchooljaar"
                                }
                            ],
                            "permissions": [],
                            "additionalObjects": {},
                            "schooljaar": {
                                "$type": "onderwijsinrichting.RSchooljaar",
                                "links": [
                                    {
                                        "id": 1234,
                                        "rel": "self",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "href": "https://api.somtoday.nl/rest/v1/schooljaren/1234"
                                    }
                                ],
                                "permissions": [
                                    {
                                        "full": "onderwijsinrichting.RSchooljaar:READ:INSTANCE(1234)",
                                        "type": "onderwijsinrichting.RSchooljaar",
                                        "operations": [
                                            "READ"
                                        ],
                                        "instances": [
                                            "INSTANCE(1234)"
                                        ]
                                    }
                                ],
                                "additionalObjects": {},
                                "naam": "2026/2027",
                                "vanafDatum": "2026-08-01",
                                "totDatum": "2027-07-31",
                                "isHuidig": true
                            },
                            "leerjaar": 5,
                            "heeftExamendossier": true
                        }
                    ],
                    "onderwijssoort": {
                        "$type": "onderwijsinrichting.ROnderwijssoort",
                        "links": [
                            {
                                "id": 1234,
                                "rel": "koppeling",
                                "type": "onderwijsinrichting.ROnderwijssoort"
                            }
                        ],
                        "permissions": [],
                        "additionalObjects": {},
                        "afkorting": "HAVO",
                        "isOnderbouw": false
                    },
                    "UUID": "0000000-0000-0000-0000-000000000000"
                }
            },
            ...
}
```
</details>

### Normal grades `GET /rest/v1/geldendvoortgangsdossierresultaten/vakresultaten/[leerlingid]/vak/[vakid]/lichting/[lichtingid]`
<details><summary>Click to open</summary>

Fetches the normal (overgang) grades of the specified subject. All ids can be gotten from `GET /rest/v1/plaatsingen`

#### Parameters

| Name                     | Type      | Value                                |
|--------------------------|-----------|--------------------------------------|
| leerlingid               | URL       | [student id]                         |
| subjectid                | URL       | [subject id]                         |
| lichtingid               | URL       | [lichting id]                        |
| Authorization            | Header    | Bearer [access_token]                |
| additional               | Parameter | vaknaam                              |
| additional               | Parameter | resultaatkolom                       |
| additional               | Parameter | heeftalternatiefniveau               |
| additional               | Parameter | naamalternatiefniveau                |
| additional               | Parameter | naamstandaardniveau                  |
| additional               | Parameter | leerjaar                             |
| additional               | Parameter | periodeAfkorting                     |
| type                     | Parameter | Toetskolom                           |
| type                     | Parameter | SamengesteldeToetsKolom              |
| type                     | Parameter | Werkstukcijferkolom                  |
| type                     | Parameter | Advieskolom                          |
| type                     | Parameter | PeriodeGemiddeldeKolom               |
| type                     | Parameter | RapportGemiddeldeKolom               |
| type                     | Parameter | RapportCijferKolom                   |
| type                     | Parameter | RapportToetskolom                    |
| type                     | Parameter | SEGemiddeldeKolom                    |
| type                     | Parameter | ToetssoortGemiddeldeKolom            |
| sort                     | Parameter | desc-geldendResultaatCijferInvoer    |
| plaatsingUuid            | Parameter | [plaatsing id]                       |

#### Returns
```json
{
    "items": [
        {
            "$type": "resultaten.RGeldendExamendossierResultaat",
            "links": [
                {
                    "id": 1234,
                    "rel": "self",
                    "type": "resultaten.RGeldendExamendossierResultaat",
                    "href": "https://api.somtoday.nl/rest/v1/geldendexamendossierresultaten/1234"
                }
            ],
            "permissions": [
                {
                    "full": "resultaten.RGeldendExamendossierResultaat:READ:INSTANCE(1234)",
                    "type": "resultaten.RGeldendExamendossierResultaat",
                    "operations": [
                        "READ"
                    ],
                    "instances": [
                        "INSTANCE(1234)"
                    ]
                }
            ],
            "additionalObjects": {
                "resultaatkolom": "1234",
                "vaknaam": "ckv",
                "leerjaar": 4
            },
            "cijfer": 8.1,
            "cijferEerstePoging": 8.1,
            "isVoldoende": true,
            "isVoldoendeEerstePoging": true,
            "periode": 4,
            "formattedResultaat": "8,1",
            "formattedEerstePoging": "8,1",
            "volgnummer": 443,
            "type": "Toetskolom",
            "toetscode": "p44c",
            "omschrijving": "CZP 2",
            "weging": 10,
            "datumInvoerEerstePoging": "2026-07-01T15:20:49",
            "isLabel": false,
            "isCijfer": true,
            "herkansing": "Geen",
            "toetssoort": "PO"
        },
        ...
}
```
</details>

### Exam grades `GET /rest/v1/geldendexamendossierresultaten/vakresultaten/[leerlingid]/vak/[vakid]/lichting/[lichtingid]`
<details><summary>Click to open</summary>

Fetches the exam grades of the specified subject. All ids can be gotten from `GET /rest/v1/plaatsingen`

#### Parameters

| Name                     | Type      | Value                                |
|--------------------------|-----------|--------------------------------------|
| leerlingid               | URL       | [student id]                         |
| subjectid                | URL       | [subject id]                         |
| lichtingid               | URL       | [lichting id]                        |
| Authorization            | Header    | Bearer [access_token]                |
| additional               | Parameter | vaknaam                              |
| additional               | Parameter | resultaatkolom                       |
| additional               | Parameter | heeftalternatiefniveau               |
| additional               | Parameter | naamalternatiefniveau                |
| additional               | Parameter | naamstandaardniveau                  |
| additional               | Parameter | leerjaar                             |
| additional               | Parameter | periodeAfkorting                     |
| type                     | Parameter | Toetskolom                           |
| type                     | Parameter | SamengesteldeToetsKolom              |
| type                     | Parameter | Werkstukcijferkolom                  |
| type                     | Parameter | Advieskolom                          |
| type                     | Parameter | PeriodeGemiddeldeKolom               |
| type                     | Parameter | RapportGemiddeldeKolom               |
| type                     | Parameter | RapportCijferKolom                   |
| type                     | Parameter | RapportToetskolom                    |
| type                     | Parameter | SEGemiddeldeKolom                    |
| type                     | Parameter | ToetssoortGemiddeldeKolom            |
| sort                     | Parameter | desc-geldendResultaatCijferInvoer    |
| plaatsingUuid            | Parameter | [plaatsing id]                       |
#### Returns
```json
{
    "items": [
        {
            "$type": "resultaten.RGeldendExamendossierResultaat",
            "links": [
                {
                    "id": 1234,
                    "rel": "self",
                    "type": "resultaten.RGeldendExamendossierResultaat",
                    "href": "https://api.somtoday.nl/rest/v1/geldendexamendossierresultaten/1234"
                }
            ],
            "permissions": [
                {
                    "full": "resultaten.RGeldendExamendossierResultaat:READ:INSTANCE(1234)",
                    "type": "resultaten.RGeldendExamendossierResultaat",
                    "operations": [
                        "READ"
                    ],
                    "instances": [
                        "INSTANCE(1234)"
                    ]
                }
            ],
            "additionalObjects": {
                "resultaatkolom": "1234",
                "vaknaam": "ckv",
                "leerjaar": 4
            },
            "cijfer": 8.1,
            "cijferEerstePoging": 8.1,
            "isVoldoende": true,
            "isVoldoendeEerstePoging": true,
            "periode": 4,
            "formattedResultaat": "8,1",
            "formattedEerstePoging": "8,1",
            "volgnummer": 443,
            "type": "Toetskolom",
            "toetscode": "p44c",
            "omschrijving": "CZP 2",
            "weging": 10,
            "datumInvoerEerstePoging": "2026-07-01T15:20:49",
            "isLabel": false,
            "isCijfer": true,
            "herkansing": "Geen",
            "toetssoort": "PO"
        },
        ...
}
```
</details>
