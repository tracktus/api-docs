
##### Request URL

`http://*.localize.cc/api/`

##### Authentication

The authentication for the version 1 of the API is strictly based on the HTTP Header.

HTTP Header | Description
----------- | ----------------
X-Client-Id | Your REST Client ID
X-Client-Secret | Your REST Client Secret

Every API request must have the headers above set.

##### Errors

Request Status | HTTP Status | Description
-------------- | ----------- | ------------
`OK`             | 200         | The request had a successful response
`REQUEST_ERROR` | 400 | The request triggered an user level error
`NOT_AUTHORIZED_ERROR` | 403 | The request is unauthorized
`NOT_FOUND_ERROR` | 404 | The request is invalid
`QUERY_LIMIT_ERROR` | 409 | The client reached the query limit
`SERVER_FAULT_ERROR` | 500 | The server triggered an internal error for the request
