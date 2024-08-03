---
sidebar_position: 3
---

# Frequently Asked Questions

Here are some common questions and answers about the MMG Checkout Payment plugin:

## General Questions

### What is MMG Checkout Payment?
MMG Checkout Payment is a WordPress plugin that integrates with WooCommerce to provide a secure payment gateway for MMG merchants to receive e-commerce payments from MMG customers.

### Who can use this plugin?
This plugin is designed for registered MMG Merchants who want to accept payments through MMG Checkout on their WordPress-based e-commerce stores.

### Is this plugin free?
Yes, the plugin itself is free to download and use. However, you need to have an MMG Merchant account to process payments.

## Setup and Configuration

### How do I install the plugin?
You can install the plugin by downloading it from our GitHub repository and uploading it to your WordPress site. Detailed installation instructions are available in our [Quick Start Guide](/docs/quick-start).

### What are the system requirements?
The plugin requires:
- WordPress 6.0 or later
- WooCommerce 7.0 or later
- PHP 7.4 or later
- mbstring PHP extension
- SSL certificate for your website

### How do I get API credentials?
You need to contact MMG Merchant Services to request API credentials. You can do this by [sending an email](mailto:merchantservices@mmg.gy?subject=Request%20for%20MMG%20Checkout%20API%20Credentials).

MMG will need you to provide the following information:
- Response URL and Error URL for your store (this is the Callback URL that can be found in the [Quick Start Guide](/docs/quick-start#configure-the-plugin))
- Your Public Key

### What is the difference between Live and Sandbox mode?
Sandbox mode is for testing the plugin without processing real transactions. Live mode is for processing actual payments from customers.

## Security and Compliance

### Is this plugin secure?
Yes, automated security checks are performed to ensure the plugin is secure and compliant with best practices.

### Do I need an SSL certificate?
Yes, an SSL certificate is required to ensure secure transmission of payment data from your website.

### How are customer payment details handled?
Customer payment details are securely transmitted to MMG and are not stored on your WordPress site.

## Troubleshooting

### What should I do if a payment fails?
Check your API credentials and ensure your account is in good standing. If issues persist, contact MMG Merchant Support.

### The plugin isn't showing up in WooCommerce payment methods. What should I do?
Ensure the plugin is activated and properly configured in the WordPress admin area. If it still doesn't appear, check for any conflicts with other plugins.

### Where can I get support if I have more questions?
For additional support, please contact [Kalpa Services](mailto:hello@kalpa.dev?subject=MMG%20Checkout%20Payment%20Plugin%20Support) or refer to our detailed documentation.
