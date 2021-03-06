# Chainlink CoinGecko External Adapter

## Price API (default)

### Endpoint

https://api.coingecko.com/api/v3/simple/price

### Input Params

- `coinid`: The CoinGecko id of the coin to query (required if not using `from`)
- `base`, `from`, or `coin`: The ticker of the coin to query (required if not using `coinid`)
- `quote`, `to`, or `market`: The currency to convert to
- `endpoint`: The endpoint to use (defaults to "price", one of "price", "globalMarketCap", "dominance")

### Output

```json
{
  "jobRunID": "1",
  "data": {
    "ethereum": {
      "usd": 157.24
    },
    "result": 157.24
  },
  "result": 157.24,
  "statusCode": 200
}
```

## Global API

### Endpoint

https://api.coingecko.com/api/v3/global

### Input Params

- `market`, `to`, or `quote`: The ticker of the coin to query (required)
- `endpoint`: The endpoint to use (defaults to "price", one of "price", "globalMarketCap", "dominance")

### Output

```json
{
  "jobRunID": "1",
  "data": {
    "data": {
      "active_cryptocurrencies": 5957,
      "upcoming_icos": 0,
      "ongoing_icos": 52,
      "ended_icos": 3373,
      "markets": 541,
      "total_market_cap": {
        "btc": 30989831.79926188,
        "eth": 1002584380.7395577,
        "ltc": 7874292256.0918255,
        "bch": 1532212026.6933346,
        "bnb": 12865279127.650606,
        "eos": 146311079039.56436,
        "xrp": 1516169090335.9976,
        "xlm": 4552439205624.754,
        "link": 37340996120.73051,
        ...
      },
      "total_volume": {
        "btc": 3796204.0720707024,
        "eth": 122814958.57775663,
        "ltc": 964588014.5745924,
        "bch": 187693485.16268748,
        "bnb": 1575975801.6459033,
        "eos": 17922869592.737896,
        "xrp": 185728251510.49503,
        "xlm": 557666410137.1028,
        "link": 4574211388.00985,
        ...
      },
      "market_cap_percentage": {
        "btc": 59.76998558746993,
        "eth": 11.279054372152645,
        "usdt": 4.2918601818054105,
        "xrp": 2.9844952413180397,
        "bch": 1.2106035362038838,
        "bnb": 1.1507246890199336,
        "link": 1.050511825669937,
        "dot": 0.9735970943267678,
        "ada": 0.8605029833772749,
        "ltc": 0.8346408581868999
      },
      "market_cap_change_percentage_24h_usd": -0.2995489834770486,
      "updated_at": 1603237580
    },
    "result": 30989831.79926188
  },
  "result": 30989831.79926188,
  "statusCode": 200
}
```
