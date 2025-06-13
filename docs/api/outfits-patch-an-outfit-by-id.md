---
layout: page
---

# Patch clothing items by ID

Patches an [outfits](outfits.md) properties. The outfit is specified by the `id` parameter, if it exists. In this example, the `season` and `event` properties are updated with the `PATCH` method.

## URL

```shell

{server_url}/outfits/{id}
```

## Properties

|Property Name |Type |Description |
|---------------|-----|------------|
| `name`      |string |A descriptive name for the outfit|
|`season`    |string |The season that best fits the outfit|
|`event`     |string |The event type that the user wears the outfit to|
|`description` |string |A long description of the outfit|
|`clothingItems`|string | An array that contains the `clothing` resources that make up the outfit|
|`id` |number |A number that represents the outfit's unique record ID|

## Request headers

* `Content-Type: application/json`
* `Accept: application/json`

## Request body

```json
[
    {

        "season": "winter",
        "event": "outdoors"
    }
]
```

## Return body

```json
[
    {
    "name": "picnic outfit",
    "season": "winter",
    "event": "outdoors",
    "description": "Cottage-core, but make it practical.",
    "clothingItems": "long-sleeved shirt, denim jeans, sneakers, backpack",
    "id": "4"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related references

* [Post a new outfit](outfits-post-a-new-outfit.md)
* [Delete an outfit](outfits-delete-an-outfit.md)
