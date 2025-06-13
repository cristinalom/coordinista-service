---
layout: page
---

# Patch clothing items by ID

Patches a [clothing](clothing.md) item's properties. The `id` parameter specifies which clothing item in the service to patch. In this example, the `color` property is patched for the clothing item that corresponds to the `id` 3.

## URL

```shell

{server_url}/clothing/{id}
```

## Properties

|Property Name |Type |Description |
|---------------|-----|------------|
| `name`      |string |A descriptive name for the clothing item|
|`type`    |string |The clothing item type|
|`color`     |string |The clothing item's color|
|`description` |string |A long description of the clothing item|
|`outfits`|string | An array that contains the `outfit` resources that a clothing item belongs to|
|`id` |number |A number that represents the clothing items unique record ID|

## Request headers

* `Content-Type: application/json`
* `Accept: application/json`

## Request body

```json
[
    {

        "color": "orange"
    }
]
```

## Return body

```json
[
    {
        "name": "hiking boots",
        "type": "footwear",
        "color": "orange",
        "description": "Waterproof, comfortable",
        "outfits": "mountain hiking outfit",
        "id": "3"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related tutorials

* [Add a new clothing item](../clothing-add-a-new-clothing-item.md)

## Related references

* [Patch an outfit](outfits-patch-an-outfit-by-id.md)
