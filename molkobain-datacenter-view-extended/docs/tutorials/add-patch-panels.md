<button onclick="history.back()">Back</button>

# Add patch panels and display them

* [Introduction](#introduction)
* [Step 1 - Install the Cable Management extension](#step-1---install-the-cable-management-extension)
* [Step 2 - Register PatchPanel class for the graphical view](#step-2---register-patchpanel-class-for-the-graphical-view)

## Introduction

Patch panels are not part of the standard iTop datamodel, but they can be easily added and integrated with _Datacenter View Extended_ thanks to [TeemIP](https://www.teemip.net/) great and free [Cable Management](https://wiki.teemip.net/doku.php?id=extensions:teemip-cable-mgmt) extension.

Here is a brief summary of its features:
* New `PatchPanel` objects
* New `NetworkSocket` objects
* New `Cable` objects
* Enhanced `PhysicalInterface` objects
* Wiring diagram

![](https://wiki.teemip.net/lib/exe/fetch.php?media=extensions:cabling_scenarios.png)
_Overview - Copyright [TeemIP](https://www.teemip.net)_

## Step 1 - Install the _Cable Management_ extension

* Retrieve **v1.1.0** or newer of the extension either on
  * Community users: iTop Hub or [GitHub](https://github.com/TeemIp/teemip-cable-mgmt)
  * Combodo's customers: Contact Combodo's support
* Install the extension as usual

## Step 2 - Register `PatchPanel` class for the graphical view

* Open iTop configuration file
* Find `molkobain-datacenter-view-extended` section
* Add `PatchPanel` to the array of custom classes (to be displayed in the graphical view) in the `custom_device_classes` parameter
* Save configuration file

You should have something similar to this:
```php
'molkobain-datacenter-view-extended' => array (
    'custom_device_classes' => ['CustomClassA', 'CustomClassB', 'PatchPanel'],
),
```



