---
layout: page
---

# Tutorial: Find all clothing resources that make up an outfit

This tutorial shows you how use the `outfits_like` filter to return all clothing items that make up an outfit in the service.
> This tutorial takes about 15 minutes to complete.

## Prerequisites

* Complete the [Before you begin](../before-you-begin.md) topic to ensure that you have the service installed on your system.
* Ensure that all the `clothing` resources in the service have corresponding `outfit` properties based on the `outfits` resource. In other words, ensure that your outfits are represented in the `outfits` property of your `clothing` resource.

> NOTE: Ensure that the json-server version that you installed is 0.17.4 or older, or the `like` filter does not render results.

## Return clothing resources based on the outfits property

Use the `GET` method and the `outfits_like` filter to retrieve all clothing items with the same `outfits` property.

> The `{base_url}` for the service is `http://localhost:3000`.

**To find clothing resources that make up an outfit:**

1. From GitHub desktop, open your terminal to access your fork of the Coordinista repository in the command line.
2. If your local service is not running yet, start it with the following command:

    ```shell
    cd <your-github-workspace>/coordinista-service/api
    json-server -w coordinista-db.json
    ```

3. Open the Postman app on your desktop.
4. In the Postman app, create a new request with the following values:
    * **METHOD**: `GET`
    * **URL**: `{{base_url}}/clothing?outfits_like=cocktail party outfit`
    * **Headers**:
        * `Content-Type: application/json`

5. In the Postman app, click **Send** to make the request.
6. Watch for the response body, which should generate all `clothing` resources that have `cocktaill party outfit` listed in the `outfits` property:

    ```json
    [
        {
            "name": "strappy heels",
            "type": "footwear",
            "color": "silver",
            "description": "Looks amazing but not too comfortable",
            "outfits": "wedding party outfit, cocktail party outfit",
            "id": 6
        },
        {
            "name": "little black dress",
            "type": "dress",
            "color": "black",
            "description": "The name is self-explanatory",
            "outfits": "cocktail party outfit",
            "id": 13
        },
        {
            "name": "pendant necklace",
            "type": "accessory",
            "color": "silver",
            "description": "Gorgeous necklace from grandma -- don't lose!",
            "outfits": "cocktail party outfit",
            "id": 14
        }
    ]
    ```

## Related tutorials

To add a clothing item to an existing outfit, refer to [Add a new clothing item](../tutorials/clothing-add-a-new-clothing-item.md).

To return all `outfit` resources that include a specific clothing item, refer to [Get an outfit based on clothing items](../tutorials/outfits-get-outfit-based-on-clothing-item.md).