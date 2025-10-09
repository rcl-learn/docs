---
title: Payments
description: Learn about RCL Learn payment.
has_children: false
nav_order: 4
---

# Paid Events
**V1.0**

An organization can collect payments with [PayPal](https://www.paypal.com/us/home).

## PayPal account

The organization must set up a [PayPal Business Account](https://www.paypal.com/us/business/open-business-account) to collect online payments.

## Configure PayPal in the portal

- Payments can only be configured by an owner in the portal.

- In the ``Payments > PayPal Configuration`` page, add the ``Business Email`` address of the PayPal account.

## Setting up Instant Payment Notification (IPN) in PayPal

- For the application to process PayPal payments, IPN must be enabled in PayPal.

- In ``PayPal Account Settings``, navigate to the ``Website payments`` page and update the ``Instant payment notification``.

- In the ``Instant Payment Notification (IPN)`` page, click on the ``Choose IPN Settings`` button.

- Add the following URL in the ``Notification URL`` text box :

```
https://rclapi.azure-api.net/v1/payment/paypal/webhook

```

- Select the ``Receive IPN messages (Enabled)`` to enable IPN.

- Save the settings when you are done.

## Set the Auto Return page in PayPal

- In ``PayPal Account Settings``, navigate to the ``Website payments`` page and update the ``Website preferences``.

- In the ``Website payment preferences`` page, set the ``Auto return`` to ``On`` and set the return URL to :

```
https://<your-custom-or-shared-domain>/Payment/PayPalReturn/PaymentSuccess
```

Note: Replace the ``your-custom-or-shared-domain`` place holder with your domain, eg,

```
https://contoso.cloudtnt.com/Payment/PayPalReturn/PaymentSuccess
```

or 

```
https://learn.contoso.com/Payment/PayPalReturn/PaymentSuccess
```

- Click the ``Save`` link when you are done.

- Set the ``PayPal account optional`` to ``On``.

## View complete payments in the portal

An organization can view a list of completed payments in the portal.

- In the portal, navigate to the ``Portal > Portal`` page.

- In the ``Recent Payments`` page, you view and manage payments

