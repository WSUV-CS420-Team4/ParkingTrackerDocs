#API Information

## Data Upload Format

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

## Date Format

http://en.wikipedia.org/wiki/ISO_8601#Combined_date_and_time_representations


## Blockface Submission Endpoint

`http://parking.bitsrc.net/api/v1/blockfaces`    ←- POST
