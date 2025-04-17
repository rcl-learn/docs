---
title: Marketing Tag
description: Learn about RCL Learn marketing tags
has_children: false
parent: Marketing
nav_order: 1
---

# Marketing Tags
**V1.0**

Marketing tags are used optimize [Facebook ads](https://www.facebook.com/business/tools/facebook-ads) for your events and to track page views in [Google Analytics](https://marketingplatform.google.com/about/analytics/).

## Google Analytics tag

The Google Analytics tag is use to track page views in an organization's site. The following pages are tracked :

- Site home page

- Event groups page

- Event details page

In this way, you can track a site's views and you event views.

- In Google Analytics, create a new property.

- Name the property with your shared or custom domain name, eg. ``constoso.cloudtntcom``.

- Set up a data stream with your shared or custom domain URL, eg. ``https://contoso.cloudtnt.com``.

- Copy the ``MEASUREMENT ID`` to install in the portal later on.

- In the RCL Learn portal, navigate to ``Marketing >> Marketing Tag``.

- In the ``Marketing Tags`` page, click the ``Create a Marketing Tag`` button.

- Create a ``Google Analytics`` tag and add the ``MEASUREMENT ID`` from Google Analytics, then click the ``Submit`` button when you are done.

- You can now see the page views for a site on Google Analytics.

## Meta Pixel tag

The Meta Pixel tag is used to optimize Facebook ads for a event.

- In [Meta for Business](https://business.facebook.com/) , navigate to ``Events Manager`` and click on the ``Data Sources`` link.

- If you do not have a Pixel, create a new web data source, set a name for your Meta Pixel.

- Copy the ``ID` for the Pixel to install in the portal later on.

- In the RCL Learn portal, navigate to ``Marketing >> Marketing Tag``.

- In the ``Marketing Tags`` page, click the ``Create a Marketing Tag`` button.

- Create a ``Metal Pixel`` tag and add the Pixel ``ID`` from Meta for Business, then click the ``Submit`` button when you are done.

- In the ``Pixel`` page in Meta for Business, click the ``Test events`` tab.

- In the ``Test Browser Events`` , add the following URL to test a free event enrollment :

```https://<your-shared-or-custom-domain>/Event/EventPublic/EnrollmentSuccess```

Note: replace the domain place holder with your shared or custom domain name, eg. 

``https://contoso.cloudtnt.com/Event/EventPublic/EnrollmentSuccess`` 

or 

``https://learn.contoso.com/Event/EventPublic/EnrollmentSuccess``.

- You should see the ``Complete registration`` event was processed.

- Also test the following URL for a paid event :

```https://<your-shared-or-custom-domain>/Payment/PayPalReturn/PaymentSuccess```

- To include your Meta Pixel in an ad, create a new ``Sales`` campaign.

- Select ``Website`` conversion location and select the Meta Pixel in the ``Dataset``.

- Select ``Complete registration`` in the ``Conversion event``.

- The pixel will noe be added to your ad campaign.
