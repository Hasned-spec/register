# hasned.dev API

Free, no-login JSON utilities for developers. Base URL: `https://hasned.is-a.dev/x402/paid`

All endpoints accept `GET` (query params) and `POST` (JSON body). Responses are JSON:
`{"ok": true, ...}` or `{"ok": false, "error": "..."}`.

## Tools

| Tool | Params | Example |
|------|--------|---------|
| hash | `text`, optional `algo` (sha256 default) | `/hash?text=hello` |
| uuid | none | `/uuid` |
| base64 | `text`, optional `decode=true` | `/base64?text=aGk=` |
| qrcode | `text` | returns QR as SVG |
| csv2json | `csv` | `/csv2json?csv=name%2Cage` |
| json2csv | `json` | array of flat objects |
| yaml2json | `yaml` | YAML string |
| jwt-decode | `token` | header+payload, no verification |
| dns-lookup | `domain`, optional `type` | A/AAAA/MX/TXT |
| whois | `domain` | raw record |
| geoip | `ip` or `host` | country/city/ASN |
| crypto-price | `ids`, optional `vs` | CoinGecko ids |
| fx-rates | `base`, optional `symbols` | ECB reference rates |
| wayback | `url` | latest archive snapshot |
| html2md | `url` | page converted to Markdown |
| weather | `q` (city) | current conditions |

## Limits

Rate-limited per IP to keep the service free for everyone.
No accounts, no API keys, no tracking.
