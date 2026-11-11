---
title: PriceSaver bot
---

# PriceSaver bot

PriceSaver is a price-alert app for shoppers in Finland. Users save a product link from an online shop, and the app tells them when the price drops.

Our price checker identifies itself with this User-Agent:

```
PriceSaverBot/1.0 (+https://pricesaver.github.io/bot/)
```

## What it does
- It reads only **public product pages** that a user of the app has saved or pasted. It does not crawl shops, follow links or read search pages.
- It reads the product name, price, currency, image link and available sizes.
- It never logs in, never adds anything to a cart and never collects personal data.

## How often
- Each saved product is checked **at most about twice a day**, plus once when a user pastes a new link.
- Requests to one shop are spaced at least **5 seconds** apart, and results are cached.

## Rules it follows
- It respects **robots.txt**. Pages that robots.txt disallows are not fetched.
- If a shop blocks it or shows a challenge page, it **stops** for that shop and does not try to get around the block.

## Contact and opt-out
If you run a shop and want us to stop checking your pages, or you have any question, please [open an issue](https://github.com/PriceSaver/pricesaver.github.io/issues/new). We stop checking a shop as soon as it asks.
