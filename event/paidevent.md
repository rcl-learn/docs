---
title: Paid Events
description: Learn about RCL Learn paid events
has_children: false
parent: Event
nav_order: 2
---


# Paid Events

An organizer can create a paid event where a learner will need to pay a fee to enroll for the event.

## Prerequisites

Before a paid event can be created, the following prerequisites must be met :

- Create a [PayPal Business Account](/payment/payment.md/#paypal-account) in PayPal.

- Enable [Instant Payment Notification](/payment/payment.md/#setting-up-instant-payment-notification-ipn-in-paypal) in PayPal.

- Set the payment [Auto Return Page](/payment/payment.md/#set-the-auto-return-page) in PayPal.

## Create a PayPal Buynow Button

- In ``PayPal Account Settings``, navigate to the ``Website payments`` page and update the ``PayPal buttons``.

- In the ``Make a PayPal Button`` page, click on the ``Buy Now`` button.

= In the ``Buy Now`` page, add the Product Name and Price

- In the RCL Learn portal, navigate to the ``Events`` page and in the events lis, get the ``Id`` of the event.

- In ``PayPal``, set the ``Product ID`` to the event ``Id``.

- Set the button text to ``Pay Now``.

- Click the ``Save and Create`` button when you are done.

## Create a Paid Event

- In the portal, navigate to the events list for a selected group. 

- Click on the admin button to the far right on the list for a selected event and click on the ``Cost`` link.

- In the ``Event Cost`` page, add the cost for the event.

- In PayPal, navigate to the ``Saved links and buttons`` page.

- Open the Buy Now button you created for the event and copy the ``ID`` for the button.

- In the portal, add the ``PayPal Button Id`` in the ``Event Cost`` page.

- Click the ``Submit button`` when you are done.

