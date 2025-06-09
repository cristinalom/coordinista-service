---
layout: page
---

# Get clothing items by type

Returns an array of `clothing` items based on item `type`.

## URL

```shell

{server_url}/clothing?type={clothing item type}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `type` | string | Describes the clothing item type|

## Request headers

None

## Request body

None

## Return body

```json
[
    {
        "name": "hiking boots",
        "type": "footwear",
        "color": "blue",
        "description": "Waterproof, comfortable",
        "outfits": "mountain hiking outfit",
        "id": "3"
    },
    {
        "name": "strappy heels",
        "type": "footwear",
        "color": "silver",
        "description": "Looks amazing but not too comfortable",
        "outfits": "wedding party outfit, cocktail party outfit",
        "id": "6"
    },
    ...
]
```

## Related tutorials

*[Add a new clothing item](../clothing-add-a-new-clothing-item.md)
