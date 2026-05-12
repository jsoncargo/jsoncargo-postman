# JSONCargo API — Postman Collection

[![Collection](https://img.shields.io/badge/Postman-Collection-orange?logo=postman)](JSONCargo_API.postman_collection.json)
[![API Docs](https://img.shields.io/badge/API-Reference-blue)](https://jsoncargo.com/documentation-api/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

The official Postman collection for the [JSONCargo](https://jsoncargo.com) container and vessel tracking API. 12 requests across 4 folders covering container tracking, vessel tracking, ports, terminals, and utilities.

---

## Import in two clicks

### Option A — Import files directly

1. Download both files:
   - [`JSONCargo_API.postman_collection.json`](JSONCargo_API.postman_collection.json)
   - [`JSONCargo_API.postman_environment.json`](JSONCargo_API.postman_environment.json)

2. In Postman: **Import** → drag and drop both files at once

3. Select the **JSONCargo API** environment from the environment dropdown (top-right corner)

4. Click the environment name → set your `api_key` value → **Save**

5. Run **🔧 Utilities → API Key Stats** to confirm everything works

### Option B — Import from URL

In Postman: **Import → Link** and paste:

```
https://raw.githubusercontent.com/jsoncargo/jsoncargo-postman/main/JSONCargo_API.postman_collection.json
```

Then repeat for the environment:

```
https://raw.githubusercontent.com/jsoncargo/jsoncargo-postman/main/JSONCargo_API.postman_environment.json
```

> **Get your API key** at [jsoncargo.com/pricing-plans](https://jsoncargo.com/pricing-plans/)

---

## What is in the collection

### 📦 Container Tracking

| Request | Description |
|---|---|
| Track a container | Full tracking details by container number |
| Track a container (with shipping_line) | Use when the prefix is shared across carriers |
| Get containers from Bill of Lading | Returns all container numbers on a BOL |

### 🚢 Vessel Tracking

| Request | Description |
|---|---|
| Vessel Basic | Live position, speed, course, navigation status |
| Vessel Pro | Adds departure port, draught, ATD, timezone |
| Vessel Bulk | Up to 100 vessels in one request |
| Vessel Finder | Search static registry by name, type, flag, tonnage |
| Vessel Specs | Full static specs for a specific vessel |

### 🏔 Ports and Terminals

| Request | Description |
|---|---|
| Port Finder | Search by name, country, type, or coordinates |
| Terminal Info | Terminal details by UN/LOCODE |

### 🔧 Utilities

| Request | Description |
|---|---|
| Prefix Lookup | Which shipping line owns a container prefix |
| API Key Stats | Plan name, requests used, requests remaining |

---

## The shipping_line parameter

Some container prefixes are shared across carriers. If you get a 404 on a container request, add `shipping_line` to your query. Use the **Prefix Lookup** request to check which line owns a given prefix.

Valid values: `MAERSK` `HAPAG_LLOYD` `HMM` `ONE` `EVERGREEN` `MSC` `CMA_CGM` `COSCO` `ZIM` `YANG_MING` `PIL`

---

## Environment variables

| Variable | Set by | Description |
|---|---|---|
| `api_key` | You | Your JSONCargo API key |
| `base_url` | Pre-set | API base URL — do not change |
| `requests_available` | Auto-updated | Remaining requests this month |
| `requests_total` | Auto-updated | Total monthly allowance |

`requests_available` and `requests_total` are automatically updated in your environment after every API Key Stats request.

---

## Support

- [jsoncargo.com/documentation-api](https://jsoncargo.com/documentation-api/)
- support@jsoncargo.com
