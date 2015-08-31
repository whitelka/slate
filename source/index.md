---
title: API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to Careerfully API!

# Authentication

# APIs

## Users
Method | Path | Params 
-------------- | -------------- | --------------
POST | /api/v1/user | email, password, full_name

## Session
Method | Path | Params 
-------------- | -------------- | --------------
POST | /api/v1/session | email, password

## Matches
> GET /api/v1/candidate/matches result looks like this:

```json
{
  "matches": [
    {
      "id": 4,
      "job_description_id": 2,
      "bookmarked": false,
      "applied": true,
      "company_name": "The Ventures",
      "job_description_title": "Web Frontend Engineer",
      "key_skills": []
    },
    {
      "id": 3,
      "job_description_id": 1,
      "bookmarked": false,
      "applied": false,
      "company_name": "Seedtime",
      "job_description_title": "SW Engineer",
      "key_skills": []
    }
  ],
  "meta": {
    "page_count": 1
  }
}
```
> GET /api/v1/candidate/match result looks like this:

```json
{
  "match": {
    "id": 4,
    "job_description_id": 2,
    "bookmarked": false,
    "applied": true,
    "company_name": "The Ventures",
    "job_description_title": "Web Frontend Engineer",
    "experience_range_start": null,
    "experience_range_end": null,
    "address": "bangalore test",
    "qualifications": {
      "key_skills": [],
      "domains": [
        {
          "trait_name": "system programming"
        }
      ],
      "programming_languages": [
        {
          "trait_name": "Java"
        }
      ],
      "industries": [],
      "platforms": [],
      "roles": [],
      "tools": [],
      "specific_technologies": [],
      "concepts": []
    }
  }
}
```
Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/matches | 
GET | /api/v1/candidate/match | id

## Bookmarks
Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/bookmarks | 
GET | /api/v1/candidate/bookmark | id
POST | /api/v1/candidate/bookmark/create | match_id 또는 job_description_id
DELETE | /api/v1/candidate/bookmark/destroy | id

## Applications
> GET /api/v1/candidate/applications result lloks like this:

```json
{
  "applications": [
    {
      "id": 1,
      "company_name": "The Ventures",
      "job_description_title": "Web Frontend Engineer",
      "job_description_id": 2,
      "experience_range_start": null,
      "experience_range_end": null,
      "key_skills": []
    },
    {
      "id": 2,
      "company_name": "Seedtime",
      "job_description_title": "SW Engineer",
      "job_description_id": 1,
      "experience_range_start": null,
      "experience_range_end": null,
      "key_skills": []
    }
  ],
  "meta": {
    "page_count": 1
  }
}
```
> GET /api/v1/candidate/offers result lloks like this:
```json
{
  "offers": [
    {
      "id": 1,
      "company_name": "The Ventures",
      "job_description_title": "Web Frontend Engineer",
      "job_description_id": 2,
      "experience_range_start": null,
      "experience_range_end": null,
      "key_skills": []
    }
  ],
  "meta": {
    "page_count": 1
  }
}
```

Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/applications | 
GET | /api/v1/candidate/application | id
POST | /api/v1/candidate/application/create | job_description_id or match_id

## Offers
> GET /api/v1/candidate/offers result lloks like this:

```json
{
  "offers": [
    {
      "id": 1,
      "company_name": "The Ventures",
      "job_description_title": "Web Frontend Engineer",
      "job_description_id": 2,
      "experience_range_start": null,
      "experience_range_end": null,
      "key_skills": []
    }
  ],
  "meta": {
    "page_count": 1
  }
}
```

> GET /api/v1/candidate/offer result lloks like this:

```json
{
  "id": 1,
  "job_description_title": "Web Frontend Engineer",
  "job_description_id": 2,
  "company_name": "The Ventures",
  "current_stage": "applied",
  "key_skills": []
}
```

Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/offers | 
GET | /api/v1/candidate/offer | 

## Profile
> GET /api/v1/candidate/profile result looks like this:

```json
{
  "profile": {
    "id": 1,
    "address": null,
    "preferences_traits": {
      "domain": [
        {
          "trait_id": 1,
          "trait_name": "mobile game"
        }
      ],
      "platform": [
        {
          "trait_id": 19,
          "trait_name": "CentOS"
        }
      ],
      "programming_language": [
        {
          "trait_id": 10,
          "trait_name": "Java"
        }
      ], 
      "tool": [
        {
          "trait_id": 20,
          "trait_name": "CentOS"
        }
      ]
    }
  }
}
```

> GET /api/v1/candidate/profile/traits result looks like this:

```json
{
  "role": {
    "recommanded_traits": [],
    "traits": []
  },
  "domain": {
    "recommanded_traits": [],
    "traits": [
      {
        "id": 1,
        "name": "mobile game"
      },
      {
        "id": 2,
        "name": "system programming"
      },
      {
        "id": 3,
        "name": "network programming"
      },
      {
        "id": 4,
        "name": "Product QA"
      },
      {
        "id": 5,
        "name": "phone protocol stack"
      },
      {
        "id": 6,
        "name": "web frontend"
      }
    ]
  }
}
```
Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/profile | 
GET | /api/v1/candidate/profile/traits | trait_types[] 

