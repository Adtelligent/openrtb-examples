# Sample 2: Video mobile

Headers:
```$xslt
 -H 'Content-Type: application/json' 
 -H 'x-openrtb-version: 2.5.1' 
```
Request:
```json
{
   "id":"0C3FAEFB58D44111",
   "imp":[
      {
         "id":"C8C21CC5ABDE47A1",
         "video":{
            "mimes":[
               "video/x-flv",
               "video/mp4",
               "application/x-shockwave-flash",
               "application/javascript"
            ],
            "minduration":0,
            "maxduration":30,
            "protocols":[
               1,
               2,
               3,
               4,
               5,
               6
            ],
            "w":728,
            "h":90,
            "startdelay":0,
            "api":[
               1,
               2
            ]
         },
         "bidfloor":0.15,
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
   "at":2,
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
    "id": "0C3FAEFB58D44111",
    "seatbid": [
        {
            "bid": [
                {
                    "id": "p0mOnVxy9UjVfyI8",
                    "impid": "C8C21CC5ABDE47A1",
                    "price": 0.3304,
                    "adid": "YXxw4Pijx0eKi6K",
                    "nurl": "http://adsn.adtelligent.com/tracking/win?adid=4B3EBFD207842AA6&event=nurl&price=${AUCTION_PRICE}",
                    "adomain": [
                        "http://adtelligent.com"
                    ],
                    "crid": "123456a789",
                    "attr": [],
                    "w": 728,
                    "h": 90,
                    "burl": "http://adsn.adtelligent.com/tracking/win?adid=4B3EBFD207842AA6&event=burl&price=${AUCTION_PRICE}",
                    "lurl": "http://adsn.adtelligent.com/tracking/lurl?adid=4B3EBFD207842AA6",
                    "ext": {
                        "avn": "Adtelligent LLC",
                        "agn": "Adtelligent LLC"
                    }
                }
            ],
            "seat": "1"
        }
    ],
    "bidid": "0C3FAEFB58D44111",
    "cur": "USD"
}```