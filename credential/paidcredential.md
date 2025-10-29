---
title: Paid Credentials
description: Learn about RCL Learn paid credentials
has_children: false
parent: Credential
nav_order: 3
---


# Paid Credentials

An organizer can create a paid credential where a learner will need to pay a fee to enroll for the credential. 

## Prerequisites

Before a paid credential can be created, the following prerequisites must be met :

- Create a [PayPal Business Account](../payment/payment#paypal-account) in PayPal.

- [Configure PayPal](../payment/payment#configure-paypal-in-the-portal) in the Organizer portal.

- Enable [Instant Payment Notification](../payment/payment#setting-up-instant-payment-notification-ipn-in-paypal) in PayPal.

- Set the payment [Auto Return Page](../payment/payment#set-the-auto-return-page-in-paypal) in PayPal.

## Create a PayPal Buy Now Button in PayPal

- In PayPal ``Account Settings``, navigate to the ``Website payments`` page and update the ``PayPal buttons``.

- In the ``Make a PayPal Button`` page, click on the ``Buy Now`` button.

- In the ``Buy Now`` page, add the **Product Name** and **Price**

- In the RCL Learn portal, navigate to the ``Credentials`` page and in the credentials list, get the ``Id`` of the credential.

- In ``PayPal``, set the ``Product ID`` to the credential ``Id``.

- Set the button text to ``Pay Now``.

- Click the ``Save and Create`` button when you are done.

- Click the ``View your saved buttons`` link.

- Open the button and copy the **ID** for the button.

## Create a Paid Credential in the portal

- In the Organizer portal, navigate to the credentials list for a selected group. 

- Click on the admin button to the far right on the list for a selected credential and click on the ``Edit Cost`` link.

- In the ``Credential Cost`` page, add the cost for the credential.

- In PayPal, navigate to the ``Saved links and buttons`` page.

- Open the Buy Now button you created for the credential and copy the ``ID`` for the button.

- In the Organizer portal, add the ``PayPal Button Id`` in the ``Credential Cost`` page.

- Uncheck the ``Is Free`` checkbox for the credential.

- Click the ``Submit button`` when you are done.