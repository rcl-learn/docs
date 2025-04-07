---
title: Custom Domain
description: Learn how to create a custom domain for a site
has_children: false
parent: Site
nav_order: 3
---

# Custom Domain
**V1.0**

A custom domain is managed by the organization, and is the URL for the organization's [site](./create.md). It is used to navigate to the site in a web browser, eg. ``learn.contoso.com``.
The custom domain must be a sub-domain.

## Creating a Custom Domain

- If you have already registered a Shared Domain Name for your site, please delete it. You cannot have a [Shared Domain Name](./shareddomain.md) and Custom Domain Name at the same time.

- In the ``Site > Custom Domain`` page, create a custom domain name.

- In the management portal of your domain registrar, add the ``TXT`` record and ``CNAME`` records as shown on the ``Create Custom Domain Name`` page.

- It may take a few minutes to create the custom domain, so be patient.

- Once the custom domain is created, you can navigate to your [site](./create.md) using the URL displayed in the ``Custom Domain Name`` page.

- Note: You cannot have both a [Shared Domain Name](./shareddomain.md) and a Custom Domain Name at the same time, one must be deleted.

{: .warning }
Multiple creation and deletion of a custom domain is an expensive compute operation and is not allowed. Your site may be disabled for this type of action.


