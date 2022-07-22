# coingecko-api-with-proxy-ip

[![CI](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ip)](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ip) [![codecov](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ip)](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ip) [![version](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ip)](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ipg)

The nodejs api library for accessing coingecko api v3 with proxy-ip , develop with typescript with zero dependencies

- [Official document here](https://www.coingecko.com/api/documentations/v3)

- [API document generated](https://github.com/StepanyanAlbert/coingeck-api-with-proxy-ip)


## Get started

```
npm install coingecko-api-with-proxy-ip

```

```js
import { CoinGeckoClient } from 'coingecko-api-with-proxy-ip';
const client = new CoinGeckoClient({
  timeout: 10000,
  autoRetry: true,
  localAddress:[ '37.186.114.54' ]
});
const trendingSearch = await client.trending();
```

## Options

- timeout (optional): The http timeout, default 30s
- autoRetry (optional): Auto retry if the http response code is 429 - to many request
- localAddress (optional) : proxy ip

## Supported API method

| Endpoint                                                   |                           function | tested? |
| ---------------------------------------------------------- | ---------------------------------: | :-----: |
| /ping                                                      |                      client.ping() |   ✅    |
| /simple/price                                              |               client.simplePrice() |   ✅    |
| /simple/token_price/:id                                    |             client.simplePriceId() |   ✅    |
| /simple/supported_vs_currencies                            | client.simpleSupportedCurrencies() |   ✅    |
| /coins/list                                                |                  client.coinList() |   ✅    |
| /coins/markets                                             |               client.coinMarkets() |   ✅    |
| /coins/:id                                                 |                    client.coinId() |   ✅    |
| /coins/:id/tickers                                         |             client.coinIdTickers() |   ✅    |
| /coins/:id/history                                         |             client.coinIdHistory() |   ✅    |
| /coins/:id/market_history                                  |       client.coinIdMarketHistory() |   ✅    |
| /coins/id/market_chart                                     |         client.coinIdMarketChart() |   ✅    |
| /coins/{id}/market_chart/range                             |    client.coinIdMarketChartRange() |   ✅    |
| /coins/{id}/status_updates                                 |       client.coinIdStatusUpdates() |   ✅    |
| /coins/{id}/ohlc                                           |                client.coinIdOHLC() |   ✅    |
| /coins/{id}/contract/{contract_address}                    |                  client.contract() |   ✅    |
| /coins/{id}/contract/{contract_address}/market_chart/      |       client.contractMarketChart() |   ✅    |
| /coins/{id}/contract/{contract_address}/market_chart/range |  client.contractMarketChartRange() |   ✅    |
| /exchanges                                                 |                 client.exchanges() |   ✅    |
| /exchanges/list                                            |              client.exchangeList() |   ✅    |
| /exchanges/{id}/tickers                                    |         client.exchangeIdTickers() |   ✅    |
| /exchanges/{id}/status_update                              |   client.exchangeIdStatusUpdates() |   ✅    |
| /exchanges/{id}/volume_chart                               |     client.exchangeIdVolumeChart() |   ✅    |
| /finance_platforms                                         |          client.financePlatforms() |   ✅    |
| /finance_products                                          |           client.financeProducts() |   ✅    |
| /indexes                                                   |                   client.indexes() |   ✅    |
| /indexes/{market_id}/{id}                                  |           client.indexesMarketId() |   ✅    |
| /indexes/list                                              |               client.indexesList() |   ✅    |
| /indexes/list_by_market_and_id/{market_id}/{id}            |           client.financeProducts() |   ✅    |
| /derivatives                                               |              client./derivatives() |   ✅    |
| /derivatives/exchanges                                     |     client./derivativesExchanges() |   ✅    |
| /derivatives/exchanges/{id}                                |   client./derivativesExchangesId() |   ✅    |
| /status_updates                                            |             client.statusUpdates() |   ✅    |
| /event                                                     |                    client.events() |   ✅    |
| //events/countries                                         |            client.eventCountries() |   ✅    |
| /events/types                                              |               client.eventsTypes() |   ✅    |
| /exchange_rates                                            |             client.exhangesRates() |   ✅    |
| /search/trending                                           |                  client.trending() |   ✅    |
| /global                                                    |                    client.global() |   ✅    |
| /status_updates                                            |             client.statusUpdates() |   ✅    |
| //global/decentralized_finance_defi                        |                client.globalDefi() |   ✅    |
