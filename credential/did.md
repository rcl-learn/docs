---
title: DID
description: Learn what is a decentralized identifier (DID) 
has_children: false
nav_order: 1
---

# Decentralized Identifier (DID)

A Decentralized Identifier is used to uniquely identify holders and issuers of [W3C Verifiable Credentials](https://www.w3.org/TR/vc-data-model-2.0/).

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

# DID for Learners

## Holder's DID 

A holder can create their DID in the Learner portal of RCL Learn. The DID will be provided to the user as a text (``.txt``) file. The DID will be provided to the user to download and save in a safe place.

## The holder's private key

he private key will be provided to the user as a text (``.txt``) file. The private key will be provided to the user to download and save in a safe place.

