---
layout: page
---

# Delete an outfit by id

Deletes the user specified by the `{id}` parameter.

## URL

```shell

{base_url}/delete/outfits/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record `id` of the outfit to delete |

## Request headers

None

## Request body

None

## Return body

```js
{}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related references

* [Delete a clothing item](clothing-delete-a-clothing-item.md)
* [Get all outfits](outfits-get-all-outfits.md)
* [Post a new outfit](outfits-post-a-new-outfit.md)
