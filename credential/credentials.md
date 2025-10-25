---
title: Credentials
description: Learn how to create and issue W3C Verifiable Credentials in RCL Learn.
parent: Credential
has_children: false
nav_order: 2
---

# Credentials
**V1.0**

An organization will issue a credential to a learner to recognize his/her achievement. The [credential](/introduction/introduction.md) will be created in accordance with the [W3C Verifiable Credentials Specification](https://www.w3.org/TR/vc-data-model-2.0/).

## Credential Group

An organizer will organize credentials within ``Credential Groups``. To create a group :

- In the ``Organizer`` portal, click on ``Credentials`` in the side menu

- In the ``Credentials Group`` page, add a new group

- You will then add credentials to this group

{: .information }
Before a credential group can be created, the organizer must create a [DID](./did.md).

## Credential

Credentials are created within a credential group. To create a credential :

- In the **Organizer** portal, in the ``Credentials Groups`` page, for a selected Group, click on ``Credentials`` from the drop down menu

- In the ``Credentials`` page, create a credential

- Once a credential is created, an issuer can issue this credential to a holder

## Credential Issuance

{: .information }
An organization must be **Verified** as who they claim to be before they can issue a credential. The organization must make a request to be verified using the support platform provided.

To issue a credential to a holder:

- In the **Organizer** portal, in the ``Credentials`` page, for a selected credential, click on the ``Issuances`` link in the drop down menu

- In the ``Issuances`` page, create a new Issuance

- In the ``Create Issuance`` page, add the holder username to which the credential will be issued

{: .information }
Before a holder username can be added. The user should have created a profile and DID in the ``Learner`` portal. You can click on the ``Search Holder`` link to search for the username to ensure it is a valid user. Please ensure the user's profile data and photo are acceptable, as it will be included in the credential.

- Create a ``Cohort`` or select an exiting one. A cohort is used to organize issuances.

- When you have created an issuance the holder can view and download the credential in the **Learner** portal.