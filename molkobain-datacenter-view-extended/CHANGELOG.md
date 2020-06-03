# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## Unreleased

## [1.5.0] - 2020-06-03
### Added
- Add weight capacity for racks and enclosures
- Add expected power requirement for racks and enclosures
- Add typology and basic hierarchy on Location to prepare rooms graphical view

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

[Unreleased]: https://github.com/Molkobain/itop-datacenter-view-extended/compare/v1.4.1...HEAD
[1.4.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.4.1
[1.4.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.4.0
[1.3.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.3.0
[1.2.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.2.0
[1.1.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.1.1
[1.1.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.1.0
[1.0.1]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.0.1
[1.0.0]: https://github.com/Molkobain/itop-datacenter-view-extended/releases/tag/v1.0.0