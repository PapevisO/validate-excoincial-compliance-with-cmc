# validate-excoincial-compliance-with-cmc

## Prototype sample

Ideal API Endpoint Samples
\( issued by Coinmarketcap on 2 Sep 2019 \)

[sample description link](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg/edit)

Name | Category | Link on Excoincial and mapping sample_name:excoincial_name | Status | Description | Link to sample
--- | --- | --- | --- | --- | ---
Summary Endpoint | | | | Overview of market data for all tickers. | [bitrue sample](https://www.bitrue.com/kline-api/public.json?command=returnTicker)
Endpoint 1 | /assets | **[/v2/currencies](https://excoincial.com/api/v2/currencies) available fields mapping** \["name":"name", "min_withdraw":"min_withdraw_amount", "max_withdraw":"withdraw_limit_24h"\] **[/v2/fees/trading](https://excoincial.com/api/v2/fees/trading) available fields mapping** \["maker_fee","\{market_id_with_currency_as_base\}:ask_fee:value", "taker_fee","\{market_id_with_currency_as_base\}:bid_fee:value"\] *No_endpoint* **suggested_hardcode_mappings** \["can_withdraw":"true", "can_deposit":"true", "maker_fee":"0.0015", "taker_fee":"0.0015"\]| | In depth details on crypto currencies available on the exchange. | [CMC description ENDPOINT_1](https://docs.google.com/document/d/1S4urpzUnO2t7DmS_1dc4EL4tgnnbTObPYXvDeBnukCg/edit#bookmark=id.yu07m9vl46wn)
 
