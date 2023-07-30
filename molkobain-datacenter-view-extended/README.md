👋 Available exclusively on [iTop Hub](https://store.itophub.io/en_US/products/molkobain-datacenter-view-extended)

# iTop extension: molkobain-datacenter-view-extended

## Description
**Molkobain Datacenter View Extended** extension is the advanced (and paid) version of the free **[Molkobain Datacenter View](https://github.com/Molkobain/itop-datacenter-view)** extension. \
It includes everything the simple version has, plus advanced features / customizations.

## Documentation
### Features, usages, Q&As
  * [Graphical tab overview](docs/features/graphical-tab-overview.md)
  * [Drag & Drop](docs/features/drag-and-drop.md)
  * [Complex enclosures support (grid system)](docs/features/complex-enclosures.md)
  * [Occupancy rates](docs/features/occupancy-rates.md)
  * [Power capacity](docs/features/power-capacity.md)
  * [Weight capacity](docs/features/weight-capacity.md)
  * [Misc. slots](docs/features/misc-slots.md)
  * [Zero-U devices](docs/features/zero-u-devices.md)
  * [Consistency checks](docs/features/consistency-checks.md)
  * [Audit rules](docs/features/audit-rules.md)
  * [Misc. options](docs/features/misc-options.md)

### Limitations
#### Downgrade to simple version
If you want to remove the extended version of the extension to only keep the simple version, mind unlinking all elements off the hosts' (racks and enclosures) **rear panel** prior to it, otherwise elements from the rear panel will fallback on the front panel, overlapping genuine elements of the front panel.

### Installation & configuration
  * [Installation](docs/configuration/installation.md)
  * [Datamodel changes](docs/configuration/datamodel-changes.md)
  * [Configuration parameters](docs/configuration/configuration-parameters.md)
  * [Change log](./CHANGELOG.md)

### Tutorials
  * [How to use / position my own datamodel classes](docs/tutorials/custom-datamodel-classes.md)

## Online demo
You can try this extension on the online demo. There are already some racks, enclosures and devices mounted as an example. Just click on the links below to access it:
  * [Administration console](http://mbc.itop.molkobain.com/pages/UI.php?operation=details&class=Rack&id=15&c[menu]=SearchCIs&auth_user=admin&auth_pwd=admin#tabbedContent_0=8) (admin / admin)

## Licensing
This extension is not open source and is bound by the license choose you purchased. There are several licenses available, see [https://www.molkobain.com/usage-licenses](https://www.molkobain.com/usage-licenses) for more information.

## Dependencies
This extension embeds some resources that are necessary for it to work. \
Everything is included in the distributed packages, no extra effort needed.

### iTop modules

  * Module [molkobain-handy-framework](https://github.com/Molkobain/itop-handy-framework)
  * Module [molkobain-console-tooltips](https://github.com/Molkobain/itop-console-tooltips)
  * Module [molkobain-newsroom-provider](https://github.com/Molkobain/itop-newsroom-provider)

### Third parties

  * Zero-U panel icon (USB memory stick) comes from [Icons8](https://icons8.com/icon/FlnYHAW3wYBn/usb-memory-stick)
  * Some class icons come from [Icons8](https://icons8.com)

### Contributors
A huge thank you to the people who contribute to this module 🙌

  * Bostoen, Jeffrey ([@jbostoen](https://github.com/jbostoen))
  * Raenker, Martin ([@mraenker](https://github.com/mraenker))
