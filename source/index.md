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
Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/matches | 
GET | /api/v1/candidate/match | id
``` json
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
## Bookmarks
Method | Path | Params 
-------------- | -------------- | --------------
GET | /api/v1/candidate/bookmarks | 
GET | /api/v1/candidate/bookmark | id
POST | /api/v1/candidate/bookmark/create | match_id 또는 job_description_id
DELETE | /api/v1/candidate/bookmark/destroy | id

## Applications
## Profile
Method | Path | Params 
-------------- | -------------- | --------------
GET | /candidate/profile | 
``` json
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

