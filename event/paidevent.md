---
title: Paid Events
description: Learn about RCL Learn paid events
has_children: false
parent: Event
nav_order: 4
---


# Paid Events

An organizer can create a paid event where a learner will need to pay a fee to enroll for the event. The event can be a live video delivered in a Microsoft Teams Meeting or a recorded video stored in Microsoft OneDrive.

## Prerequisites

Before a paid event can be created, the following prerequisites must be met :

- Create a [PayPal Business Account](../payment/payment#paypal-account) in PayPal.

- [Configure PayPal](../payment/payment#configure-paypal-in-the-portal) in the Organizer portal.

- Enable [Instant Payment Notification](../payment/payment#setting-up-instant-payment-notification-ipn-in-paypal) in PayPal.

- Set the payment [Auto Return Page](../payment/payment#set-the-auto-return-page-in-paypal) in PayPal.

## Create a PayPal Buy Now Button in PayPal

- In PayPal ``Account Settings``, navigate to the ``Website payments`` page and update the ``PayPal buttons``.

- In the ``Make a PayPal Button`` page, click on the ``Buy Now`` button.

- In the ``Buy Now`` page, add the **Product Name** and **Price**

- In the RCL Learn portal, navigate to the ``Events`` page and in the events list, get the ``Id`` of the event.

- In ``PayPal``, set the ``Product ID`` to the event ``Id``.

- Set the button text to ``Pay Now``.

- Click the ``Save and Create`` button when you are done.

- Click the ``View your saved buttons`` link.

- Open the button and copy the **ID** for the button.

## Create a Paid Event in the portal

- In the Organizer portal, navigate to the events list for a selected group. 

- Click on the admin button to the far right on the list for a selected event and click on the ``Edit Cost`` link.

- In the ``Event Cost`` page, add the cost for the event.

- In PayPal, navigate to the ``Saved links and buttons`` page.

- Open the Buy Now button you created for the event and copy the ``ID`` for the button.

- In the portal, add the ``PayPal Button Id`` in the ``Event Cost`` page.

- Uncheck the ``Is Free`` checkbox for the event.

- Click the ``Submit button`` when you are done.

