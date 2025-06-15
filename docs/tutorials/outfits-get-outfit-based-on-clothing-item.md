---
layout: page
---

# Tutorial: Find outfits based on the clothingItems property

This tutorial shows you how to use the `clothingItems_like` filter to return outfits in the service that use a specific clothing item.
> This tutorial takes about 15 minutes to complete.

## Prerequisites

* Complete the [Before you begin](../before-you-begin.md) topic to ensure that you have the service installed on your system.
* Ensure that all the outfits in the service have corresponding `clothingItems` based on the `clothing` resource.

To add an outfit to the service, refer to [Post a new outfit](../api/clothing-post-a-new-clothing-item.md). To add a clothing item to an existing outfit, refer to [Add a new clothing item](../tutorials/clothing-add-a-new-clothing-item.md).

## Find outfits based on the clothingItems property

Use the `GET` method and the `clothingItems_like` filter to retrieve all outfits with the same `clothingItems` property.

> The `{base_url}` for the service is `http://localhost:3000`.

To find outfits based on the clothingItems propery:

1. From GitHub desktop, open your terminal to access your fork of the Coordinista repository in the command line.
2. If your local service is not running yet, start it with the following command:

    ```shell
    cd <your-github-workspace>/coordinista-service/api
    json-server -w coordinista-db.json
    ```

3. Open the Postman app on your desktop.
4. In the Postman app, create a new request with the following values:
    * **METHOD**: `GET`
    * **URL**: `{{base_url}}/outfits?clothingItems_like=backpack`
    * **Headers**:
        * `Content-Type: application/json`

5. In the Postman app, click **Send** to make the request.
6. Watch for the response body, which should generate all outfits with `backpacks` in the `clothingItems` property:
