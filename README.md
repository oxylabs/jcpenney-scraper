# Jcpenney Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Jcpenney Scraper](https://oxylabs.io/products/scraper-api/ecommerce/jcpenney?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Jcpenney website effortlessly. This brief guide showcases how Jcpenney Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Jcpenney results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Jcpenney page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.jcpenney.com/g/women/view-all-women?id=cat10011030002'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/jcpenney-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en\" data-reactroot=\"\"><head><style id=\"app-inline-styles\">undefined</sty ... </html>",
      "created_at": "2024-02-20 12:53:43",
      "updated_at": "2024-02-20 12:53:44",
      "page": 1,
      "url": "https://www.jcpenney.com/g/women/view-all-women?id=cat10011030002",
      "job_id": "7165689981141259265",
      "status_code": 200
    }
  ]
}
```
With our Jcpenney Scraper, you can seamlessly pull public data from any Jcpenney web page. Gather necessary product details like current fashion trends, customer reviews, or product descriptions to keep track of market pulse and stay a step ahead of your competitors. Any doubts or queries? Our support team is just a live chat or an email away at hello@oxylabs.io.