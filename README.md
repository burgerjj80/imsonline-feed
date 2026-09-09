# imsonline-feed

Auto-published **Meta / Facebook product catalog feed** for [IMS Online](https://imsonline.co.za).

A scheduled GitHub Action ([`.github/workflows/publish-feed.yml`](.github/workflows/publish-feed.yml))
pulls `https://imsonline.co.za/feed/facebook.xml` from the storefront every 4 hours and
republishes it to **GitHub Pages**, so Meta fetches it from GitHub's CDN instead of the
origin (which rate-limits rapid crawler bursts).

**Feed URL for Meta Commerce Manager:**

```
https://burgerjj80.github.io/imsonline-feed/facebook.xml
```

The feed is the standard Google Merchant / Meta RSS spec (in-stock products only, ZAR,
prices incl. VAT). It contains only public storefront product data — no secrets.
