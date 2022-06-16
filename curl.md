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

### Errors

Errors I've encountered and how to fix them.

#### "Bad range in URL position..."

This error is probably caused if you have brackets in your url (`https://example.com?foo[0]=bar`). In order to avoid curl from interpreting it as a range add the `-g/--globoff` option to your call.

> `-g/--globoff`
> ```
> This  option  switches  off  the "URL globbing parser". When you set this option, you can
> specify URLs that contain the letters {}[] without having them being interpreted by  curl
> itself.  Note  that  these  letters  are not normal legal URL contents but they should be
> encoded according to the URI standard.```
