---
title: API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='http://stocksearchapi.com/accounts/register/'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Stock Search API! You can use our API to lookup stock symbols (tickers) associated with publicly traded companies, ETFs and funds trading on US exchanges.  To date we have over 8000 listed securities.

# Authentication

Stock Search uses API keys to allow access to the API. You can register a new API key by [signing up](http://stocksearchapi.com/accounts/register/).

Stock Search expects an API key to be included in all API requests to the server in a GET field:

`api_key=YOUR_API_KEY`

<aside class="notice">
You must replace <code>YOUR_API_KEY</code> with your personal API key.
</aside>

# Search

## Search by symbol OR company name

```shell
curl "http://stocksearchapi.com/api/?search_text=USER_SEARCH_INPUT&api_key=YOUR_API_KEY"
```

> Replacing USER_SEARCH_INPUT with "f" would return JSON structured like this:

```json
[
  {
    "company_name": "Facebook, Inc.",
    "company_symbol": "FB",
    "listing_exchange": "NASDAQ"
  },
  {
    "company_name": "First Trust New Opportunities MLP & Energy Fund ",
    "company_symbol": "FPL",
    "listing_exchange": "NYSE"
  },
  {
    "company_name": "FedEx Corporation ",
    "company_symbol": "FDX",
    "listing_exchange": "NYSE"
  },
  {
    "company_name": "Ford Motor Company ",
    "company_symbol": "F",
    "listing_exchange": "NYSE"
  },
]
```

<aside class="notice">
A maximum of <code>10</code> results will be returned per search.
</aside>

This endpoint allows retrieval of a company based on its (partial) symbol or name

### HTTP Request

`GET http://stocksearchapi.com/api/?search_text=USER_SEARCH_INPUT&api_key=YOUR_API_KEY`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
search_text | YES | A character that is a substring of a company symbol or company name
api_key | YES | YOUR_API_KEY

<aside class="warning">
Remember — Neither <code>search_text</code> nor <code>api_key</code> should be empty
</aside>

