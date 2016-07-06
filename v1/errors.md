Request Status | HTTP Status | Description
-------------- | ----------- | ------------
`OK`             | 200         | The request had a successful response
`NOT_AUTHORIZED_ERROR` | 403 | The request is unauthorized
`QUERY_LIMIT_ERROR` | 409 | The client reached the query limit
`SERVER_FAULT_ERROR` | 500 | The server triggered an internal error for the request
`NOT_FOUND_ERROR` | 404 | The request is invalid
