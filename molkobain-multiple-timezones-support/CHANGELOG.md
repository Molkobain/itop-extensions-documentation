# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

## [1.3.1] - 2024-02-27
### Changed
- Fix timezone selector options height in iTop 3.0+

## [1.3.0] - 2023-09-09
### Added
- Add compatibility with iTop 3.1+

### Changed
- Update dependancies

## [1.2.0] - 2023-04-14
### Added
- Add support for log entries dates
  - End-user portal: Only works wirh default date/timeformat due to iTop's lacks of metadata
  - Backoffice: Only works with iTop 3.0+ due to lack of metadata

## [1.1.1] - 2023-03-01
### Changed
- Fix crash due to wrong stylesheet compilation (variables.scss not found for import)

## [1.1.0]
### Added
- Add compatibility with iTop 3.0.1+ (but NOT iTop 3.0.0 due to a regression in the app APIs 😕)
- **[iTop 3.0+ only]** Add timezone display in tables that are automatically refreshed

## [1.0.1] - 2021-03-10
### Changed
- Fixed multiple timezone icons in stimulus forms

## [1.0.0] - 2020-05-27
### Added
- First version

[Unreleased]: https://github.com/Molkobain/itop-multiple-timezones-support/compare/v1.3.1...HEAD
[1.3.1]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.1
[1.3.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.0
[1.2.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.2.0
[1.1.1]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.1.1
[1.1.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.1.0
[1.0.1]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.0.1
[1.0.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.0.0