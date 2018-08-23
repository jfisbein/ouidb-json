# ouidb-json

json version of the OUI Database published at https://linuxnet.ca/ieee/oui/

Using https://github.com/jfisbein/ouidb-to-json-publisher everyday it's updated with latest change (if any).

#### Format
```
[
  {
    "prefix": "000000",
    "organization": {
      "name": "Xerox Corporation",
      "address": {
        "line1": "M/S 105-50C",
        "line2": "Webster  NY  14580",
        "countryCode": "US"
      }
    }
  },
  {
    "prefix": "000001",
    "organization": {
      "name": "Xerox Corporation",
      "address": {
        "line1": "M/S 105-50C",
        "line2": "Webster  NY  14580",
        "countryCode": "US"
      }
    }
  }
  ....
  {
    "prefix": "FCFFAA",
    "organization": {
    "name": "IEEE Registration Authority",
    "address": {
      "line1": "445 Hoes Lane",
      "line2": "Piscataway NJ 08554",
      "countryCode": "US"
    }
  }
}
]
```
