# Sample 4: Banner mobile

Headers:
```$xslt
 -H 'Content-Type: application/json' 
 -H 'x-openrtb-version: 2.5.1' 
```
Request:
```json
{
   "id":"4B3EBFD207842A9A",
   "imp":[
      {
         "id":"D48DCA95E4C16676",
         "banner":{
            "w":120,
            "h":600,
            "mimes":[
               "image/jpeg",
               "image/png",
               "image/gif",
               "text/html",
               "application/javascript"
            ],
            "api":[
               1,
               2
            ]
         },
         "bidfloor":0.01,
         "bidfloorcur":"USD"
      }
   ],
  "app":{
     "id":"agltb3B1Yi1pbmNyDAsSA0FwcBiJkfIUDA",
     "name":"Yahoo Weather",
     "cat":[
        "IAB15",
        "IAB15-10"
     ],
     "ver":"1.0.2",
     "bundle":"12345",
     "storeurl":"https://itunes.apple.com/id628677149",
     "publisher":{
        "id":"agltb3B1Yi1pbmNyDAsSA0FwcBiJkfTUCV",
        "name":"yahoo",
        "domain":"www.yahoo.com"
     }
  },
  "device": {
   "ua": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.13 (KHTML, like Gecko) Version/5.1.7 Safari/534.57.2",
   "ip": "123.145.167.10"
  },
   "regs":{
      "ext":{
         "gdpr":0
      }
   },
   "user":{
      "id":"0413565179d2d91b"
   },
   "at":1,
   "tmax":500,
   "bcat":[
      "IAB26"
   ]
}
```

Expected response:

HTTP Status 200 OK

```json
{
    "id": "4B3EBFD207842A9A",
    "seatbid": [
        {
            "bid": [
                {
                    "id": "KkWjlSkkSLkY5NWR",
                    "impid": "D48DCA95E4C16676",
                    "price": 1.0569,
                    "adid": "ldPJzX9mA0KLIyq",
                    "nurl": "http://adsn.adtelligent.com/tracking/win?adid=4B3EBFD207842AA0&event=nurl&price=${AUCTION_PRICE}",
                    "adm": "<script id=\"P4B3EBFD207842AA0\" type=\"text/javascript\" >(function(d){var wrapper = d.createElement(\"script\"); wrapper.id = \"W4B3EBFD207842AA0\";wrapper.type = \"text/javascript\";wrapper.src = \"http://adsn.adtelligent.com/display/?adid=4B3EBFD207842AA0&cb=867909738\";var s = d.getElementById(\"P4B3EBFD207842AA0\");s.parentNode.insertBefore(wrapper, s);}(document));</script><noscript><img border=\"0\" alt=\"\" src=\"http://adsn.adtelligent.com/tracking/error/?adid=4B3EBFD207842AA0&code=2505\"></noscript>",
                    "adomain": [
                        "http://adtelligent.com"
                    ],
                    "crid": "123456a789",
                    "attr": [],
                    "w": 120,
                    "h": 600,
                    "burl": "http://adsn.adtelligent.com/tracking/win?adid=4B3EBFD207842AA0&event=burl&price=${AUCTION_PRICE}",
                    "lurl": "http://adsn.adtelligent.com/tracking/lurl?adid=4B3EBFD207842AA0",
                    "ext": {
                        "avn": "Adtelligent LLC",
                        "agn": "Adtelligent LLC"
                    }
                }
            ],
            "seat": "1"
        }
    ],
    "bidid": "4B3EBFD207842A9A",
    "cur": "USD"
}
```