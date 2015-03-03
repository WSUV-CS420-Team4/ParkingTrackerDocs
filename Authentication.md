# Authentication

## Token Management

### Endpoint

http://bend.encs.vancouver.wsu.edu/~jason_moss/api/v1/login

### Input

POST'd JSON object:
```json
{
"Username": "Test",
"Password": "test"
}
```

### Output

```json
{
"Token": "46301dc2a36e0e1636b71dd2f08cec6adc6e2f87c3fe29c15609a65fdd143931"
}
```

## Requests

To make an authenticated request to the API, include the header `X-Auth-Token: <TOKEN>` with the request.
If the request is not succesfully authenticated, for cases such as the token is incorrect, the token has expired, or
an admin has invalidated a token, the result will be `401 Unauthorized`
