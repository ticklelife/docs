# General API Guidelines

## Response Codes

**200 OK**: Everything is fine

**400 BAD REQUEST**: Request body passed is incorrect

**403 FORBIDDEN**: API Key invalid or user invalid

**429 TOO MANY REQUESTS**: If we get too many requests. Current limit: 10/minute.

**204 NO CONTENT**: If there are no articles matching the criteria
