👋 [Available on Molkobain I/O!](https://www.molkobain.com/product/multiple-timezones-support/)

# iTop extension: Multiple Timezones Support
* [Description](#description)
* [Limitations](#limitations)
* [Compatibility](#compatibility)
* [Downloads](#downloads)
* [Installation](#installation)
* [Configuration](#configuration)
* [Third parties](#third-parties)

## Support
If you like this project, you can buy me beer, always appreciated! 🍻😁

[![Donate](https://img.shields.io/static/v1?label=Donate&message=Molkobain%20I/O&color=green&style=flat&logo=paypal)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=BZR88J33D4RG6&source=url)

## Description
Allow users to see or edit dates & times in their own timezone instead of the server's default one. Perfect for:

  * Companies with employees or customers accross several countries
  * Planning changes safely with everyone seeing the right time (no more math!)

![Description decoration](docs/mmts-wizard-01.png)

### User setup
Easy on the users with a simple wizard to set up their timezone, they can either choose to let the app find their timezone and adjust it when they travel...

![](docs/mmts-wizard-02-auto.png)

... or they can choose a specific timezone and stick to it (useful when working with a remote team) ...

![](docs/mmts-wizard-02-user.png)

... and, that's all! Timezone can be changed at any time in the user preferences.

![](docs/mmts-wizard-03.png)

### How it looks
Any dates & times attributes in the UI will automatically be converted, a small icon indicates that it is now displayed in the user's timezone. (see [limitations](#limitations)). Works in both the backoffice and the end-users portal.

*Backoffice lists*
![](docs/mmts-console-lists.png)

*Backoffice object details*
![](docs/mmts-console-fields.png)

*Portal lists*
![](docs/mmts-portal-lists.png)

## Limitations
**IMPORTANT: Before buying it, make sure you have read the following limitations.**

For the moment some parts of the application are NOT compatible with the timezones:

  * Notifications
  * Imports / exports
  * REST/JSON API
  * SLA computations are made based on the iTop server timezone, but on the user’s
  * **[iTop 2.7.x]** Tables that are automatically refreshed

## Compatibility
Compatible with iTop 2.7.x and 3.0.**1**+. \
**NOT** compatible with iTop 3.0.**0** due to a regression in the app APIs. 😕

## Downloads
Stable releases can only be found on [Molkobain I/O](https://www.molkobain.com/product/multiple-timezones-support/).

## Installation
Installation procedure is the same as for any iTop extension, just follow the instruction on the iTop official documentation [here](https://www.itophub.io/wiki/page?id=extensions%3Ainstallation).

## Configuration
No configuration needed, each user will be prompt to choose its timezone on next login.

### Parameters
Some configuration parameters are available from the Configuration editor of the console:

  * `enabled` Enable / disable the extension without having to uninstall it. Value can be `true` or `false`.
  * `disabled_guis` Specify for which GUIs the extension should be disabled, for example if you only want to use it in the backoffice and not in the end-users portal. Values can be `backoffice`, `itop-portal` or any other portal instance ID.

*Default values:*
```
'enabled' => true,
'disabled_guis' => array(),
```

## Third parties
This extension embeds some third-party resources:

  * [Moment Timezone](https://momentjs.com/timezone/) for dates & times manipulations
  * Cover image used in the wizard & documentation is from [RAStudio](https://www.vectorstock.com/royalty-free-vectors/vectors-by_RAStudio)