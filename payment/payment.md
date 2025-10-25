---
title: Payments
description: Learn about RCL Learn payment.
has_children: false
nav_order: 5
---

# PayPal Payments
**V1.0**

An organization can collect payments with [PayPal](https://www.paypal.com/us/home).

## PayPal account

The organization must set up a [PayPal Business Account](https://www.paypal.com/us/business/open-business-account) to collect online payments.

## Configure PayPal in the portal

- Payments can only be configured by an organizer in the portal.

- In RCL Learn Organizer portal, go to the ``Payments > PayPal Configuration`` page, add the ``Business Email`` address of your PayPal business account.

- You can get the Business Email in PayPal in the ``Account Setting`` section under ``Account ownership info`` page.


## Setting up Instant Payment Notification (IPN) in PayPal

- For the application to process PayPal payments, IPN must be enabled in PayPal.

- In PayPal ``Account Settings``, navigate to the ``Website payments`` page and update the ``Instant payment notification``.

- In the ``Instant Payment Notification (IPN)`` page, click on the ``Choose IPN Settings`` button.

- Add the following URL in the ``Notification URL`` text box :

```
https://rclapi.azure-api.net/v1/payment/paypal/webhook

```

- Select the ``Receive IPN messages (Enabled)`` to enable IPN.

- Save the settings when you are done.

## Set the Auto Return page in PayPal

- In PayPal ``Account Settings``, navigate to the ``Website payments`` page and update the ``Website preferences``.

- In the ``Website payment preferences`` page, set the ``Auto return`` to ``On`` and set the return URL to :

```
https://learn.rclapp.com/Public/PayPalReturn/PaymentSuccess
```

- Click the ``Save`` link when you are done.

- Set the ``PayPal account optional`` to ``On``.

## View complete payments in the portal

An organization can view a list of completed payments in the portal.

- In the Organizer portal, navigate to the ``Payments > PayPal Payments`` page.

- In the ``Recent Payments`` page, you view and manage payments

