---
title: DID
description: Learn what is a decentralized identifier (DID) 
parent: Credential
has_children: false
nav_order: 1
---

# Decentralized Identifier (DID)

A Decentralized Identifier is used to uniquely identify holders and issuers of [W3C Verifiable Credentials](https://www.w3.org/TR/vc-data-model-2.0/).

# What is a DID

A DID is machine-readable and enables verifiable and decentralized identity. There are many DID methods that can be used to create the DID. These DID methods will outline the electronic format for the DID, how it is hosted and how it is resolved.

# Cryptography

The foundation building block for a DID are Asymmetric Cryptographic Keys. A key pair is generated for the owner of a DID. A private key is securely held by the owner and a correspondent public key is distributed to the public.

An owner of a DID will use their private key to digitally sign a digital file and send this file to a receiver’s computer. The receiver’s computer will then use the public key of the sender that is publicly available to verify the sender’s signature on the digital file. When the digital signature is verified, the receiver’s computer will deem the signature valid and the digital file wll be accepted.

When a DID is created, a public and private key pair is generated for the owner. The owner will download and store the private key in a secure location. The public key will be embedded in the DID. Based on the particular DID method to be used, the public key will be made publicly available by resolving the DID. The public key can then be accessed in a DID document.

# Requirements for the DID

The following are the requirements for the DID that are currently supported. 

## Asymmetric Key Pair

An asymmetric public/private key pair must be created with the [RSA](https://datatracker.ietf.org/doc/html/rfc3447) algorithm with a key size of 2048 bits. The public key is used to create the DID.

{: .information }
Only RSA keys for DIDs created with the ``did:jwk`` method are supported.

The keys should be formatted in the [PEM](https://www.rfc-editor.org/rfc/rfc1422) format and issued in a text (``.txt``) file.

### Example Private Key in PEM format issued as a text file
```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAm1rdLzutW7fSndzQhDYfCCoApsm6kod9nBEHib+3GAKLMRtA
7Kw2CtdxckvHCv+oJyaoLnOM4uh7BYrO9InQhPpl73hvbVDW2jsOc8m3QDhd5X4F
5MDO1T44D9viwIuhFYoHuWXZAMvfW+O3Y++wKfKXnaw9qAlCCqwMU4gs7T6aZjEZ
znkwLYYT3wyrC4Ts3MOynbmm38mHTE936ixMKWfHSirhXqEcnxGTSNHqXMUssuZS
2x17YiJbC4CZ1QnDI1wdwDHfzyDVN2wSY3u2Gsep02PaOEyw6xguuz5MdiOtZpcj
oY6DkZke3lwptHQnywd/Hriv7nObS6OEZNn3DQIDAQABAoIBAF3BXWDG9B0496t7
en9/pgSoTJJbhfQuPpj0EgeIorejuVreZrUuTMMIOBfRMYMqvNE73B2EcI7z3GKA
3droXOYTs3bsyNpBAhjbsSIhpyzjl48LGgVucqRwkybG/bZTzdgQ4A58L5TydI6h
A6kVGsyF8ggezWreg3OrVxkGQo6923iK9E6xTKFn2Fz/YuG2MFv0SCEhyUmgMVVd
HHq1gt4McuFAC95fNMg1TS1TN7sZ2Wv16KSQteJKCSk/E31CQRJYbxb9Csz4xezU
6pcGI9UCLN5ulP0/9bDSsYmxQaDUTG57gREqZxYzQaZVqEkJh9K57LEMizVw+MkH
TOUmTaUCgYEAydk+JeGN7wdV6tw9lHBIws2Z1raoJ/4Y5Mt1VgrR3FhjRloUs47c
ZgJPIuRfZ9rD/MuYE5sDH7MK35OA+kMkQfAhxFRlK2KU5MyP6l0kuZsNJhWB5UTV
jPDOrIl4RgCRsgC8mRkN3JS7NP4zLFRvZLTJoG+pewuW09s0Tqh82EMCgYEAxQh7
vzU9kK472e+ArEDonWNZZMVNETZ1kMpg6dcA7DX4NMGylVvCLnhlRo44Ie8KC3he
YSauvADoF9Os+cbys0ZxJNxC26XxQ0N0mqSXbCuzVKzUrBblpGCNeBg237hIzOz1
NHZEGv5GkieE52cCoIIfgQFYQVvtASmO64Ek5m8CgYBfU5jVPRPSCk3aUE9I1kqW
rZD05Wi/EnLhQvFURGHeRWQFKq/SKSsPhhGnseEY5ClhLynQQIoWI3GEK15jUuhB
t83Ksezhs3oMIEvrbDfW7FImZUvmYj7UhDmnJHlH3ibwwQZQ65MvVJKhMVgrnGjL
T9JVUcbh1JRT05d9encTjwKBgAfe8OKQg+cVrrpkAOXgqeovn9CQuSVo4YVpMDnn
JthIx6OD4VhqE/W7RYBuCfwBCouuwUZsPyqvdpYNFKndsrBKrhZk3h7cICkptqy+
ynW9wSouxUgimgXY/Y3AmeCSAgZ9qMXxu4LAiZ0pCvwbd1VmHVAP97CUtYEIYfcy
b4DtAoGAFLh5bYHJ0p3w31GouCS4foLoidfVbOZe2f1YELhjCNkI3iVfme/G+YVe
wxH0h2gNzqCuQvVI/Bo4DwQuRAaKjwfd5TekPQZ67AyQhc3AOZcA0ax/IR6uqLXQ
SePVykjStRzrUbZ1JtIznzunR5jIk5WOTTOEOzFWKJt/W5xou1U=
-----END RSA PRIVATE KEY-----
```

### Example Public Key in PEM format issued as a text file
```
-----BEGIN RSA PUBLIC KEY-----
MIIBCgKCAQEAm1rdLzutW7fSndzQhDYfCCoApsm6kod9nBEHib+3GAKLMRtA7Kw2
CtdxckvHCv+oJyaoLnOM4uh7BYrO9InQhPpl73hvbVDW2jsOc8m3QDhd5X4F5MDO
1T44D9viwIuhFYoHuWXZAMvfW+O3Y++wKfKXnaw9qAlCCqwMU4gs7T6aZjEZznkw
LYYT3wyrC4Ts3MOynbmm38mHTE936ixMKWfHSirhXqEcnxGTSNHqXMUssuZS2x17
YiJbC4CZ1QnDI1wdwDHfzyDVN2wSY3u2Gsep02PaOEyw6xguuz5MdiOtZpcjoY6D
kZke3lwptHQnywd/Hriv7nObS6OEZNn3DQIDAQAB
-----END RSA PUBLIC KEY-----
```

The public key is used to create the DID using the ``did:jwk`` method. The DID will make the user's public key accessible for the verification of credentials.

{: .information }
The private key will be issued to the user as a text (``.txt``) file. The user should save the file in a safe place using a storage method of their own choice. 

## Public Key as a JWK

The public key is formatted as a [JSON Web Key](https://datatracker.ietf.org/doc/html/rfc7517) (JWK). It is recommended that the JWK contain the key parameters. It can be in the main body of the JWK or in a property named ``jwk``.

### Example of key parameters in the main body of a JWK
```json
{
    "alg": "RS256",
    "kty": "RSA",
    "n": "m1rdLzutW7fSndzQhDY......",
    "e": "AQAB"
}
```

### Example of key parameters in a ``jwk`` property in the JWK

```json
{
    "alg": "RS256",
    "kty": "RSA",
    "jwk": {
        "n": "m1rdLzutW7fSndzQhDYfCC......",
        "e": "AQAB"
    }
}
```

Although accepted, but highly discouraged, the JWK can include a ``kid`` property that contain a URL address that hosts the user's public key. When a ``kid`` is provided, the key parameters should not be included in the DID. The reason why this approach is discouraged is that if the website hosting the public key goes out of existence, there is no way left to verify the credential that references the DID.

### Example of a ``kid`` used in a JWK to reference a public key
```json
{
    "alg": "RS256",
    "kty": "RSA",
    "kid": "https://contoso.com/.well-known/public-key.json"
}
```
## did:jwk Method

The user's public key should be used to create the user's DID using the [did:jwk](https://github.com/quartzjer/did-jwk/blob/main/spec.md) method. This method allows for the immediate resolution of the user's public key since it is 'encapsulated' in the DID itself. This method is much simpler and potentially less expensive than other methods that use block chains to make the public key accessible to platforms. A DID should be issued to the user as a text (``.txt``) file.

### Example DID created with the ``did:jwk`` method and issued as a text file

```bash
did:jwk:eyJhbGciOiJSUzI1NiIsImt0eSI6IlJTQSIsIm4iOiI4cF9VYXZXZnlsbjJYeHY1el9GMjdBeVh4WExxU1dyMm
5DQno4ZE9vUTNYeTF6MUVsWHRvWl9Vd1p5cTFLNE1DRkVHMkl6S0NPaWZUYmJaS0plU3VtUlJQeFpoN2RjOENmU0YxUWE1
Z3lIWjJxQVlOTjRLc2EyVEtlaXJMRVZzcW5tY21fR0RxU3VYUVg5UUJMNzV4b3UyWHlid1F3VG9ZdklBRTRQUjRwRjc2S1
kxZjZtR09GMkV1WVZlakNwU2VzRmw3SEx1eFliV0lDZGxDSGhCWmV1MTNfSWZPRHNKWi1MTEthTzlWVk1YMHVzQ2dwdXc5
TnpfckFBd2pMRmI4TWk3aEYzRWpDWFVzT19uY2xEVGxMNkYwVUdoWVhzT0ZvX25iQ2cxcHJkVFhRV1NEeS05UjVubUhobV
RucUJfOHMzR0E3Sk1nakxlSmZpVjkzRloxZFEiLCJqd2siOnsibiI6IjhwX1VhdldmeWxuMlh4djV6X0YyN0F5WHhYTHFT
V3IybkNCejhkT29RM1h5MXoxRWxYdG9aX1V3WnlxMUs0TUNGRUcySXpLQ09pZlRiYlpLSmVTdW1SUlB4Wmg3ZGM4Q2ZTRj
FRYTVneUhaMnFBWU5ONEtzYTJUS2VpckxFVnNxbm1jbV9HRHFTdVhRWDlRQkw3NXhvdTJYeWJ3UXdUb1l2SUFFNFBSNHBG
NzZLWTFmNm1HT0YyRXVZVmVqQ3BTZXNGbDdITHV4WWJXSUNkbENIaEJaZXUxM19JZk9Ec0paLUxMS2FPOVZWTVgwdXNDZ3
B1dzlOel9yQUF3akxGYjhNaTdoRjNFakNYVXNPX25jbERUbEw2RjBVR2hZWHNPRm9fbmJDZzFwcmRUWFFXU0R5LTlSNW5t
SGhtVG5xQl84czNHQTdKTWdqTGVKZmlWOTNGWjFkUSIsImUiOiJBUUFCIn0sImUiOiJBUUFCIn0

```

{: .information }
Only DIDs created with the ``did:jwk`` method using the RSA algorithm are supported.

# Resolving a DID

Computer systems that can read the DID will resolve the DID into a DID Document. You can use the [Universal Resolver](https://dev.uniresolver.io/) provided by the Decentralized Identity Foundation (DIF) to resolve a DID. Just copy the DID into the did-url textbox and click the Resolve button. The DID will be resolved into a DID document in json format that looks something like this:

## Sample DID Document using the did:jwk Method
```json
{
  "@context": [
    "https://www.w3.org/ns/did/v1",
    {
      "@vocab": "https://www.iana.org/assignments/jose#"
    }
  ],
  "id": "did:jwk:eyJrdHkiOiJSU0EiLCJuIjoid3JFa2VvUUpOdWM5cnBuN3liSkJYb2FQMnpuYU1TWVRkSWtycWV3S1NyVFBoT0Q3cVRnQUViNFZLNldJN1dFSTZMcnoxMXRBYzd5MWJXWlgzX1BFUUFyUnFGeElKQWRvNGVzRXRxYUpWaEdXZTd1Q3NRNklxSHM4ZU9CNHgtbWFPLWVqOFJRZTkzYzZPWHZvMS02T1Z0SDVuY1FxVHRhLTBxR0ZzN0JBT2JPYUs3RGE1NjhuWG05aXUyTXR3WEtsX0JzMTVjVTR2Wlc0cGgyWmZMT0xUMFRFTVlDeXZmS3puaUVrVENUSnZ0Nll4Y3QycVFTenc1TWY2bk9RR29OV0NQdGpuY29XbVFZZUdUc1RaMDNleG5GdE5pQ25qTXdxTzBTQWxyWFd2a1dCMVhyaHlRVi1naWpfemIySjBqRFNWYk1VZ3FPRnFuY0JjRFJtd3dMTmVRIiwiZSI6IkFRQUIifQ",
  "verificationMethod": [
    {
      "id": "#0",
      "type": "JsonWebKey2020",
      "controller": "did:jwk:eyJrdHkiOiJSU0EiLCJuIjoid3JFa2VvUUpOdWM5cnBuN3liSkJYb2FQMnpuYU1TWVRkSWtycWV3S1NyVFBoT0Q3cVRnQUViNFZLNldJN1dFSTZMcnoxMXRBYzd5MWJXWlgzX1BFUUFyUnFGeElKQWRvNGVzRXRxYUpWaEdXZTd1Q3NRNklxSHM4ZU9CNHgtbWFPLWVqOFJRZTkzYzZPWHZvMS02T1Z0SDVuY1FxVHRhLTBxR0ZzN0JBT2JPYUs3RGE1NjhuWG05aXUyTXR3WEtsX0JzMTVjVTR2Wlc0cGgyWmZMT0xUMFRFTVlDeXZmS3puaUVrVENUSnZ0Nll4Y3QycVFTenc1TWY2bk9RR29OV0NQdGpuY29XbVFZZUdUc1RaMDNleG5GdE5pQ25qTXdxTzBTQWxyWFd2a1dCMVhyaHlRVi1naWpfemIySjBqRFNWYk1VZ3FPRnFuY0JjRFJtd3dMTmVRIiwiZSI6IkFRQUIifQ",
      "publicKeyJwk": {
        "kty": "RSA",
        "n": "wrEkeoQJNuc9rpn7ybJBXoaP2znaMSYTdIkrqewKSrTPhOD7qTgAEb4VK6WI7WEI6Lrz11tAc7y1bWZX3_PEQArRqFxIJAdo4esEtqaJVhGWe7uCsQ6IqHs8eOB4x-maO-ej8RQe93c6OXvo1-6OVtH5ncQqTta-0qGFs7BAObOaK7Da568nXm9iu2MtwXKl_Bs15cU4vZW4ph2ZfLOLT0TEMYCyvfKzniEkTCTJvt6Yxct2qQSzw5Mf6nOQGoNWCPtjncoWmQYeGTsTZ03exnFtNiCnjMwqO0SAlrXWvkWB1XrhyQV-gij_zb2J0jDSVbMUgqOFqncBcDRmwwLNeQ",
        "e": "AQAB"
      }
    }
  ]
}
```

# Download DIDs and Private Keys

## Download a DID 

A learner or organizer can create their DID in RCL Learn. The DID will be provided as a text (``.txt``) file. The DID can be downloaded and saved in a safe place.

## Download a private key

The private key will be provided as a text (``.txt``) file. The private key can be downloaded and saved in a safe place.