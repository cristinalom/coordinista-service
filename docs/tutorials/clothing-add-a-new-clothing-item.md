---
layout: page
---

# Tutorial: Add a new clothing item

This tutorial shows you the operations to add a new `clothing` resource as well as the operations to add that new item to an existing outfit.
> This tutorial takes about 20 minutes to complete.

## Prerequisites

* Complete the [Before you begin](../before-you-begin.md) topic to ensure that you have the service installed on your system.
* If you want to add a new clothing item to an `outfit` resource, ensure that the `outfit` resource already exists in the service.

## Add a new clothing item to the service

Use the `POST` method and a new `clothing` resource to your service.

> The `{base_url}` for the service is `http://localhost:3000`.

**To add a new clothing item:**

1. From GitHub desktop, open your terminal to access your fork of the Coordinista repository in the command line.
2. If your local service is not running yet, start it with the following command:

    ```shell
    cd <your-github-workspace>/coordinista-service/api
    json-server -w coordinista-db.json
    ```

3. Open the Postman app on your desktop.
4. In the Postman app, create a new request with the following values:
    * **METHOD**: `POST`
    * **URL**: `{{base_url}}/clothing`
    * **Headers**:
        * `Content-Type: application/json`
        * `Accept: application/json`

5. Add the properties of your new clothing item to the Request Body. For example:

    ```json
    [
        {
            "name": "silk skirt",
            "type": "bottoms",
            "color": "red",
            "description": "mysterious",
            "outfits": "cocktail party outfit"
        }
    ]
    ```

6. In the Postman app, click **Send** to make the request.
7. Watch for the response body, which should generate your new clothing item with a unique `id`.

    ```json
    [
        {
            "name": "silk skirt",
            "type": "bottoms",
            "color": "red",
            "description": "mysterious",
            "outfits": "cocktail party outfit",
            "id": "d5dc"
        }
    ]
    ```

You have successfully added a silk skirt to your `clothing` resources.

## Add a new clothing item to an existing outfit

**To add a new clothing item to an `outfit` resource:**

1. In the Postman app, create a new request with the following values:
    * **METHOD**: `PATCH`
    * **URL**: `{{base_url}}/outfits/{id}`
    * **Headers**:
        * `Content-Type: application/json`
        * `Accept: application/json`

2. Update the existing outfit's `clothingItem` parameters in the request body:

    ```json
    [
        {

            "clothingItems": ["little black dress, strappy heels, pendant necklace,silk skirt" ]
        }
    ]
    ```

    >Remember to keep the existing `clothingItems` in your request.

3. Click **Send** to make the request.
4. Ensure that the response body displays the updated `outfits` resource with the new `clothingItem` that you added.

```json
[
    {
    "name": "cocktail party outfit",
    "season": "spring",
    "event": "formal",
    "description": "Something you can wear at a fancy work event and at the club.",
    "clothingItems": [
        "little black dress, strappy heels, pendant necklace,silk skirt"
    ],
    "id": "5"
}
]
```

You have created a new `clothing` resource, and added that clothing item to your `outfit` resource.
