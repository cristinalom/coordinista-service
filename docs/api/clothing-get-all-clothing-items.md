---
layout: page
---

# Get all clothing items

Returns an array of [clothing](clothing.md) items that are used to make up all the `outfits` in the service.

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
[ 
  {
      "name": "sneakers",
      "type": "footwear",
      "color": "white",
      "description": "Trusty pair of shoes",
      "outfits": ["picnic outfit"],
      "id": 11
    },
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related tutorials

* [Add a new clothing item](../tutorials/clothing-add-a-new-clothing-item.md)

## Related references

* [Post a new clothing item](clothing-post-a-new-clothing-item.md)
* [Get all outfits](outfits-get-all-outfits.md)
