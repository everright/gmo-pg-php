GMO Payment Gateway
===================

This is a PHP library for the GMO Payment Gateway, supporting the PG Multi Payment API, exec transactions, register users, and so on.

Installation
------------

```bash
composer install gmo-pg-php
```

Usage
-----

```php
$host = '';
$site_id = '';
$site_pass = '';
$site = new \GMO\Payment\SiteApi($host, $site_id, $site_pass);
$member_id = '';
$card_no = '';
$expire = '';
$card = '';

try {
  $data = $site->updateCard($member_id, $card_no, $expire, $card);
  print_r($data);
}
catch (exception $e) {
  print $e->getMessage();
}
```
More examples are available on examples directory.

Shop API
--------

In this library, we have defined as "Shop API" an API that requires shop ID and shop password to the API call.

Site API
--------

An API that requires site ID and site password to the API call.

ShopAndSite API
---------------

An API that requires shop ID, shop password, site ID and site password to the API call.
