# Authentication

## Users Sign Up
Method | Path | Params
-------------- | -------------- | --------------
POST | /api/v1/user | email, password, full_name
POST | /api/v1/user/facebook | facebook_access_token
POST | /api/v1/user/linkedin |

## Session (Sign In)
> POST /api/v1/session/facebook success result looks like this:

```json
{
  "email": "test@test.com",
  "id": 55039602,
  "full_name": "Gloria",
  "access_token": "-rLzhoazgNCsmHW35k4W",
  "facebook_access_token": "CAACLnYtoWl4BAH96ZBxAFwMeRLp9k5XxV51rBEZBO0gV94WcH2Tna7jsscjEqBTdMGukN9UDipX7zPJpFDQTzBW5pPm6IE9TCIZAXAbkfYiVZCtU6ChiogP7uIFHoUUhIDANtBZCAsQaPIpsWAZCt0zybSrBNXNcpNOzKvpsT3l1FzCigmDMjBTS5pbjuewfRbIzvnx6Ums6cDdWZCQJLBS9Jm94TB9SNZCsnDnVlFQgggZDZD"
}
```

> POST /api/v1/session/facebook fail result looks like this:

```json
{
  "error": "unauthorized"
}
```
Method | Path | Params
-------------- | -------------- | --------------
POST | /api/v1/session | email, password
POST | /aii/v1/session/facebook | facebook_access_token
POST | /aii/v1/session/linkedin | facebook_access_token