---
layout: page
---

# Delete a clothing item by id

Deletes the `clothing` item specified by the `{id}` parameter.

## URL

```shell

{base_url}/delete/clothing/{id}
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

* [Delete an outfit](outfits-delete-an-outfit.md)
* [Patch a clothing item](clothing-patch-clothing-item-outfits.md)