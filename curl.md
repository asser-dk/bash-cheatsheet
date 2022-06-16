# Curl

Curl is a tool for transfering data to or from a server. It supports a huge array of protocols such as ftp, http, telnet, etc.

## HTTP

### GET requests

By default if you only give curl a URL it will interpret it as a GET request

```bash
curl http://example.com
```

> **Note:** If passing in longer URL's with query parameters it is usually wise to wrap the entire url in "quotes" to prevent any issues with parameters not being passed along.

## Further reading:

* [https://curl.se docs on http scripting](https://curl.se/docs/httpscripting.html)
