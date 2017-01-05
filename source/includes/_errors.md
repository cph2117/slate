# Errors

Stock Symbol Search API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Missing <code>search_text</code> parameter
401 | Unauthorized -- Your API key is incorrect or missing
404 | Not Found -- No corresponding symbols could be found
429 | Too Many Requests -- You have exceeded your allotted API request limit
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
