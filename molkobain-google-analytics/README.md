👋 [Available on Molkobain I/O](https://www.molkobain.com/product/google-analytics/)

# iTop extension: molkobain-google-analytics
* [Description](#description)
* [Compatibility](#compatibility)
* [Downloads](#downloads)
* [Installation](#installation)
* [Configuration](#configuration)
* [Change log](CHANGELOG.md)

## Support
If you like this project, you can buy me beer, always appreciated! 🍻😁

[![Donate](https://img.shields.io/static/v1?label=Donate&message=Molkobain%20I/O&color=green&style=flat&logo=paypal)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=BZR88J33D4RG6&source=url)

## Description
Enable Google Analytics reporting on your iTop instance within seconds! Just put your tracking code in the configuration file and you are good to go. Reporting can be enabled on both the admin. console and the end-user portal.

Features:
* Works on both the admin. console and end-user portal.
* Different tracking codes can be set to the admin. console and end-user portal.
* Supports multi end-user portal setups, just add portal IDs in the configuration file.
* Option to not track specific users, IPs or profiles (e.g. administrators).

## Compatibility
Compatible with iTop 3.2+

## Downloads
Stable releases can be found either on the [releases page](https://github.com/Molkobain/itop-google-analytics/releases) or on [Molkobain I/O](https://www.molkobain.com/product/google-analytics/).

Downloading it directly from the *Clone or download* will get you the version under development which might be unstable.

## Installation
Installation procedure is the same as for any iTop extension, just follow the instruction on the iTop official documentation [here](https://www.itophub.io/wiki/page?id=extensions%3Ainstallation).

## Configuration
Get tracking codes from Google Analytics' website and put them in the tracking_codes parameter (see below).

### Parameters
Some configuration parameters are available from the Configuration editor of the console:
  * `enabled`: Enable or disable extension. Possible values are `true`|`false`, default is `true`.
  * `tracking_codes`: Tracking code for each iTop "portal". `backoffice` being the admin. console, `itop-portal` the standard end-user portal. You can add any other end-user portal instance you have by adding `'PORTAL_ID' => 'TRACKING_CODE',` to the list.
  * `ignored_profiles`: Ignore specific profiles with a list of profiles. Value must be an array of profiles (e.g. `['Administrator']`), default is an empty array.
  * `ignored_users`: Ignore specific users with a list of user logins. Value must be an array of logins (e.g. `['admin', 'test-user']`), default is an empty array.
  * `ignored_ips`: Ignore specific IPs within a list. Value must be an array of strings (e.g. `['123.456.789.999', '192.168.0.1']`), default is an empty array.

*Example:*
```
'molkobain-google-analytics' => array (
  'enabled' => true,
  'tracking_codes' => array (
    'backoffice' => 'FIRST_TRACKING_CODE',
    'itop-portal' => 'SECOND_TRACKING_CODE',
  ),
  'ignored_profiles' => [],
  'ignored_users' => [],
  'ignored_ips' => [],
),
```


## Licensing
This extension is under [AGPLv3](https://en.wikipedia.org/wiki/GNU_Affero_General_Public_License).
