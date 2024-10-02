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

## Get account credentials from MMG

Email merchantservices@mmg.gy to get the necessary account credentials to use the [Checkout API](https://developer.mmg.gy/api/details/checkout_payment)

:::note
Treat these keys like passwords. They are not to be shared and kept secret.
:::

## Configure the plugin

- Go to 'Settings' > 'MMG Checkout' to configure the plugin.
- Copy the Callback URL and send it to the MMG team for them to configure your store's **response and error URLs**.
- Enter your MMG Merchant credentials:
  - Merchant Name (if different from site title)
  - Live Client ID
  - Live Merchant ID
  - Live Secret Key
  - Live RSA Public Key 
  - Live RSA Private Key
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
