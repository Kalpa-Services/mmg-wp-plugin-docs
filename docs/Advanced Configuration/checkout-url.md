---
sidebar_position: 1
description: A safer way to set the checkout URL.
---

# Checkout URL

This is the base URL of MMG's hosted checkout page. When a customer clicks on **Pay via MMG**, the plugin will redirect the customer to this URL with the base64 encoded order data.

Though these are provided by default, it is recommended to set these in the `wp-config.php` file to avoid it being accidentally changed.

The checkout URL can be set in the `wp-config.php` file by adding the following code:

```php
define('MMG_LIVE_CHECKOUT_URL', 'https://gtt-checkout.qpass.com:8743/checkout-endpoint/home');
define('MMG_DEMO_CHECKOUT_URL', 'https://gtt-uat-checkout.qpass.com:8743/checkout-endpoint/home');
```

After adding these constants, the plugin will use these URLs instead of the default ones or the ones set in the WordPress admin settings.

In the event that you need to change the checkout URL, you can do so by updating the constants in the `wp-config.php` file.