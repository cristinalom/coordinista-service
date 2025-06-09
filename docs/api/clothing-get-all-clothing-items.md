---
layout: page
---

# Get all clothing items

Returns an array of [clothing](clothing.md) items that make up all of the `outfits` in the service.

## URL

```shell

{server_url}/clothing
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

``` json
 {
      "name": "sneakers",
      "type": "footwear",
      "color": "white",
      "description": "Trusty pair of shoes",
      "outfits": ["picnic outfit"],
      "id": 11
    }
    ...
```

## Related tutorials

* [Add a new clothing item](../clothing-add-a-new-clothing-item.md)

## Related resources

* [Get clothing items by type](clothing-get-clothing-items-by-type.md)
