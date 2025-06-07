---
layout: page
---

# Before you begin

You must install the following software in your system and make a test call to the Coordinista service before you can complete the related tutorials for the Coordinista service.

> These prerequisites take about 20 minutes to complete

## Necessary software and database

To run the Coordinista service, you must have the following items installed and ready:

### Github

* [GitHub account](https://github.com)
* [Git command line](https://docs.github.com/en/get-started/quickstart/set-up-git)
* [GitHub Desktop](https://desktop.github.com)
* [Coordinista](https://github.com/cristinalom/coordinista-service) repository fork
* Coordinista database file
    Sync your fork to get a current copy of the database

### Other software

* Development system with long-term support (LTS) for Windows, MacOS, or Linux
* Current or LTS version of `node.js`
* Version 0.17.4 of [json-server](https://www.npmjs.com/package/json-server)
* [Postman desktop](https://www.postman.com/downloads/)

## Testing the service

1. Create a test branch of your fork of the Coordinista repository.
2. Open the fork of the service in GitHub Desktop, then open your terminal
3. Enter the following command in your terminal
  
 ```shell
    ls
    git checkout -b tutorial-test
    cd api
    json-server -w coordinista-db.json
```

The URL of the service displays as `http://localhost:3000`

4. Make a test call to the service:

```shell
curl http://localhost:3000/clothing
```

5. If the service is running correctly, a list of clothing items for the service displays:

```json
 [
    {
      "name": "long-sleeved shirt",
      "type": "top",
      "color": "black",
      "description": "Sweat-wicking material, perfect for physical activity",
      "outfits": ["mountain hiking outfit", "picnic outfit"],
      "id": 1
    },
    {
      "name": "waterproof pants",
      "type": "bottom",
      "color": "black",
      "description": "Sturdy, breathable despite being waterproof",
      "outfits": ["mountain hiking outfit"],
      "id": 2
    },
        ...
 ]
    ```
