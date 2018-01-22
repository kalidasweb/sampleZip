# Get Currency List


**URL** : ` /api/?action=FindRequest&service=cmms&accessKey=<Access Key>&appKey=<App Key>&timestamp=<Current Timestamp>&signatureVersion=1&signatureMethod=HmacSHA256 HTTP/1.1`

**Method** : `POST`

**Headers** : 

	Authorization: '<Auth token>'
	Content-Type: 'text/plain'

**Request PayLoad** : 
```json
{
    "className": "Currency",
    "fields": "id, strDescription, strISOCode, strName, strSymbol",
    "_maCn": "FindRequest",
    "requestId": 0,
    "requestSentUnixTime": <CurrentTimestamp>,
    "clientVersion": {
        "major": 2,
        "minor": 3,
        "patch": 1,
        "preRelease": "alpha",
        "metadata": null
    }
}
```



## Success Response

**Code** : `200 OK`

**Content examples**

```json

{
  "_maCn" : "FindResponse",
  "serverVersion" : {
    "major" : 2,
    "minor" : 3,
    "patch" : 1,
    "preRelease" : "alpha"
  },
  "sync" : {
    "revision" : 0,
    "needToSync" : false,
    "dateLastUpdated" : 1515757287000
  },
  "objects" : [ {
    "className" : "Currency",
    "id" : 1,
    "strISOCode" : "USD",
    "strName" : "US Dollar",
    "strSymbol" : "$",
    "dirty" : false,
    "new" : false,
    "uideleted" : false
  }
   ],
  "totalObjects" : 1
}
```

## Notes

* <> represents the values need pass

For more Details check out  : https://fiixlabs.github.io/api-documentation/#/ApiDoc#Authentication
