# APIs

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
    "key_skills": [],
    "qualifications": {
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

## Applications
> GET /api/v1/candidate/applications result looks like this:

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

Method | Path | Params
-------------- | -------------- | --------------
GET | /api/v1/candidate/applications |
GET | /api/v1/candidate/application | id
POST | /api/v1/candidate/application/create | match_id
POST | /api/v1/candidate/application/cancel | id

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
        "trait_id": 1,
        "trait_name": "mobile game"
      },
      {
        "trait_id": 2,
        "trait_name": "system programming"
      },
      {
        "trait_id": 3,
        "trait_name": "network programming"
      },
      {
        "trait_id": 4,
        "trait_name": "Product QA"
      },
      {
        "trait_id": 5,
        "trait_name": "phone protocol stack"
      },
      {
        "trait_id": 6,
        "trait_name": "web frontend"
      }
    ]
  }
}
```

> GET /api/v1/candidate/profile/cities result looks like this:

```json
{
  "cities" : {
    [ { "name" : "bangalore" },
      { "name": "haryana" },
      { "name": "mumbai" } ]
  }
}
```
Method | Path | Params
-------------- | -------------- | --------------
GET | /api/v1/candidate/profile |
GET | /api/v1/candidate/profile/traits | trait_types[]
GET | /api/v1/candidate/profile/cities | 

