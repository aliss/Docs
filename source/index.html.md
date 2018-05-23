---
title: ALISS API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

search: true
---

# Introduction

Welcome to the ALISS API! You can use our API to search for Health and Wellbeing services in Scotland.

ALISS is open source find us at (https://github.com/ALISS).

# Search

## Overview

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

This endpoint searches ALISS services.

### HTTP Request

`GET https://www.aliss.org/api/v3/search/`

### Query Parameters

Parameter | Required | Default | Description
--------- | -------- | ------- | -----------
postcode | True | None | The postcode that you wish to find services relevant to
q | False | None | This is the keywords with which to do a full text search of the services
category | False | None | The category slug's that you wish to filter the search by
location_type | False | None | The location type of the resource, either 'local' or 'national', default searches everything
radius | False | 5000 | The radius from the postcode that you wish the search to cover, in meters

### Filter by categories

`GET https://www.aliss.org/api/v3/search/?category=money-advice&postcode=G2 4AA`

You can filter by category by using the category query parameter and passing in a category slug.

### Filter by location type

`GET https://www.aliss.org/api/v3/search/?location_type=local&postcode=G2 4AA`

You can filter by location type by using the location type query parameter and passing in either 'local' or 'national'.


# Categories

## List all Categories

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


# Service Areas

## List all Service Areas

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
