---
layout: page
---

# Coordinista overview

Coordinista is an outfit coordinating API used to simplify the daily task of choosing an outfit.

---

## Quickstart: Get an outfit by season

Learn how Coordinista can [Generate an outfit by season](outfits-get-all-outfits-by-season.md) instantaneously.
> The tutorial takes about 15 minutes to complete.

## Setting up the Coordinista service

1. Use the [API security and authorization] tutotiral to set up your credentials and access the Coordinista service securely.
2. Access the [Before you begin](before-you-begin.md) tutorial to set up your development system and enable Coordinsta on your device.

## Tutorials

After you set up your Coordinista service in your system sucessfully, you can access one of the tutorials to further customize your service.

* Create an outfit
* Add a clothing item
* Add a clothing item to an outfit

## References by resource

Coordinista uses the `clothing` resource to create a completed outfit. Coordinista bases the `outfit` resource on a variety of factors including `season` and `event` type.

* [Clothing resource](clothing.md)
* [Outfit resource](outfit.md)

## About the service

The Coordinista app generates an outfit methodically by assessing all the `clothing` resources in your service and determining which items coordinate with one another. The Coordinista app coordinates outfits by filtering the properties of each `clothing` resource.

An `outfit` resource includes many `clothing` resources. Each `clothing` resource can belong to many outfits.
