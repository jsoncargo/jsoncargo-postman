# JSONCargo API — Postman Collection

Postman collection for the [JSONCargo](https://jsoncargo.com) container and vessel tracking API. Covers all endpoints with working example requests.

Full documentation: [jsoncargo.com/documentation-api](https://jsoncargo.com/documentation-api/)

## Import into Postman

1. Open Postman
2. Click **Import** (top left)
3. Select `JSONCargo_API.postman_collection.json`
4. The collection appears in your sidebar

## Set your API key

The collection uses a variable `{{JSONCARGO_API_KEY}}` in every request header. Set it once and all requests pick it up automatically.

1. Click the collection name in the sidebar
2. Go to the **Variables** tab
3. Paste your API key into the **Current value** field for `JSONCARGO_API_KEY`
4. Click **Save**

Don't have an API key yet? Get one at [jsoncargo.com/pricing-plans](https://jsoncargo.com/pricing-plans/).

## What is included

| Folder | Requests |
|---|---|
| Container Tracking | Track a container, Track with shipping_line, Get containers from Bill of Lading |
| Vessel Tracking | Vessel Basic, Vessel Pro, Vessel Bulk, Vessel Finder, Vessel Specs |
| Ports and Terminals | Port Finder, Terminal Info |
| Utilities | Prefix Lookup, API Key Stats |

## The shipping_line parameter

Some container prefixes are shared across carriers. If you get a 404 on a container request, try adding the `shipping_line` query parameter. Valid values:

`MAERSK` `HAPAG_LLOYD` `HMM` `ONE` `EVERGREEN` `MSC` `CMA_CGM` `COSCO` `ZIM` `YANG_MING` `PIL`

Use the **Prefix Lookup** request to check which shipping line owns a given prefix.

## Support

- support@jsoncargo.com
- [jsoncargo.com/documentation-api](https://jsoncargo.com/documentation-api/)
