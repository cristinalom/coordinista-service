---
layout: page
---

# Coordinista overview

Coordinista is an outfit coordinating API used to simplify the daily task of choosing an outfit.

---

## Quickstart: Get an outfit by season

Learn how Coordinista can [Generate an outfit by season](docs/tutorials/outfits-get-all-outfits-by-season.md) instantaneously.
> The tutorial takes about 15 minutes to complete.

## Setting up the Coordinista service

1. Use the [API security and authorization] tutotiral to set up your credentials and access the Coordinista service securely.
2. Access the [Before you begin](before-you-begin.md) tutorial to set up your development system and enable Coordinsta on your device.

## Tutorials

After you set up your Coordinista service in your system sucessfully, you can access one of the tutorials to further customize your service.

* [Get an outfit based on clothing items](docs/tutorials/outfits-get-outfit-based-on-clothing-item.md)
* [Add a new clothing item](docs/tutorials/clothing-add-a-new-clothing-item.md)

## References by resource

Coordinista uses the `clothing` resource to create a completed outfit. Coordinista bases the `outfit` resource on a variety of factors including `season` and `event` type.

* [Clothing resource](api/clothing.md)
* [Outfit resource](api/outfits.md)

## About the service

The Coordinista app generates an outfit methodically by assessing all the `clothing` resources in your service and determining which items coordinate with one another. The Coordinista app coordinates outfits by filtering the properties of each `clothing` resource.

An `outfit` resource includes many `clothing` resources. Each `clothing` resource can belong to many outfits.
