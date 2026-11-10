# DJI official store prices by country (daily)

The prices DJI shows on its **official online store in 42 countries**, collected once a day by [DJI Index](https://djiindex.com/) and converted to US dollars at dated exchange rates. Use it to compare what the same DJI drone, camera, gimbal or microphone costs in each country.

- **Live site:** https://djiindex.com/: every product's price in every store, updated daily
- **Which country is cheapest today:** https://djiindex.com/cheapest-country-to-buy-dji/
- **Monthly report:** [DJI Global Price Index](https://djiindex.com/reports/)
- **How the data is collected:** https://djiindex.com/methodology/

## Files

| File | What it is |
|------|------------|
| `data/latest-prices.json` | Every DJI product with a store price: each store's price, currency, tax status, date checked and store URL, plus the cheapest compared store. Schema: https://djiindex.com/data/openapi.json |
| `data/cheapest-by-product.csv` | One row per product: the cheapest DJI store that day, its price, the price in US dollars and the date. |
| `data/history/YYYY/YYYY-MM-DD-cheapest-by-product.csv` | A dated copy of the CSV for every daily store check since this repository started. |
| `reports/YYYY-MM-price-index.csv` | Each monthly edition of the DJI Global Price Index: a fixed basket of popular DJI products priced in every DJI store. |

The files are copied from https://djiindex.com/data/ by a scheduled GitHub Action ([`.github/workflows/sync.yml`](.github/workflows/sync.yml)) a couple of hours after the site's daily store check.

## Notes on the numbers

- Prices are **DJI's own listed prices** on its official online stores, not reseller or street prices, with the date each was checked.
- US, Canadian and Puerto Rican store prices are **before sales tax**, so they are listed but not ranked against tax-inclusive prices.
- Prices exclude shipping, import duty and local taxes you may owe when you bring a product home. Drone imports are restricted in some countries; check the rules first.
- Products are matched by barcode (EAN), so a Fly More Combo is never compared with a base kit.

## Licence and citation

The data is published under **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**. Credit **DJI Index** with a link to https://djiindex.com/, for example:

> Source: DJI Index (https://djiindex.com/), DJI official store prices, 10 Nov 2026.

For papers, see [`CITATION.cff`](CITATION.cff).

DJI Index is independent and not affiliated with or endorsed by DJI. DJI and all product names are trademarks of their respective owners.
