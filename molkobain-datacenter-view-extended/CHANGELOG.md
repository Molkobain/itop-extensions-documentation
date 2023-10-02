<button onclick="history.back()">Back</button>

# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## Unreleased

## [1.9.1] - 2023-10-02
### Changed
  * Fix compilation error due to wrong prototype for Molkobain\iTop\Extension\FontAwesome5\Console\Extension\PageUIExtension::GetLinkedStylesheetsAbsUrls()

## [1.9.0] - 2023-09-09
### Added
  * Add compatibility with iTop 3.1+
  * Add german translations thanks to [@mraenker](https://github.com/mraenker)
  * Include [bridge module for **IPAM for iTop**](https://github.com/Molkobain/itop-datacenter-view-extended-bridge-for-teemip) extensions thanks to [@xtophe38](https://github.com/xtophe38) tip for auto select condition

### Changed
  * Increase iTop min. version to 2.7.0
  * Migrate deprecated usages of FontAwesome v4
  * Migrate deprecated usages of `\ajax_page` class
  * Remove molkobain-console-tooltips from mandatory dependencies as it is now included in iTop 3.0+
  * Fix dependencies marked as optional instead of mandatory (thanks to [@Hipska](https://github.com/Hipska))

## [1.8.2] - 2022-10-24
### Changed
  * Fix "access permissions" english translations being in french

## [1.8.1] - 2022-09-20
### Changed
  * Fix devices width glitch on enclosure with few columns
  * Fix compatibility with "Location hierarchy" extension

## [1.8.0] - 2022-06-12
### Added
  * Add warning message in graphical view when no height defined for racks / enclosures

### Changed
  * Fix enclosure layout wizard not opening on some browsers in iTop 3.0+
  * Fix "Undefined mixin mhf-font-size-12" on non "production" environments
  * Fix "Undefined variable $obj-class-enclosure-bg-color" on non "production" environments

## [1.7.2] - 2022-03-18
### Changed
- Fix crash during setup on servers with PHP warnings enabled
- Migrate deprecated calls

## [1.7.1] - 2022-01-24
### Changed
- Fix crash on "Datacenter slot" opening
- Update french dictionaries

## [1.7.0] - 2022-01-16
### Added
- Add "access permissions" on Location and FunctionalCI to document which Contact can access them and how
- Add counter on unmounted panels
- Add Czech and Swedish translations on most of the UI

### Changed
- Raise iTop min. version to 2.6.0

## [1.6.0] - 2021-03-31
### Added
- Add config. parameter "display_consistency_checks" to display or not consistency checks on an element update. Values can be true|false, default is true.

### Changed
- Rename config. parameter "enable_consistency_checks" to "enforce_consistency_checks".

## [1.5.0] - 2020-06-14
### Added
- Add weight capacity for racks and enclosures
- Add expected power requirement for racks and enclosures
- Add typology and basic hierarchy on Location to prepare rooms graphical view
- Add filter panel to highlight devices based on their name / serial number / asset number

### Changed
- Rework the enclosure properties presentation
- Show devices' label vertically on narrow devices
- Upgrade dependencies
- Change a bunch of method names (that should only be used by this extension)

## [1.4.2] - 2020-04-22
### Changed
- Fix "division by zero" warning

## [1.4.1] - 2020-03-23
### Changed
- Fix contracted power precision to 3 digits

## [1.4.0] - 2020-03-04
### Added
- Add power consumption attributes to the rack class

## [1.3.0] - 2020-01-15
### Added
- Add support for grid layout on enclosures

### Changed
- Upgrade dependencies

## [1.2.0] - 2019-11-12
### Added
- Add configuration parameter to customize devices colors ('custom_device_colors')

### Changed
- Split "occupancy rate" attribute in 2, one for each panels of racks and enclosures
- Change ReservedSlot color for a better differentiation with MiscEquipmentSlot
- Change datacenter slots tab title in racks and enclosures to something more intuitive
- Fix user rights for DatacenterSlot class (needed "Administrator" profile to create/edit)

## [1.1.1] - 2019-07-24
### Changed
- Update dependencies to include their fixes

## 1.1.0 - 2019-07-22
### Added
- Include "Molkobain's newsroom provider" module to keep administrators informed on new extensions and updates (can be disabled in the conf. file) (iTop 2.6+ only)

## 1.0.1 - 2019-07-09
### Added
- Add visual hint on enclosure's abstract layout to warn when obsolete elements are included

### Changed
- Fix dropped elements being positioned outside the host on some browsers

## 1.0.0 - 2019-07-02
### Added
- Initial release

[Unreleased]: https://github.com/Molkobain/itop-datacenter-view-extended/compare/v1.9.1...HEAD
[1.9.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.9.1
[1.9.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.9.0
[1.8.2]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.8.2
[1.8.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.8.1
[1.8.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.8.0
[1.7.2]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.7.2
[1.7.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.7.1
[1.7.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.7.0
[1.6.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.6.0
[1.5.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.5.0
[1.4.2]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.4.2
[1.4.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.4.1
[1.4.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.4.0
[1.3.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.3.0
[1.2.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.2.0
[1.1.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.1.1
[1.1.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.1.0
[1.0.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.0.1
[1.0.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.0.0
