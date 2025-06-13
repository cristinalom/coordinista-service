---
layout: page
---

# Clothing resource

Contains information about clothing items stored in the Coordinista app. The user must upload clothing items to the service to create `outfits`. The `outfits` property of the `clothing` resource is what tells the service which clothing items make up an outfit.

> If you add a clothing item to the service, that item is not added to an outfit automatically. You must add the clothing item to the applicable outfits. For details, refer to [Add a new clothing item](../tutorials/clothing-add-a-new-clothing-item.md).

## Base endpoint

```shell

{server_url}/clothing
```

The `{server_url}` for the service is `http://localhost:3000`.

## Properties of the clothing resource

### Name

A string that uniquely identifies the clothing item.

### Type

A string that describes the clothing item type. 
Accepted values for the `type` property:

* `top`
* `bottom`
* `footwear`
* `accessory`
* `dress`

### Color

A string that describes the clothing item's color. The service uses the `color` property to coordinate `outfits`.

### Description

A string that provides a long description of the clothing item.

### Outfits

An array of strings that display the list of outfits that the clothing item fits into. Each clothing item can belong to many outfits.

### Id

A number that represens the clothing item's unique record ID.

## Sample clothing resource

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

## Clothing operations

### Read operations

* [Get all clothing items](clothing-get-all-clothing-items.md)

### Create operations

* [Post a new clothing item](clothing-post-a-new-clothing-item.md)

### Update operations

* [Patch a clothing item by id](clothing-patch-clothing-item-outfits.md)

### Delete operations

* [Delete a clothing item](clothing-delete-a-clothing-item.md)

## Related tutorials

* [Add a clothing item](../tutorials/clothing-add-a-new-clothing-item.md)
