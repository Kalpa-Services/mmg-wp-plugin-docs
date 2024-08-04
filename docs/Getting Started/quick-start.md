---
sidebar_position: 2
description: Configuration Guide.
---

# Installation and Configuration

---

## Install the plugin

- Download the latest release of the plugin from the [GitHub Releases page](https://github.com/Kalpa-Services/mmg-wp-plugin/releases).
- Log in to your WordPress admin area.
- Go to 'Plugins' > 'Add New'.
- Click 'Upload Plugin' and select the `mmg-checkout-payment.zip` file you downloaded.
- Click 'Install Now' to install the plugin.
- Activate the plugin through the 'Plugins' menu in WordPress.

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

:::note
When requesting your MMG Merchant credentials, you will be asked to provide the **Public Key**. This is the key you generated in the previous step.
:::

## Configure the plugin

- Go to 'Settings' > 'MMG Checkout' to configure the plugin.
- Copy the Callback URL and send it to the MMG team for them to configure your store's **response and error URLs**.
- Enter your MMG Merchant credentials:
  - Merchant Name (if different from site title)
  - Live Client ID
  - Live Merchant ID
  - Live Secret Key
  - Live RSA Public Key (MMG): this is the public key MMG will provide to you.
  - Live RSA Private Key (Merchant): this is the private key you generated.
  - Switch mode to 'Live'
  - Save the settings
- Go to 'WooCommerce' > 'Settings' > 'Payments' to configure the checkout settings.
  - Enable 'MMG Checkout' as the payment gateway.
  - Save the settings


:::note

Make sure to keep your credentials secure and never share them publicly. You should only share your **Public Key** with MMG.

:::

## Sandbox Mode

Sandbox mode is the default mode of the plugin. It uses the sandbox credentials provided by MMG.

This is used for testing the plugin and for development purposes.