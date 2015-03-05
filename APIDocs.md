#API Information

## Data Submission

### JSON Format

```json
{
  "blockfaces": [
    {
      "block": 4,
      "face": "A",
      "stalls": [
        {
          "plate": "AGP2556",
          "time": "2007-04-05T12:30:05-08:00",
          "attr": ["HC","RP"]
        }]
    }
  ]
}
```

[Date Format](http://en.wikipedia.org/wiki/ISO_8601#Combined_date_and_time_representations) (ISO 8601)


### Endpoint

`POST https://bend.encs.vancouver.wsu.edu/~jason_moss/api/v1/blockfaces`

## Authentication

### Token Management

#### Endpoint

`POST https://bend.encs.vancouver.wsu.edu/~jason_moss/api/v1/login`

#### Input

POST'd JSON object:
```json
{
"Username": "Test",
"Password": "test"
}
```

#### Output

```json
{
"Token": "46301dc2a36e0e1636b71dd2f08cec6adc6e2f87c3fe29c15609a65fdd143931"
}
```

### Requests

To make an authenticated request to the API, include the header `X-Auth-Token: <TOKEN>` with the request.
If the request is not succesfully authenticated, for cases such as the token is incorrect, the token has expired, or
an admin has invalidated a token, the result will be `401 Unauthorized`
