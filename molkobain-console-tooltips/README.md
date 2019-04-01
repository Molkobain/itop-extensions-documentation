👋 Available on [iTop Hub](https://store.itophub.io/en_US/products/molkobain-console-tooltips) & [Molkobain I/O!](https://www.molkobain.com/product/console-tooltips/)

# iTop extension: molkobain-console-tooltips
* [Description](#description)
* [Compatibility](#compatibility)
* [Downloads](#downloads)
* [Installation](#installation)
* [Configuration](#configuration)

## Description
Display a tooltip on object's attributes (console only). A ? is added next to the attribute's label to indicate that a description is available for an attribute.

Works with all objects (standard / from extensions / custom made), but only attributes for which a description exists will be affected.

Can be set on any field, to provide a long description to explain the usage of a particular field. This description can be more explicit to explain the meaning and expected usage of the field.

Description comes from iTop's dictionary entry ``'Class:<CLASS_NAME>/Attribute:<ATTRIBUTE_CODE>+' => 'Some description about the attribute'``.

As part of the standard datamodel, only few fields have such description documented, especially because it is specific to the way an organization uses iTop. But with this extension, it's a good opportunity to enrich your dictionnary with business tooltips for online guidance to your users.

*Note: By default iTop has not much descriptions, if you want to add some, you have to add dictionary entries.*

![Description decoration](https://raw.githubusercontent.com/Molkobain/itop-console-tooltips/develop/docs/mct-object-01.PNG)
![Description tooltip](https://raw.githubusercontent.com/Molkobain/itop-console-tooltips/develop/docs/mct-object-02.PNG)

## Compatibility
Compatible with iTop 2.3+

## Dependencies
* Module `molkobain-handy-framework/1.0.0`

*Note: All dependencies are included in the `dist/` folder, so all you need to do is follow the installation section below.*

## Downloads
Stable releases can be found either on the [releases page](https://github.com/Molkobain/itop-console-tooltips/releases), [iTop Hub](https://store.itophub.io/en_US/products/molkobain-console-tooltips) or on [Molkobain I/O](https://www.molkobain.com/product/console-tooltips/).

Downloading it directly from the *Clone or download* will get you the version under development which might be unstable.

## Installation
* Unzip the extension
* Copy the ``dist/molkobain-console-tooltip`` folder under ``<PATH_TO_ITOP>/extensions`` folder of your iTop
* Run iTop setup & select extension *Attributes description tooltip*

*Your folders should look like this*

![Extensions folder](https://raw.githubusercontent.com/Molkobain/itop-console-tooltips/develop/docs/mct-install.PNG)

## Configuration
### Parameters
The extension has 2 configuration parameters:
  * decoration_class: Change tooltip icon by setting any *Font Awesome 5* icon classes (see [here](https://fontawesome.com/icons?d=gallery&m=free)  for examples). Default is ``fas fa-question``.
  * enabled: Enable or disable extension. Possible values are true|false, default is true.

## Licensing
This extension is under [AGPLv3](https://en.wikipedia.org/wiki/GNU_Affero_General_Public_License).

## Third party libs
This extension embeds the Font Awesome 5.0.6 library. For more information visit its [website](https://fontawesome.com).
