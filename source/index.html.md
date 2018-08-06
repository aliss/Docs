---
title: ALISS API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

search: true
---

# Introduction

Welcome to the ALISS API! You can use our API to search for Health and Wellbeing services in Scotland.

Both these docs and ALISS are open source. If you'd like to improve [this documentation](https://github.com/aliss/Docs) or [ALISS itself](https://github.com/aliss/ALISS) please add an issue or submit a pull request.

# Attribution and licensing

ALISS allows the use of data under a [Creative Commons (CC BY 4.0) licence](https://creativecommons.org/licenses/by/4.0/). For more information see [ALISS Terms and Conditions](https://www.aliss.org/terms-and-conditions/).

ALISS, contains data from a variety of sources, including:

- National Statistics data © Crown copyright and database right 2018 [(Open Government Licence v3.0)](http://www.nationalarchives.gov.uk/doc/open-government-licence/)
- [The Scottish Charity Register](https://www.oscr.org.uk) (Office of the Scottish Charity Register) shared under the [Open Government Licence (v2.0)](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/2/)
- [Scottish Postcode Directory](https://www.nrscotland.gov.uk/statistics-and-data/geography/nrs-postcode-extract) (National Records of Scotland) shared under the [Open Government Licence (v3.0)](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)
- Contributions by [ALISS users](https://www.aliss.org/terms-and-conditions/)


# API Version 4

## Service search

```shell
curl "https://www.aliss.org/api/v4/services/?postcode=G2 4AA"
```

> The above command returns JSON structured like this:

```json

{
    "meta": {
        "attribution": [
            {
                "text": "Contains National Statistics data © Crown copyright and database right 2018",
                "url": "http://geoportal.statistics.gov.uk/datasets/local-authority-districts-december-2016-generalised-clipped-boundaries-in-the-uk/"
            },
            {
                "text": "Contains information from the Scottish Charity Register supplied by the Office of the Scottish Charity Regulator and licensed under the Open Government Licence v2.0",
                "url": "https://www.oscr.org.uk/about-charities/search-the-register/charity-register-download"
            },
            {
                "text": "Contains National Records of Scotland data licensed under the Open Government Licence v3.0",
                "url": "https://www.nrscotland.gov.uk/statistics-and-data/geography/nrs-postcode-extract"
            },
            {
                "text": "Contains contributions from ALISS users",
                "url": "https://www.aliss.org/terms-and-conditions"
            }
        ],
        "licence": "https://creativecommons.org/licenses/by/4.0/"
    },
    "count": 222,
    "next": "https://www.aliss.org/api/v4/services/?page=2&postcode=G2+4AA",
    "previous": null,
    "data": [
        {
            "id": "fed34ae8-cf8b-4d6d-9250-6a7d56809d8d",
            "organisation": {
                "id": "0e5d57d2-2e3d-4538-9c4f-d72770d608a7",
                "name": "CrossReach",
                "aliss_url": "https://www.aliss.org/organisations/0e5d57d2-2e3d-4538-9c4f-d72770d608a7/",
                "is_claimed": false
            },
            "name": "One-to-one counselling",
            "description": "Sometimes we experience difficulties and may or may not know why we feel uneasy, anxious or depressed. Counselling provides the chance to explore feelings and experiences in a safe and confidential environment with someone who is trained to help you.\r\n\r\nThe counsellor won’t give you advice or tell you what to do. They will give you time, space and their particular skills to help you work toward a more satisfactory life.",
            "url": "http://www.crossreach.org.uk/one-one-counselling",
            "phone": "0141 221 1535",
            "email": "tomallan@crossreach.org.uk",
            "categories": [
                {
                    "name": "Counselling",
                    "slug": "counselling"
                },
                {
                    "name": "Mental Health Issues",
                    "slug": "mental-health"
                }
            ],
            "locations": [
                {
                    "id": "619d32db-e780-44ab-8ed2-5180c56fc1c3",
                    "formatted_address": "Tom Allan Centre, 23 Elmbank Street, Glasgow, G2 4PB",
                    "name": "Tom Allan Centre",
                    "description": "",
                    "street_address": "23 Elmbank Street",
                    "locality": "Glasgow",
                    "region": "",
                    "state": "",
                    "postal_code": "G2 4PB",
                    "country": "GB",
                    "latitude": 55.8639028,
                    "longitude": -4.2685076
                }
            ],
            "service_areas": [
                {
                    "code": "S12000046",
                    "type": "Local Authority",
                    "name": "Glasgow City"
                }
            ],
            "aliss_url": "https://www.aliss.org/services/fed34ae8-cf8b-4d6d-9250-6a7d56809d8d/",
            "last_updated": "2018-01-24T09:57:56.111368+00:00"
        },
        {
            "id": "a6750941-8b45-4259-9835-ada48c34d9b3",
            "organisation": {
                "id": "f5e9fa9e-774e-49a8-af12-627466225b9e",
                "name": "StepChange Debt Charity",
                "aliss_url": "https://www.aliss.org/organisations/f5e9fa9e-774e-49a8-af12-627466225b9e/",
                "is_claimed": false
            },
            "name": "Debt Advice",
            "description": "Provides free, impartial, confidential advice tailored to your situation. We also provide a range of managed debt solutions plus support you need to help you deal with your debts.",
            "url": "https://www.stepchange.org/Howwecanhelpyou/Debtadvice.aspx",
            "phone": "0800 138 1111",
            "email": "",
            "categories": [
                {
                    "name": "Money Advice",
                    "slug": "money-advice"
                }
            ],
            "locations": [],
            "service_areas": [
                {
                    "code": "XS",
                    "type": "Country",
                    "name": "Scotland"
                }
            ],
            "aliss_url": "https://www.aliss.org/services/a6750941-8b45-4259-9835-ada48c34d9b3/",
            "last_updated": "2018-01-26T15:55:34.778144+00:00"
        },
        {
            "id": "17074c19-1f0d-47b9-a798-361b10bad50f",
            "organisation": {
                "id": "17e6fe98-ea05-440f-84a9-45e81f93e4ef",
                "name": "Scottish Families Affected by Alcohol and Drugs (SFAD)",
                "aliss_url": "https://www.aliss.org/organisations/17e6fe98-ea05-440f-84a9-45e81f93e4ef/",
                "is_claimed": false
            },
            "name": "Bereavement Support Service",
            "description": "Have you lost a loved one due where drugs were implicated in the cause of their death in the last 5 years?  Would you like someone to talk to?\r\n\r\nScottish Families offers a FREE and confidential support service to provide you with listening and emotional support in the immediate period after the loss of your loved one and, if appropriate, we can arrange up to 6 face to face counselling sessions for you.  We can also give you information about local peer support groups to meet together with people who have experienced a similar loss.\r\n\r\nYou will receive your initial telephone appointment from our Bereavement Co-ordinator within 5 working days of making contact with the Helpline.",
            "url": "http://www.sfad.org.uk/get-help-now/bereavement-support-service",
            "phone": "08080 101011",
            "email": "helpline@sfad.org.uk",
            "categories": [
                {
                    "name": "Drug Addiction",
                    "slug": "drug-addiction"
                },
                {
                    "name": "Bereavement",
                    "slug": "bereavement"
                }
            ],
            "locations": [],
            "service_areas": [
                {
                    "code": "XS",
                    "type": "Country",
                    "name": "Scotland"
                }
            ],
            "aliss_url": "https://www.aliss.org/services/17074c19-1f0d-47b9-a798-361b10bad50f/",
            "last_updated": "2018-01-11T13:15:18.344698+00:00"
        },
        {
            "id": "f6f28039-1d8e-4041-8d6b-9b4f0acdc42e",
            "organisation": {
                "id": "4def5506-6b9e-4de0-aab0-4f31bf68884d",
                "name": "Quaker Social Action",
                "aliss_url": "https://www.aliss.org/organisations/4def5506-6b9e-4de0-aab0-4f31bf68884d/",
                "is_claimed": false
            },
            "name": "Down to Earth",
            "description": "With funeral costs high and rising, many people faced with a sudden loss struggle to find an affordable send off for their loved ones. Our unique service aims to ensure no one faces unnecessary debt or distress due to high funeral costs.\r\n\r\nDown to Earth supports you to identify and arrange an affordable and meaningful funeral. We can do this face to face, over the phone or by email. Our experienced team support thousands of people across the UK to look at their options, keep costs affordable, and identify ways to raise money for a funeral.",
            "url": "https://www.quakersocialaction.org.uk/we-can-help/helping-bereavement/down-earth/how-it-works",
            "phone": "020 8983 5055",
            "email": "downtoearth@qsa.org.uk",
            "categories": [
                {
                    "name": "Money",
                    "slug": "money"
                },
                {
                    "name": "Burial & Funeral Help",
                    "slug": "burial-funeral-help"
                }
            ],
            "locations": [],
            "service_areas": [
                {
                    "code": "XB",
                    "type": "Country",
                    "name": "United Kingdom"
                }
            ],
            "aliss_url": "https://www.aliss.org/services/f6f28039-1d8e-4041-8d6b-9b4f0acdc42e/",
            "last_updated": "2018-01-11T13:25:16.249587+00:00"
        },
        {
            "id": "501d6827-c460-4361-a68d-902ff6656856",
            "organisation": {
                "id": "15ac4a10-2635-4992-ad26-3b554d27ffbb",
                "name": "Abused Men in Scotland",
                "aliss_url": "https://www.aliss.org/organisations/15ac4a10-2635-4992-ad26-3b554d27ffbb/",
                "is_claimed": false
            },
            "name": "Domestic Violence Helpline",
            "description": "Our Domestic violence helpline for men is open every weekday 9:00 am to 4:00 pm. whether you want to take the first steps to leaving an abusive relationship or just want to someone to talk too, give us a call today on:",
            "url": "http://www.amis.org.uk/help-for-men.html",
            "phone": "0808 800 0024",
            "email": "",
            "categories": [
                {
                    "name": "Mental Health Issues",
                    "slug": "mental-health"
                },
                {
                    "name": "Mens Health",
                    "slug": "mens-health"
                },
                {
                    "name": "Sexual Violence",
                    "slug": "sexual-violence"
                }
            ],
            "locations": [],
            "service_areas": [
                {
                    "code": "XS",
                    "type": "Country",
                    "name": "Scotland"
                }
            ],
            "aliss_url": "https://www.aliss.org/services/501d6827-c460-4361-a68d-902ff6656856/",
            "last_updated": "2018-01-09T15:45:15.473794+00:00"
        },
        {
            "id": "8e3e6ee9-359a-472d-b573-4e0a75fe2145",
            "organisation": {
                "id": "7b202cac-03c4-4246-94be-66dda9994700",
                "name": "In Care Survivors Service Scotland (ICSSS)",
                "aliss_url": "https://www.aliss.org/organisations/7b202cac-03c4-4246-94be-66dda9994700/",
                "is_claimed": false
            },
            "name": "Helpline",
            "description": "A national confidential telephone Helpline with a team of specially trained counsellors offering help specifically for survivors of historic in-care abuse.\r\n\r\nThis helpline is currently available from 9am to 11am Monday to Friday and is for those of you who have not yet been allocated a worker or to make a new referral.",
            "url": "http://www.incaresurvivors.org.uk/index.php?option=com_content&view=article&id=91&Itemid=127",
            "phone": "0800 121 6027",
            "email": "",
            "categories": [
                {
                    "name": "Counselling",
                    "slug": "counselling"
                },
                {
                    "name": "Mental Health Issues",
                    "slug": "mental-health"
                }
            ],
            "locations": [],
            "service_areas": [
                {
                    "code": "XS",
                    "type": "Country",
                    "name": "Scotland"
                }
            ],
            "aliss_url": "https://www.aliss.org/services/8e3e6ee9-359a-472d-b573-4e0a75fe2145/",
            "last_updated": "2018-01-18T11:09:03.373490+00:00"
        }
    ]
}
```

The service search feature is the core of ALISS. Search returns services on ALISS filtered by geography, and optionally by keywords or categories.

Services can be delivered at a specific location, or they can be delivered across a whole area or areas. Locations are specific to the organisations that run the services, whereas areas of delivery are selected from a pre-defined list. You can request the list of possible areas from the [`service-areas` endpoint](#service-areas).

### HTTP Request

`GET https://www.aliss.org/api/v4/services/`

You can request an HTML formatted version of the result with your browser: [https://www.aliss.org/api/v4/services/?postcode=G2 4AA](https://www.aliss.org/api/v4/services/?postcode=G2%204AA)

### Query parameters

Parameter | Required | Default | Description
--------- | -------- | ------- | -----------
postcode | True | None | The postcode that you wish to find services relevant to
q | False | None | This is the keywords with which to do a full text search of the services
category | False | None | The category slugs that you wish to filter the search by
location_type | False | None | The location type of the resource, either 'local' or 'national', default searches everything
radius | False | 5000 | The radius from the postcode that you wish the search to cover, in meters
page_size | False | 10 | The number of results in a page (max. 100)

### Filter by categories

`GET https://www.aliss.org/api/v4/services/?category=money-advice&postcode=G2 4AA`

You can filter by category by using the category query parameter and passing in a category slug.

### Filter by location type

`GET https://www.aliss.org/api/v4/services/?location_type=local&postcode=G2 4AA`

You can filter by location type by using the location type query parameter and passing in either 'local' or 'national'.

### Response structure

Key | Description
--- | ---
meta | metadata associated with the result
count | number of results returned in all pages of the request
next | url to next page
previous | url to previous page
results | collection of service objects (see below)

**Service object**

Key | Description
--- | ---
id | UUID for the service
name | name of the service
organisation.id | object with details of the organisation that runs the service
organisation.name | name of the organisation
organisation.aliss_url | url to the organisation entry on aliss.org
organisation.is_claimed | whether a representative of the organisation has claimed editorial privelege over the entry
description | free text description of the service
url | url to a site describing the service 
phone | contact telephone number for the service
email | contact email address for the service
categories | collection of category objects associated with the service including a human readable name and slug
locations | collection of location objects associated with the service
service_areas | collection of service area objects associated with the service, a full list of possible areas can be requested from the [service areas endpoint](#service-areas)
aliss_url | url to the service entry on aliss.org
last_updated | timestamp ([ISO 8601](https://www.w3.org/TR/NOTE-datetime)) of when the service entry was last edited


## Categories

### List all Categories

```shell
curl "https://www.aliss.org/api/v4/categories/"
```

> The above command returns JSON structured like this:

```json
{
    "meta": {
        "attribution": [],
        "licence": "https://creativecommons.org/licenses/by/4.0/"
    },
    "data": [
        {
            "name": "Housing and Homelessness",
            "slug": "housing-and-homelessness",
            "sub_categories": [
                {
                    "name": "Social Housing",
                    "slug": "social-housing",
                    "sub_categories": []
                },
                {
                    "name": "Sheltered Housing",
                    "slug": "sheltered-housing",
                    "sub_categories": []
                },
                {
                    "name": "Housing Advice",
                    "slug": "housing-advice",
                    "sub_categories": []
                },
                {
                    "name": "Housing Support",
                    "slug": "housing-support",
                    "sub_categories": []
                },
                {
                    "name": "Housing Adaptations",
                    "slug": "housing-adaptations",
                    "sub_categories": []
                }
            ]
        },
        {
            "name": "Food & Nutrition",
            "slug": "food-nutrition",
            "sub_categories": [
                {
                    "name": "Community Garden",
                    "slug": "community-garden",
                    "sub_categories": []
                },
                {
                    "name": "Food Delivery",
                    "slug": "food-delivery",
                    "sub_categories": []
                },
                {
                    "name": "Foodbank",
                    "slug": "foodbank",
                    "sub_categories": []
                },
                {
                    "name": "Free Meals",
                    "slug": "free-meals",
                    "sub_categories": []
                },
                {
                    "name": "Community Cafe",
                    "slug": "community-cafe",
                    "sub_categories": []
                }
            ]
        },
        {
            "name": "Money",
            "slug": "money",
            "sub_categories": [
                {
                    "name": "Money Advice",
                    "slug": "money-advice",
                    "sub_categories": []
                },
                {
                    "name": "Energy Advice",
                    "slug": "energy-advice",
                    "sub_categories": []
                }
            ]
        }
    ]
}
```

This endpoint retrieves all categories. 

### HTTP Request

`GET https://www.aliss.org/api/v4/categories/`

You can view an HTML formatted version of the result with your browser: [https://www.aliss.org/api/v4/categories/](https://www.aliss.org/api/v4/categories/)


## Service areas

### List all Service areas

```shell
curl "https://www.aliss.org/api/v4/service-areas/"
```

> The above command returns JSON structured like this:

```json
{
    "meta": {
        "attribution": [
            {
                "text": "Contains National Statistics data © Crown copyright and database right 2018",
                "url": "http://geoportal.statistics.gov.uk/datasets/local-authority-districts-december-2016-generalised-clipped-boundaries-in-the-uk/"
            },
            {
                "text": "Contains information from the Scottish Charity Register supplied by the Office of the Scottish Charity Regulator and licensed under the Open Government Licence v2.0",
                "url": "https://www.oscr.org.uk/about-charities/search-the-register/charity-register-download"
            }
        ],
        "licence": "https://creativecommons.org/licenses/by/4.0/"
    },
    "data": [
        {
            "code": "S12000005",
            "type": "Local Authority",
            "name": "Clackmannanshire"
        },
        {
            "code": "S12000006",
            "type": "Local Authority",
            "name": "Dumfries and Galloway"
        },
        {
            "code": "S12000008",
            "type": "Local Authority",
            "name": "East Ayrshire"
        },
        {
            "code": "S12000010",
            "type": "Local Authority",
            "name": "East Lothian"
        },
        {
            "code": "S12000011",
            "type": "Local Authority",
            "name": "East Renfrewshire"
        },
        {
            "code": "S12000013",
            "type": "Local Authority",
            "name": "Na h-Eileanan Siar"
        },
        {
            "code": "S12000014",
            "type": "Local Authority",
            "name": "Falkirk"
        },
        {
            "code": "S12000015",
            "type": "Local Authority",
            "name": "Fife"
        }
    ]
}
```

This endpoint retrieves all service areas. An HTML formatted version of the result is available here: http://www.aliss.org/api/v4/service-areas/

### HTTP Request

`GET https://www.aliss.org/api/v4/service-areas/`

You can view an HTML formatted version of the result with your browser: [https://www.aliss.org/api/v4/service-areas/](https://www.aliss.org/api/v4/service-areas/)

## Changes since v3

The main difference between v4 and v3 is the structure of the JSON that is returned. All endpoints return an object rather than collections. This change facilitated the addition of metadata and other fields to the responses. The categories endpoint returns a significantly different result, as the response objects are structured to reflect the hierarchy of parent and sub-categories, rather than being flattened.

Other notable changes:

- Service endpoint has taken a more RESTful style (`/services` rather than `/search`)
- Service objects include a `last_updated` field
- Service and organisation objects include `aliss_url` fields
- Service organisation object includes a `is_claimed` field
- Service area `type` field shows a human friendly boundary name

# API Version 3

## Search

Thes service search feature is the core of ALISS. Search returns services on ALISS filtered by geography, and optionally by keywords or categories.

Services can be delivered at a specific location, or they can be delivered across a whole area or areas. Locations are specific to the organisations that run the services, whereas areas of delivery are selected from a pre-defined list. You can request the list of possible areas from the [`service-areas` endpoint](#service-areas).


```shell
curl "https://www.aliss.org/api/v3/search/?postcode=G2 4AA"
```

> The above command returns JSON structured like this:

```json
{
    "count":159,
    "next":"https://www.aliss.org/api/v3/search/?page=2&postcode=G2+4AA",
    "previous":null,
    "results":[
        {
            "id":"417f8631-f38e-46ef-9cf3-ea9e3fc6f47c",
            "organisation": {
                "id": "c823d858-d417-487d-a09d-11720e801519",
                "name": "Possobilities"
            },
            "name": "Cook and Care",
            "description": "For almost 12 years, our social enterprise, Cook and Care has been providing a first-class meals delivery service for vulnerable, elderly and disabled people in their own homes. Cook and Care widens our message of supporting independent living because we are able to help people stay in their own homes for longer.\r\n\r\nWe serve the whole of North Glasgow and pride ourselves on the quality of our meals and the efficiency and friendliness of our volunteer care staff.\r\n\r\nOur homemade meals are cooked from scratch every day and delivered hot and ready to eat, rather than overpriced frozen meals\r\nOur menus are varied, working on a 3 weekly menu cycle and are always healthy and nutritious. In addition, theyâ€™re really delicious!\r\nOur local volunteers are very flexible we can deliver on one or two days only, or every day, as required, hence a meal delivery tailored to suit you!\r\nOur service is open to anyone who needs it. Some of our customers have a disability, others use Cook and Care simply for convenience or due to temporary illness. It might even save you cooking!\r\n\r\nWe are always happy to discuss your requirements and can also take away a lot of the anxiety and stress of caring for a friend or relative at meal times.\r\n\r\nMeals are currently £4.00 for a 3 course meal, fantastic value for money and you can order online!",
            "url": "http://possobilities.org.uk/cook-n-care-meal-delivery/",
            "phone": "0141 336 3562",
            "email": "",
            "categories": [
                {
                    "name": "Food",
                    "slug": "food"
                }
            ],
            "locations": [],
            "service_areas": [
                {
                    "code":"S12000046",
                    "type":"Local Authority",
                    "name":"Glasgow City"
                }
            ]
        },
        {
            "id": "79e5b5d9-91b8-4bd1-9117-d4cdd2f717cc",
            "organisation": {
                "id": "fbbb0dee-94e4-4806-b517-3934fb21a49d",
                "name": "Glasgow Central Citizens Advice Bureau"
            },
            "name": "Debt Advice",
            "description": "Are you finding it difficult to manage your debts?\r\n\r\nGlasgow Central CAB have advisers who can assist you to look at the options available to help.\r\n\r\nGlasgow Central CAB will only see people who live or work in the Glasgow City Council Tax area.\r\n\r\nThe bureau does not run an appointment system. We only operate a drop-in service where clients are seen in turn.",
            "url": "http://www.glasgowcentralcab.org.uk/debt.html",
            "phone": "0141 552 5556",
            "email": "",
            "categories": [
                {
                    "name": "Money Advice",
                    "slug": "money-advice"
                }
            ],
            "locations": [
                {
                    "id": "e5431115-a06f-4ca9-ad4d-9d158a492adf",
                    "formatted_address": "The Mitchell Library, 201 North St, Glasgow, G3 7DN",
                    "name": "The Mitchell Library",
                    "description": "",
                    "street_address": "201 North St",
                    "locality": "Glasgow",
                    "region": "Glasgow City",
                    "state": "",
                    "postal_code": "G3 7DN",
                    "country": "GB",
                    "latitude": 55.8651895,
                    "longitude": -4.2724227
                }
            ],
            "service_areas": []
        }
    ]
}
```

### HTTP Request

`GET https://www.aliss.org/api/v3/search/`

### Query parameters

Parameter | Required | Default | Description
--------- | -------- | ------- | -----------
postcode | True | None | The postcode that you wish to find services relevant to
q | False | None | This is the keywords with which to do a full text search of the services
category | False | None | The category slugs that you wish to filter the search by
location_type | False | None | The location type of the resource, either 'local' or 'national', default searches everything
radius | False | 5000 | The radius from the postcode that you wish the search to cover, in meters

### Filter by categories

`GET https://www.aliss.org/api/v3/search/?category=money-advice&postcode=G2 4AA`

You can filter by category by using the category query parameter and passing in a category slug.

### Filter by location type

`GET https://www.aliss.org/api/v3/search/?location_type=local&postcode=G2 4AA`

You can filter by location type by using the location type query parameter and passing in either 'local' or 'national'.

### Response structure

Key | Description
--- | ---
count | number of results returned in all pages of the request
next | url to next page
previous | url to previous page
results | collection of service objects (see below)

**Service object**

Key | Description
--- | ---
id | UUID for the service
organisation | object with details of the organisation that runs the service
name | name of the service
description | free text description of the service
url | url to a site describing the service 
phone | contact telephone number for the service
email | contact email address for the service
categories | collection of category objects associated with the service including a human readable name and slug
locations | collection of location objects associated with the service
service_areas | collection of service area objects associated with the service, a full list of possible areas can be requested from the [service areas endpoint](#service-areas)


## Categories

### List all Categories

```shell
curl "https://www.aliss.org/api/v3/categories/"
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": 2,
        "name": "Housing and Homelessness",
        "slug": "housing-and-homelessness",
        "parent": null
    },
    {
        "id": 5,
        "name": "Depression",
        "slug": "depression",
        "parent": 3
    },
    {
        "id": 6,
        "name": "Suicide",
        "slug": "suicide",
        "parent": 3
    },
    {
        "id": 7,
        "name": "Anxiety",
        "slug": "anxiety",
        "parent": 3
    }
]
```

This endpoint retrieves all categories.

### HTTP Request

`GET https://www.aliss.org/api/v3/categories/`


## Service areas

### List all service areas

```shell
curl "https://www.aliss.org/api/v3/service-areas/"
```

> The above command returns JSON structured like this:

```json
[
    {
        "code": "S37000025",
        "type": "4",
        "name": "Scottish Borders"
    },
    {
        "code": "S37000026",
        "type": "4",
        "name": "Shetland Islands"
    },
    {
        "code": "S37000027",
        "type": "4",
        "name": "South Ayrshire"
    },
    {
        "code": "S37000028",
        "type": "4",
        "name": "South Lanarkshire"
    },
    {
        "code": "S37000029",
        "type": "4",
        "name": "West Dunbartonshire"
    },
    {
        "code": "S37000030",
        "type": "4",
        "name": "West Lothian"
    },
    {
        "code": "S37000031",
        "type": "4",
        "name": "Western Isles"
    },
    {
        "code": "XB",
        "type": "0",
        "name": "United Kingdom"
    },
    {
        "code": "XS",
        "type": "0",
        "name": "Scotland"
    }
]
```

This endpoint retrieves all service areas.

### HTTP Request

`GET https://www.aliss.org/api/v3/service-areas/`
