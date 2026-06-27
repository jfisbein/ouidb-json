# ouidb-json

JSON (and raw) version of the IEEE OUI database, published from `http://standards-oui.ieee.org/oui/oui.txt`.

It is updated every night by [ouidb-to-json-publisher](https://github.com/jfisbein/ouidb-to-json-publisher), which only commits when the upstream IEEE data actually changes.

## Published files

| File | Description |
|---|---|
| `ouidb.json` | The OUI database parsed and converted to JSON |
| `ouidb.json.gz` / `ouidb.json.bz2` | Compressed variants of `ouidb.json` |
| `oui.txt` | The raw IEEE `oui.txt`, mirrored verbatim |
| `oui.txt.gz` / `oui.txt.bz2` | Compressed variants of `oui.txt` |
| `ouidb.schema.json` | JSON Schema describing `ouidb.json` |

This repo also acts as a **mirror of the raw `oui.txt`**. The IEEE host sits behind an anti-bot WAF that blocks many datacenter / cloud IP ranges (the connection is dropped before HTTP), so downloading `oui.txt` directly often fails from CI runners and cloud servers. If that happens to you, fetch it from here instead.

### Direct (raw) URLs

- JSON: `https://raw.githubusercontent.com/jfisbein/ouidb-json/master/ouidb.json`
- JSON (gzip): `https://raw.githubusercontent.com/jfisbein/ouidb-json/master/ouidb.json.gz`
- JSON (bzip2): `https://raw.githubusercontent.com/jfisbein/ouidb-json/master/ouidb.json.bz2`
- Raw `oui.txt`: `https://raw.githubusercontent.com/jfisbein/ouidb-json/master/oui.txt`
- Raw `oui.txt` (gzip): `https://raw.githubusercontent.com/jfisbein/ouidb-json/master/oui.txt.gz`
- Raw `oui.txt` (bzip2): `https://raw.githubusercontent.com/jfisbein/ouidb-json/master/oui.txt.bz2`

## JSON format
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
