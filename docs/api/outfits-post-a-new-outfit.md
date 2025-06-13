---
layout: page
---

# Post a new outfit

Adds a new outfit to the service.

## Prerequisites

Before you add the new outfit, ensure that all the applicable clothing items that make up the outfit are already added to the service:

* [Get all clothing items](clothing-get-all-clothing-items.md)
* [Add a new clothing item](docs/tutorials/clothing-add-a-new-clothing-item.md)

## URL

```shell

{server_url}/outfits
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

`Content-Type: application/json`

## Request body

A sample request body that demonstrates how to add a new outfit to the service:

```json


    {
        "name": "lumberjack",
        "season": "fall",
        "event": "outdoors",
        "description": "In case apple picking is not enough.",
        "clothingItems": "flannel shirt, waterproof pants, sneakers, beanie",
    }

```

## Return body

Returns the information from the request body plus a unique ID for the task.

```json


 {
        "id": "69fe",
        "name": "lumberjack",
        "season": "fall",
        "event": "outdoors",
        "description": "In case apple picking is not enough.",
        "clothingItems": "flannel shirt, waterproof pants, sneakers, beanie"
    }
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related references

* [Patch an outfit](outfits-patch-an-outfit-by-id.md)