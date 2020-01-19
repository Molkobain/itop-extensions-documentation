👋 [Available on Molkobain I/O](https://www.molkobain.com/product/markdown-viewer/)

# iTop extension: molkobain-markdown-viewer
* [Description](#description)
* [Online demo](#online-demo)
* [Compatibility](#compatibility)
* [Downloads](#downloads)
* [Installation](#installation)
* [Configuration](#configuration)
* [Change log](CHANGELOG.md)

## Description
Easily edit fields in Markdown without any modification to your datamodel! Perfect for FAQs and many others objects 👌

Advanced features support such as headings, emphasis, lists, images, hyperlinks, highlighting, code formatting...

![Description decoration](docs/mmv-console-edition-01.png)

Instant preview of Markdown rendering while editing
![Preview while editing](docs/mmv-console-preview-01.png)

Fully compatible with the enhanced portal in both visualization...
![Portal visualization](docs/mmv-portal-view-01.png)

... and edition with instant preview
![Portal editing](docs/mmv-portal-edition-01.png)
![Portal preview](docs/mmv-portal-preview-01.png)

## Online demo
You can try this extension on the online demo. There are already some FAQs with a markdown description as an example. Just click on the links below to access it:
* [Administration console](http://mbc.itop.molkobain.com/pages/UI.php?operation=details&class=FAQ&id=1&c[menu]=FAQ&auth_user=admin&auth_pwd=admin) (admin / admin)
* [Enhanced portal](http://mbc.itop.molkobain.com/pages/exec.php/object/view/FAQ/1?exec_module=itop-portal-base&exec_page=index.php&portal_id=itop-portal&auth_user=portal&auth_pwd=portal) (portal / portal)

*Note: Mind to logout before switching between console & portal.*

## Compatibility
Compatible with iTop 2.4+

## Dependencies
* Module `molkobain-handy-framework/1.3.0`
* Module `molkobain-newsroom-provider/1.0.1`

*Note: All dependencies are included in the `dist/` folder, so all you need to do is follow the installation section below.*

## Downloads
Stable releases can be found on the [releases page](https://github.com/Molkobain/itop-markdown-viewer/releases) or on [Molkobain I/O](https://www.molkobain.com/product/markdown-viewer/).

Downloading it directly from the Clone or download will get you the version under development which might be unstable.

## Installation
* Unzip the extension
* Copy the ``molkobain-markdown-viewer`` folder under ``<PATH_TO_ITOP>/extensions`` folder of your iTop
* Run iTop setup & select extension *Markdown editor*

*Your folders should look like this*

![Extensions folder](docs/mmv-install.png)

## Configuration
Out of the box this extension doesn't change any attributes, you have to configure which attributes you want to be rendered as Markdown. To do so, take a look at the ``markdown_attributes`` parameter in the next section.

### Parameters
Some configuration parameters are available from the Configuration editor of the console:
* ``enabled`` Enable / disable the extension without having to uninstall it. Value can be ``true`` or ``false``.
* ``markdown_attributes`` Class attributes to enable as Markdown. Value must be an array of classes, each containing an array of the attributes you want to render as Markdown. Default value is none, you have to set which ones you want!

*Example:*
```
'molkobain-markdown-viewer' => array (
  'enabled' => true,
  'markdown_attributes' => array(
    'Service' => array('description'),
    'ServiceSubcategory' => array('description'),
    'FAQ' => array('summary', 'description'),
  ),
),
```

## Contributors
I would like to give a special thank you to the people who contributed to this:
 - Bostoen, Jeffrey a.k.a @jbostoen
 
## Licensing
This extension is under [AGPLv3](https://en.wikipedia.org/wiki/GNU_Affero_General_Public_License).

## Third party libs
This extension is based on the awesome Showdown library. For more information visit its [website](https://github.com/showdownjs/showdown).
