---
layout: page
---

# Before you begin

You must install the following software in your system and make a test call to the Coordinista service before you can complete the related tutorials for the Coordinista service.

> After you install all the necessary software, testing the service takes 20 minutes to complete.

## Necessary software and database

To run the Coordinista service, you must have the following items installed and ready:

### Github

* [GitHub account](https://github.com)
* [Git command line](https://docs.github.com/en/get-started/quickstart/set-up-git)
* [GitHub Desktop](https://desktop.github.com)
* [Coordinista](https://github.com/cristinalom/coordinista-service) repository fork
* Coordinista database file
  > Sync your fork to get a current copy of the database.

### Other software

* Development system with long-term support (LTS) for Windows, MacOS, or Linux
* Current or LTS version of `node.js`
* Version 0.17.4 of [json-server](https://www.npmjs.com/package/json-server)
* [Postman desktop](https://www.postman.com/downloads/)

## Testing the service

Before you can test your service, ensure that you have created a fork of the Coordinista service and that your fork has a current copy of the database file.

> Note: The service runs on the `http://localhost:3000` URL.

1. Open your fork of the Coordinista service locally, in GitHub Desktop.
2. From Github Desktop, open your terminal to access your fork in the command line.
   1. Click **Repository** in the top menu bar and select the option to open your terminal.
3. Enter the following command in your terminal to create a test branch of your fork:
  
   ```shell
    ls
    # lists all of the files in your fork of the Coordinista repository
    git checkout -b tutorial-test
    # creates the test branch of your fork
    cd api
    # changes the directory to the api file
    json-server -w coordinista.db.json
    # starts the json-server application
   ```
  
4. Make a test call to the service:

   ```shell
   curl https://localhost:3000/clothing
   ```

5. If the service is running correctly, a list of clothing items for the service displays:

```js
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
 ]
```

You have tested the service successfully. You can now perform the tasks in the related tutorials as needed.

Try your hand at our Quickstart tutorial: [Get all outfits by season](../docs/tutorials/outfits-get-all-outfits-by-season.md).
