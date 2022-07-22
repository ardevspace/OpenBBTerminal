```
usage: cgstables [-l N] [-s {Rank,Name,Symbol,Price,Change_24h,Exchanges,Market_Cap,Change_30d}] [--export {csv,json,xlsx}] [-h]
```

Shows stablecoins by market capitalization. Stablecoins are cryptocurrencies that attempt to peg their market value to some external reference like
the U.S. dollar or to a commodity's price such as gold. You can display only N number of coins with --limit parameter. You can sort data by Rank,
Name, Symbol, Price, Change_24h, Exchanges, Market_Cap, Change_30d with --sort.

```
optional arguments:
  -l N, --limit N     display N number records (default: 15)
  -s {Rank,Name,Symbol,Price,Change_24h,Exchanges,Market_Cap,Change_30d}, --sort {Rank,Name,Symbol,Price,Change_24h,Exchanges,Market_Cap,Change_30d}
                        Sort by given column. Default: Rank (default: Rank)
  --pie                 displays market cap distribution across stablecoins
  --export {csv,json,xlsx}
                        Export dataframe data to csv,json,xlsx file (default: )
  -h, --help            show this help message (default: False)
```

Example:
```
2022 Feb 15, 08:16 (✨) /crypto/ov/ $ cgstables

First 15 stablecoins have a total 182.582 B dollars of market cap.

                                                                     Stablecoin Data
┌─────────┬──────────────────────┬───────────┬────────────────┬─────────────────┬────────────────┬───────────────┬────────────┬──────────────────────────┐
│ Symbol  │ Name                 │ Price [$] │ Market Cap [$] │ Market Cap Rank │ Change 24h [%] │ Change 7d [%] │ Volume [$] │ Percentage [%] of top 15 │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ usdt    │ Tether               │ 1.001     │ 78.556 B       │ 3               │ -0.014         │ -0.063        │ 43.035 B   │ 43.025                   │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ usdc    │ USD Coin             │ 1         │ 52.519 B       │ 5               │ 0.120          │ -0.052        │ 2.976 B    │ 28.765                   │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ busd    │ Binance USD          │ 1.001     │ 17.557 B       │ 13              │ 0.041          │ -0.105        │ 3.124 B    │ 9.616                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ ust     │ TerraUSD             │ 1.001     │ 11.616 B       │ 17              │ 0.132          │ -0.053        │ 318.818 M  │ 6.362                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ dai     │ Dai                  │ 1.001     │ 9.820 B        │ 19              │ 0.069          │ 0.059         │ 237.136 M  │ 5.378                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ mim     │ Magic Internet Money │ 1.001     │ 2.788 B        │ 51              │ 0.419          │ 0.107         │ 42.304 M   │ 1.527                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ frax    │ Frax                 │ 1.001     │ 2.660 B        │ 53              │ 0.553          │ -0.490        │ 25.748 M   │ 1.457                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ tusd    │ TrueUSD              │ 1.001     │ 1.487 B        │ 80              │ 0.014          │ 0.017         │ 92.185 M   │ 0.814                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ usdp    │ Pax Dollar           │ 1.001     │ 1.034 B        │ 100             │ -0.164         │ -0.003        │ 13.857 M   │ 0.566                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ fei     │ Fei USD              │ 1.002     │ 556.435 M      │ 147             │ 0.248          │ -0.048        │ 14.805 M   │ 0.305                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ lusd    │ Liquity USD          │ 1.010     │ 498.292 M      │ 159             │ 0.210          │ 0.038         │ 6.557 M    │ 0.273                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ usdn    │ Neutrino USD         │ 0.999     │ 443.663 M      │ 169             │ 1.023          │ 0.073         │ 11.068 M   │ 0.243                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ xaut    │ Tether Gold          │ 1.851 K   │ 418.617 M      │ 173             │ 2.029          │ -0.250        │ 4.853 M    │ 0.229                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ mimatic │ MAI                  │ 0.999     │ 264.095 M      │ 235             │ 0.043          │ 0.085         │ 3.754 M    │ 0.145                    │
├─────────┼──────────────────────┼───────────┼────────────────┼─────────────────┼────────────────┼───────────────┼────────────┼──────────────────────────┤
│ husd    │ HUSD                 │ 1.005     │ 263.061 M      │ 236             │ 0.686          │ 0.524         │ 35.886 M   │ 0.144                    │
└─────────┴──────────────────────┴───────────┴────────────────┴─────────────────┴────────────────┴───────────────┴────────────┴──────────────────────────┘
```