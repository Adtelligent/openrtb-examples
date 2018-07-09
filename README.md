# Real Time Bidding (RTB) Project 
# Adtelligent Bid Request/Response Samples

## OpenRTB Version HTTP Header
The OpenRTB Version should be passed in the header of a bid request with a custom header parameter. This will allow bidders to recognize the version of the message contained before attempting to parse the request.
Adtelligent supports 2.2 - 2.5 OpenRTB version
Please, specify the preferred OpenRTB version in the header:
```$xslt
X-openrtb-version: 2.5
```

OpenRTB 2.3 version is used by default

## Transport
The base protocol between an exchange and its bidders is HTTP. Specifically, HTTP POST is required for bid requests to accommodate greater payloads than HTTP GET and facilitate the use of binary representations. Win notices may be either POST or GET at the discretion of the exchange.

Calls returning content (e.g., any bid response, a win notice that returns markup) should return HTTP code 200. Calls returning no content in response to valid requests (e.g., an empty bid response which is one option for indicating no-bid, a win notice that does not return markup) should return HTTP 204. Invalid calls (e.g., a bid request containing a malformed or corrupt payload) should return HTTP 400 with no content.

Adtelligent response codes:
- HTTP 204 No Ads
- HTTP 200 Bid response
- HTTP 400 Invalid request

## Samples
### [Sample 1: Video desktop](./video-desktop.md)

### [Sample 2: Video mobile](./video-mobile.md)

### [Sample 3: Banner desktop](./banner-desktop.md)

### [Sample 4: Banner mobile](./banner-mobile.md)


