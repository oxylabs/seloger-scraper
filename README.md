# Seloger Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Seloger Scraper](https://oxylabs.io/products/scraper-api/web/seloger?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Seloger website effortlessly. This brief guide explains how an Seloger Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Seloger results by providing your own URLs to our service. We can return the HTML for any Seloger page you like.

#### Python code example

The example below illustrates how you can get HTML of Seloger page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.seloger.com/immobilier/locations/immo-paris-75/bien-appartement/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/seloger-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang=\"fr\">\n<head>\n    <meta charset=\"utf-8\" />\n    <meta name=\"viewport\" conte ... </html>",
      "created_at": "2023-12-18 10:43:56",
      "updated_at": "2023-12-18 10:43:59",
      "page": 1,
      "url": "https://www.seloger.com/immobilier/locations/immo-paris-75/bien-appartement/",
      "job_id": "7142464496181775361",
      "status_code": 200
    }
  ]
}
```
With our Seloger Scraper, you can seamlessly gather publicly available information from any Seloger web page. Collect essential property details, such as listing price, user reviews, or property descriptions, to understand the real estate market and stay a step ahead of your competitors. If you have any queries, feel free to reach out to our support team via live chat or email us at hello@oxylabs.io.