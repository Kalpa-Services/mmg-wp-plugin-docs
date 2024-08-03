---
sidebar_position: 1
---

# Introduction

MMG Checkout Payment is a WordPress plugin that enables MMG Checkout Payment flow for registered MMG Merchants to receive E-Commerce payments from MMG customers. This plugin integrates seamlessly with WooCommerce to provide a secure and efficient payment gateway for your online store.

## Getting Started

Get started by **[registering for an MMG Merchant Account](https://www.mmg.gy/lead-generation/)**.



### What you'll need

- [WordPress 6.0 or later](https://wordpress.org/download/)
- WooCommerce 7.0 or later
- PHP 7.4 or later
- mbstring extension enabled
- RSA keys for encryption and decryption
- SSL certificate for your website
- [MMG Checkout API credentials](mailto:merchantservices@mmg.gy?subject=Request%20for%20MMG%20Checkout%20API%20Credentials&body=Hello%2C%0A%0AI%20would%20like%20to%20request%20MMG%20Checkout%20API%20credentials%20for%20my%20merchant%20account.%0A%0AThank%20you.)

## Generate an RSA key pair

You can generate an RSA key pair using OpenSSL via the command line. Here are the steps to do so:

1. **Generate the Private Key**:
   ```sh
   openssl genpkey -algorithm RSA -out private_key.pem -pkeyopt rsa_keygen_bits:2048
   ```

2. **Generate the Public Key from the Private Key**:
   ```sh
   openssl rsa -pubout -in private_key.pem -out public_key.pem
   ```

These commands will create two files:

- `private_key.pem` containing your private key.
- `public_key.pem` containing your public key.

If you open these files, you will see the keys formatted as you requested:

#### Private Key (private_key.pem):
```
-----BEGIN PRIVATE KEY-----
<Your Private Key Data>
-----END PRIVATE KEY-----
```

#### Public Key (public_key.pem):
```
-----BEGIN PUBLIC KEY-----
<Your Public Key Data>
-----END PUBLIC KEY-----
```

To view the contents of these files directly from the command line, you can use the `cat` command:

```sh
cat private_key.pem
cat public_key.pem
```

Make sure to keep your private key secure and do not share it publicly.