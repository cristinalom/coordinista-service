---
layout: page
---

# Tutorial: Get an outfit by season

This tutorial shows you the process to get an outfit from the Coordinista service based on the season.
> This tutorial takes about 10 minutes to complete

## Prerequisites

* You completed the [Before you begin](before-you-begin.md) tutorial
* You have outfits stored in the service

## Get an outfit by season

Use the `GET` method to get an outfit based on specific parameters, such as season.

1. Start your service in the terminal with the following command:

    ```shell
    cd <your-github-workspace>/coordinista-service/api
    json-server -w coordinista-db.json
    ```

2. Open the Postman app on your desktop.
3. Create a new request in the Postman app with the following values and parameters:
    * **METHOD**: `GET`
    * **URL**: `{{base_url}}/outfits`
    * **Headers**:
        * `Content-Type: application/json`
    * **Query Params**:
    | Key      | Value         | Description |
    | -------------- |------------| -----------|
    | **season**  | winter    |   Returns all outfits for the winter season|

4. Click **Send** to make the request
5. Ensure that the response body displays the same season that you identified in your request:

```json
[
    {
        "name": "mountain hiking outfit",
        "season": "winter",
        "event": "outdoors",
        "description": "Hiking? In the winter? Extremely unlikely but not impossible.",
        "clothingItems": "long-sleeved shirt, waterproof pants, hiking boots, beanie, backpack",
        "id": "1"
    }
]
```
