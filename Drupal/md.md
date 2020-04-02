# CONTENTS OF THIS FILE

 * Introduction
 * Requirements
 * Installation
 * Configuration
 * Maintainers


## INTRODUCTION

The Cloudflare Bypass module automatically adds logged in users to the
Cloudflare firewall bypass.

This will allow them to bypass any extra filtering put in place by Cloudflare.

 * For a full description of the module, visit the project page:
   https://drupal.org/project/cloudflare_bypass

 * To submit bug reports and feature suggestions, or to track changes:
   https://drupal.org/project/issues/cloudflare_bypass


## REQUIREMENTS

This module requires no modules outside of Drupal core.


## INSTALLATION

 * Install as you would normally install a contributed Drupal module. Visit:
   https://www.drupal.org/node/895232 for further information.


## CONFIGURATION

The module provides a UI to see all the rules added by the module and the
ability to delete them. The admin url is
`/admin/config/development/cloudflare-whitelist`

This module works with `v4` of the [Cloudflare API](https://api.cloudflare.com/#user-level-firewall-access-rule-properties).


### Cloudflare API.

Get your Cloudflare API key from the My Profile page in Cloudflare.
You will want the `Global API Key`.


### Drupal

You need to add the following config to your `settings.php` file.

The email is the email address you use to login in to Cloudflare.

```php
  $conf['cloudflare_bypass_auth_email'] = 'example@example.com';
  $conf['cloudflare_bypass_auth_key'] = 'XXXXXXXXX9999999';
```

Alternatively you can also set those variables with Drush

```bash
drush vset cloudflare_bypass_auth_email 'example@example.com'
drush vset cloudflare_bypass_auth_key 'XXXXXXXXX9999999'
``` 

## MAINTAINERS

Current maintainers:
 * [Paul Sheldrake - paulsheldrake](https://www.drupal.org/u/paulsheldrake)
 * [AmyJune Hineline - volkswagenchick](https://www.drupal.org/u/volkswagenchick)

This project is sponsored by:
 * [Kanopi Studios](https://www.drupal.org/kanopi-studios)

Special thanks to the [Mises Institute](http://mises.org) for sharing.
