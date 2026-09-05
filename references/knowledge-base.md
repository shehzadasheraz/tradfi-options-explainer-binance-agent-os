# TradFi & Options Knowledge Base

This is the full content bank used for both Explain mode and Quiz mode. Each entry has the concept, a plain-language explanation, and the quiz question, options, and correct answer where applicable.

## Options Basics

Calls and Puts: A Call option gives the holder the right to buy the underlying at the strike price. A Put option gives the holder the right to sell the underlying at the strike price.
Quiz: Which statement about Calls and Puts is correct? A) Call = right to sell, Put = right to buy. B) Call = right to buy, Put = right to sell (correct). C) Both give the right to sell. D) Neither gives any right.

Strike Price: the predetermined price at which the option can be exercised, fixed when the contract is created.
Quiz: What is an option's strike price? A) Option's trading fee. B) Predetermined exercise price (correct). C) Current market price. D) Time to expiration.

Theta: measures how much an option's price decays as time passes, all else equal.
Quiz: In Options, what does Theta measure? A) The perpetual funding rate. B) Sensitivity to volatility. C) Price change as time decreases (correct). D) Strike price movement.

Maximum loss for an option buyer: buying an option caps your maximum loss at the premium paid, unlike selling or writing options.
Quiz: What is the maximum loss for a Commodity Option buyer? A) The premium paid (correct). B) The strike price. C) The contract's full value. D) Unlimited.

In-the-money expiration: if a Commodity Option is in-the-money at expiration, it is automatically exercised rather than expiring worthless.
Quiz: What happens to an in-the-money Commodity Option at expiration? A) It is automatically exercised (correct). B) It automatically renews. C) It becomes a perpetual contract. D) It expires worthless.

## Binance Commodity Options Specifics

Expiry structures: short-dated expiries, one day and one week.
Quiz: Which expiry structures are available for Binance Commodity Options? A) One hour and four hours. B) They have no expiry. C) One day and one week (correct). D) One month and one year.

Exercise style: European-style, meaning they can only be exercised at expiration, not any time before.
Quiz: What exercise style do Binance Commodity Options use? A) Perpetual-style. B) European-style (correct). C) American-style. D) Asian-style.

Retail user actions: retail users can buy to open and sell to close, standard long-only options access.
Quiz: Which action is available to retail Commodity Options users? A) Short-sell without margin. B) Buy to open and sell to close (correct). C) Sell to open only. D) Write uncovered calls.

## Binance TradFi Perpetuals Specifics

Trading hours: TradFi Perpetuals trade 24/7, same as crypto perpetuals.
Quiz: When can Binance TradFi Perpetuals be traded? A) Weekends only. B) 24/7 (correct). C) Only during US market hours. D) Only during pre-market.

Expiry: TradFi Perpetuals have no expiry date, just like crypto perpetual futures.
Quiz: Do Binance TradFi Perpetuals have an expiry date? A) Yes, every week. B) Yes, every quarter. C) No, they have no expiry date (correct). D) Yes, every month.

Asset categories: equities, ETFs, and commodities, tokenized traditional-market exposure traded perpetually.
Quiz: Which asset categories have been included among Binance TradFi Perpetuals? A) Equities, ETFs and commodities (correct). B) Fiat currencies only. C) NFTs and gaming items. D) Real estate tokens.

Weekend pricing mode: since underlying markets close on weekends but TradFi Perps trade 24/7, Binance uses Orderbook EWMA Mode, an exponentially weighted moving average based on the perpetual's own order book.
Quiz: Which index mode applies to equity and commodity TradFi Perps on weekends? A) Fixed Price Mode. B) Auction Mode. C) Orderbook EWMA Mode (correct). D) Last Price Mode.

## General Futures and Perps Mechanics

Mark Price vs Last Price: Mark Price triggers liquidation, using an index and funding based calculation to smooth out short-term wicks or manipulation.
Quiz: Which price triggers the liquidation of a Binance Futures position? A) Mark Price (correct). B) Last Price. C) Strike Price. D) None of the above.

Funding rate direction: when funding rate is positive, long-position holders pay short-position holders, since the perp price trades above the underlying index.
Quiz: When a perpetual contract's funding rate is positive, who pays the funding fee? A) Long-position holders pay short-position holders (correct). B) Short-position holders pay long-position holders. C) No funding payment occurs. D) Binance pays both sides.

## Live Data Reference

For live price checks, use Binance Agent OS with contractType TRADIFI_PERPETUAL on the continuous contract kline endpoint. Supported pairs follow the format TICKER plus USDT, for example AAPLUSDT, NVDAUSDT, TSLAUSDT, for tokenized equities included in the TradFi Perpetuals program. Always confirm the pair is a real supported TradFi Perp before quoting a price, since not every stock ticker will have a corresponding perpetual pair.
