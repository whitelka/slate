# Authentication

## Users Sign Up

Method | Path | Params
-------------- | -------------- | --------------
POST | /api/v1/user/create | email, password, full_name
POST | /api/v1/user/create_with_sns | sns_type, sns_access_token
GET | /api/v1/user/sns_redirect |

## Session (Sign In)
> POST /api/v1/session/create result looks like this:

```json
{
  "email": "test@test.com",
  "token_type": "Bearer",
  "id": 79827032,
  "full_name": "tester",
  "access_token": "B-5P9o7et7zxKfrtHXFx",
  "sns_access_token": null,
  "city": null,
  "role": null,
  "domain": null,
  "key_skills": null,
  "photo_url": null,
  "phone": "",
  "active": false,
  "experience": null,
  "min_salary": null,
  "preferred_city": null,
  "wish_to_avoid": null,
  "available_in": null,
  "resume_url": null,
  "resume_updated_at": null
}
```

> POST /api/v1/session/create_with_sns result looks like this:

```json
{
  "email": "test@test.com",
  "id": 55039602,
  "full_name": "Gloria",
  "access_token": "-rLzhoazgNCsmHW35k4W",
  "sns_access_token": "CAACLnYtoWl4BAH96ZBxAFwMeRLp9k5XxV51rBEZBO0gV94WcH2Tna7jsscjEqBTdMGukN9UDipX7zPJpFDQTzBW5pPm6IE9TCIZAXAbkfYiVZCtU6ChiogP7uIFHoUUhIDANtBZCAsQaPIpsWAZCt0zybSrBNXNcpNOzKvpsT3l1FzCigmDMjBTS5pbjuewfRbIzvnx6Ums6cDdWZCQJLBS9Jm94TB9SNZCsnDnVlFQgggZDZD"
}
```

Method | Path | Params
-------------- | -------------- | --------------
POST | /api/v1/session/create | email, password
POST | /aii/v1/session/create_with_sns | sns_type, sns_access_token
GET | /aii/v1/session/sns_redirect | 

## Account

Method | Path | Params
-------------- | -------------- | --------------
GET | /api/v1/account/request_otp | contact(email or phone)
POST | /aii/v1/session/verify_otp | contact(email or phone), otp_code
POST | /aii/v1/session/reset_password | contact(email or phone), otp_code, new_password
POST | /aii/v1/session/change_password | current_password, new_password
