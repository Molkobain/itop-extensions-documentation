👋 Available on [iTop Hub](https://store.itophub.io/en_US/products/molkobain-bubble-caselogs) and [Molkobain I/O](https://www.molkobain.com/product/bubble-caselogs/)

# iTop extension: molkobain-bubble-caselogs
* [Description](#description)
* [Online demo](#online-demo)
* [Compatibility](#compatibility)
* [Downloads](#downloads)
* [Installation](#installation)
* [Configuration](#configuration)
* [Change log](CHANGELOG.md)

## Support
If you like this project, you can buy me beer, always appreciated! 🍻😁

[![Donate](https://img.shields.io/static/v1?label=Donate&message=Molkobain%20I/O&color=green&style=flat&logo=paypal)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=BZR88J33D4RG6&source=url)

## Description
This extension changes the look and feel of the caselogs in both the enhanced portal and the console to make it look like modern messaging applications.

It also allows you to:
* Easily distinguish users of the conversation through colors and profile pictures.
* Open / close all messages at once.

![Description decoration](docs/mbc-portal-example-01.png)

## Online demo
You can try this extension on the online demo. There is already a user request with a detailled public log as an example. Just click on the links below to access it:
* [Administration console](http://mbc.itop.molkobain.com/pages/UI.php?operation=details&class=UserRequest&id=2&auth_user=admin&auth_pwd=admin) (admin / admin)
* [Enhanced portal](http://mbc.itop.molkobain.com/pages/exec.php/manage/ongoing-tickets-for-portal-user?exec_module=itop-portal-base&exec_page=index.php&portal_id=itop-portal&auth_user=portal&auth_pwd=portal) (portal / portal)

*Note: Mind to logout before switching between console & portal.*

## Compatibility
Compatible with iTop 2.4 to 2.7\
Obsolete for iTop 3.0+ as it is now directly included in iTop 🙌

## Dependencies
* Module `molkobain-fontawesome5-pack`
* Module `molkobain-handy-framework`
* Module `molkobain-newsroom-provider`

## Downloads
Stable releases can be found on [Molkobain I/O](https://www.molkobain.com/product/bubble-caselogs/).

## Installation
Installation procedure is the same as for any iTop extension, just follow the instruction on the iTop official documentation [here](https://www.itophub.io/wiki/page?id=extensions%3Ainstallation).

## Configuration
No configuration needed, the extension can be used out of the box!

### Parameters
Some configuration parameters are available from the Configuration editor of the console:
* ``enabled`` Enable / disable the extension without having to uninstall it. Value can be ``true`` or ``false``.
* ``all_entries_opened`` Open all messages by default instead of only the first 2. Value can be ``true`` or ``false``.
* ``reverse_order`` Display messages in a chronological order. Value can be ``true`` or ``false``.
* ``disabled_in_backoffice`` Disable rendering in the admin. console. Value can be `true` or `false`.
* ``disabled_in_portals`` Disable rendering in the end-user portals. Value can be `true` or `false`.
* ``open_all_icon`` CSS classes of the *open* icon, allows you to choose any FontAwesome icon. Value must be a string of CSS classes separated by a space (eg. ``'fas fa-book-open'``).
* ``close_all_icon`` CSS classes of the *close* icon, allows you to choose any FontAwesome icon. Value must be a string of CSS classes separated by a space (eg. ``'fas fa-book'``).
* ``icons_separator`` Separator of the 2 icons. Value must be a string (eg. ``'-'``).

*Example:*
```
'molkobain-bubble-caselogs' => array (
  'enabled' => true,
  'all_entries_opened' => false,
  'reverse_order' => false,
  'disabled_in_backoffice' => false,
  'disabled_in_portals' => false,
  'open_all_icon' => 'fas fa-book-open',
  'close_all_icon' => 'fas fa-book',
  'icons_separator' => '-',
),
```

## Contributors
I would like to give a special thank you to those who contributed to this project, including:

### Aliases
- @pcadeot

## Licensing
This extension is under [AGPLv3](https://en.wikipedia.org/wiki/GNU_Affero_General_Public_License).
