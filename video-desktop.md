# Sample 1: Video desktop

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
   "site":{
      "id":"617682",
      "domain":"qwertyui.com",
      "page":"qwertyui.com",
      "publisher":{
         "id":"278066"
      }
   },
   "device":{
      "dnt":1,
      "ua":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_13_3) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36",
      "ip":"172.217.16.14",
      "geo":{
         "lat":37.419200000000004,
         "lon":-122.0574,
         "country":"USA"
      },
      "os":"Mac OS",
      "osv":"X 10_13_3",
      "w":728,
      "h":90,
      "devicetype":2
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
    "bidid": "0C3FAEFB58D44111",
    "cur": "USD",
    "id": "0C3FAEFB58D44111",
    "seatbid": [
        {
            "bid": [
                {
                    "adomain": [
                        "http://adtelligent.com"
                    ],
                    "attr": null,
                    "crid": "123456a789",
                    "id": "knupSligvYdMzO2T",
                    "impid": "C8C21CC5ABDE47A1",
                    "price": 1.75,
                    "adm": "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<VAST version=\"2.0\">\n <Ad id=\"qcWW7SLTLIGaHgmgsBeC\">\n  <InLine>\n   <AdSystem>adtelligent.com</AdSystem>\n   <AdTitle><![CDATA[ 82057.713253288.834430 ]]></AdTitle>\n   <Creatives>\n    <Creative sequence=\"1\">\n     <Linear>\n      <Duration>00:00:30</Duration>\n      <MediaFiles>\n       <MediaFile id=\"adtelligent.com\" delivery=\"progressive\" width=\"640\" height=\"360\" type=\"video/mp4\" bitrate=\"578\" scalable=\"true\" maintainAspectRatio=\"true\"><![CDATA[https://cdn.adtelligent.com/vpaid-tests/vm_passback_360.mp4?price=${AUCTION_PRICE}&cur=${AUCTION_CURRENCY}&imp=${AUCTION_IMP_ID}]]></MediaFile>\n      </MediaFiles>\n     </Linear>\n    </Creative>\n   </Creatives>\n  </InLine>\n </Ad>\n</VAST>",
                    "nurl": "http://adsn.adtelligent.com/tracking/win?adid=0C3FAEFB58D44111&event=nurl&price=${AUCTION_PRICE}",
                    "ext": {
                        "avn": "Adtelligent LLC",
                        "agn": "Adtelligent LLC"
                    },
                    "adid": "4SL8xwYXpzJT0PZ",
                    "w": 728,
                    "h": 90
                }
            ],
            "seat": "1",
            "group": 0
        }
    ]
}
```