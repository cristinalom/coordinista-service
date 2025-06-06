---
layout: page
---

# `clothing` resource

Contains information about clothing items stored in the Coordinista app. The user must upload clothing items of differen types to the service before Coordinista can generate outfits.

## Base endpoint

```shell

{server_url}/clothing
```

## Properties of the clothing resource

### `name`

A string that uniquely identifies the clothing item.

### `type`

A string that describes the clothing item type. The relationship between the `type` property and `outfit` resource is 1:1. The service allows one item type per `outfit`.

### `color`

A string that describes the clothing item's color. The service uses the `color` property to coordinate `outfits`.

### `description`

A string that provides a long description of the clothing item.

### `outfits`

A string with arrays that display the list of outfits that the clothing item fits into. Each clothing item can belong to many outfits.

### `id`

A number that represens the clothing item's unique record ID.

## Sample `clothing` resource

``` json
 {
      "name": "sneakers",
      "type": "footwear",
      "color": "white",
      "description": "Trusty pair of shoes",
      "outfits": ["picnic outfit"],
      "id": 11
    }
```

## `clothing` operations

### Read operations

* [Get all clothing items](clothing-get-all-clothing-items.md)
* [Get clothing items by type](clothing-get-clothing-items-by-type.md)

### Create operations

* [Post a new clothing item](clothing-post-a-new-clothing-item.md)

### Delete operations

* [Delete a clothing item](clothing-delete-a-clothing-item.md)

## Related tutorials

* [Add a clothing item]
* [Add a clothing item to an outfit]
