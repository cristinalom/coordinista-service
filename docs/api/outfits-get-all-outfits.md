---
layout: page
---

# Get all outfits

Returns an array of [outfits](outfits.md) that contains all outfits that belong to the service.

## URL

```shell

{server_url}/outfits
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

```json

[
   {
        "name": "wedding party outfit",
        "season": "summer",
        "event": "formal",
        "description": "It's giving Keira Knightley in 'Atonement'.",
        "clothingItems": "evening gown, strappy heels, pearl clutch",
        "id": "2"
    },
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related references

* [Outfits](outfits.md)
* [Post a new outifit](outfits-post-a-new-outfit.md)