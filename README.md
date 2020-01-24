# validate-excoincial-compliance-with-cmc

## Prototype sample

Ideal API Endpoint Samples
\( issued by Coinmarketcap on 2 Sep 2019 \)

[sample description link](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg/edit)

Name | Category | Link on Excoincial and mapping sample_name:excoincial_name | Status | Description | Link to sample
--- | --- | --- | --- | --- | ---
<sub>Summary Endpoint</sub> | | | | Overview of market data for all tickers. | [bitrue sample](https://www.bitrue.com/kline-api/public.json?command=returnTicker)
<sub>Endpoint&nbsp;1</sub> | /assets | **[/v2/currencies](https://excoincial.com/api/v2/currencies) available fields mapping**<br>\["name":"name", <sub>"min_withdraw":"min_withdraw_amount"</sub>, <sub>"max_withdraw":"withdraw_limit_24h"</sub>\] **[/v2/fees/trading](https://excoincial.com/api/v2/fees/trading)<br>suggested fields walkaround**<br>\["maker_fee":<sub>"\{market_id&nbsp;with&nbsp;currency&nbsp;as&nbsp;base\}::ask_fee::value"</sub>, "taker_fee":<sub>"\{market_id&nbsp;with&nbsp;currency&nbsp;as&nbsp;base\}::bid_fee::value"</sub>\]<br>*No&nbsp;endpoint* **suggested_hardcode_mappings**<br>\["can_withdraw":"true", "can_deposit":"true", "maker_fee":"0.0015", "taker_fee":"0.0015"\]| Compliant with mandatory | In depth details on crypto currencies available on the exchange. | [CMC description ENDPOINT_1](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg/edit#bookmark=id.yu07m9vl46wn)
<sub>Endpoint&nbsp;2</sub> | /ticker | **[/v2/tickers](https://excoincial.com/api/v2/tickers)<br>available fields mapping**<br>\["last_price":"last", "base_volume":"volume", "quote_volume":"quote_volume"\]<br>*No&nbsp;endpoint* **suggested_hardcode_mappings**<br>\["isFrozen":"0"\]<br>**!disabled markets are not reflected in API responses!** | Compliant with mandatory | 24-hour rolling window price change statistics for all markets. | [CMC description ENDPOINT_2](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg/edit#bookmark=id.vs2pdh9rb8fa)
<sub>Endpoint&nbsp;3</sub> | /orderbook | **[/v2/depth?market=market_pair](https://excoincial.com/api/v2/depth?market=btcusd&limit=300)<br>available parameters mapping**<br>\["market_pair":"market", "depth":"limit"\]<br>**available fields mapping**<br>\["timestamp":"timestamp", "asks":"asks",  "bids":"bids"\] | Compliant with mandatory | Market depth of a trading pair. One array containing a list of ask prices and another array containing bid prices. Query for level 2 order book with full depth available as minimum requirement. | [CMC description ENDPOINT_3](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg/edit#bookmark=id.9caev86c3vcc)
