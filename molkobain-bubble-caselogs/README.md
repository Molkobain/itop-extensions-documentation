👋 [Available on Molkobain I/O](https://www.molkobain.com/product/bubble-caselogs/)

# iTop extension: molkobain-bubble-caselogs
* [Description](#description)
* [Compatibility](#compatibility)
* [Downloads](#downloads)
* [Installation](#installation)
* [Configuration](#configuration)

### Description
This extension changes the look and feel of the caselogs in both the enhanced portal and the console to make it look like modern messaging applications.

It also allows you to:
* Easily distinguish users of the conversation through colors and profile pictures.
* Open / close all messages at once.

![Description decoration](https://raw.githubusercontent.com/Molkobain/itop-bubble-caselogs/develop/docs/mbc-portal-example-01.png)

### Compatibility
Compatible with iTop 2.4+

## Dependencies
* Module `molkobain-fontawesome5-pack/1.1.0`
* Module `molkobain-handy-framework/1.1.0`

## Downloads
Stable releases can be found either on the [releases page](https://github.com/Molkobain/itop-bubble-caselogs/releases) or on [Molkobain I/O](https://www.molkobain.com/product/bubble-caselogs/).

Downloading it directly from the *Clone or download* will get you the version under development which might be unstable.

### Installation
* Unzip the extension
* Copy the ``dist/molkobain-bubble-caselogs`` folder under ``<PATH_TO_ITOP>/extensions`` folder of your iTop
* Run iTop setup & select extension *Bubble caselogs*

*Your folders should look like this*

![Extensions folder](https://raw.githubusercontent.com/Molkobain/itop-bubble-caselogs/develop/docs/mbc-install.png)

### Configuration
No configuration needed.

#### Parameters
Some configuration parameters are available from the Configuration editor of the console:
* ``enabled`` Enable / disable the extension without having to uninstall it. Value can be ``true`` or ``false``.
* ``all_entries_opened`` Open all messages by default instead of only the first 2. Value can be ``true`` or ``false``.
* ``reverse_order`` Display messages in a chronological order. Value can be ``true`` or ``false``.
* ``open_all_icon`` CSS classes of the *open* icon, allows you to choose any FontAwesome icon. Value must be a string of CSS classes separated by a space (eg. ``'fas fa-book-open'``).
* ``close_all_icon`` CSS classes of the *close* icon, allows you to choose any FontAwesome icon. Value must be a string of CSS classes separated by a space (eg. ``'fas fa-book'``).
* ``icons_separator`` Separator of the 2 icons. Value must be a string (eg. ``'-'``).

### Licensing
This extension is bound by the license you purchased. A license grants you a non-exclusive and non-transferable right to use and incorporate the item in your personal or commercial projects. There are several [licenses available](https://www.molkobain.com/usage-licenses/).
