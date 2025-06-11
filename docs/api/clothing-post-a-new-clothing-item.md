---
layout: page
---

# Post a new clothing item

Use the `POST` method to add a new clothing item to the service.

## URL

```shell

{server_url}/clothing
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

`Content-Type: application/json`
`Accept: application/json`

## Request body

```json
[
    {
        "name": "running shorts",
        "type": "bottoms",
        "color": "pink",
        "description": "Sweat-wicking, comfortable",
        "outfits": "mountain hiking outfit",
    }
]
```

## Return body

```json
[
    {
        "id": "c371",
        "name": "running shorts",
        "type": "bottoms",
        "color": "pink",
        "description": "Sweat-wicking, comfortable",
        "outfits": "mountain hiking outfit"
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

*[Add a new clothing item](../clothing-add-a-new-clothing-item.md)