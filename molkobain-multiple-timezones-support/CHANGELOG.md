# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

## [1.3.6] - 2026-02-14
### Changed
- Disable extension when a user is impersonating another one to avoid having the blocking wizard modal

## [1.3.5] - 2025-12-05
### Changed
- Fix packaging issue causing missing update of French dictionary

## [1.3.4] - 2025-12-03
### Changed
- Fix initial modal size being too big and small screens (height < 800px)
- Fix typo in French dictionary

## [1.3.3] - 2025-11-28
### Changed
- Update dependencies

## [1.3.2] - 2025-11-15
### Changed
- Fix crash when installing extension in "test" environment if it isn't in the "production" environment yet
- Fix conversion not done in some modals of the backoffice

## [1.3.1] - 2024-02-27
### Changed
- Fix timezone selector options height in iTop 3.0+

## [1.3.0] - 2023-09-09
### Added
- Add compatibility with iTop 3.1+

### Changed
- Update dependencies

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

[Unreleased]: https://github.com/Molkobain/itop-multiple-timezones-support/compare/v1.3.6...HEAD
[1.3.6]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.6
[1.3.5]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.5
[1.3.4]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.4
[1.3.3]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.3
[1.3.2]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.2
[1.3.1]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.1
[1.3.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.3.0
[1.2.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.2.0
[1.1.1]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.1.1
[1.1.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.1.0
[1.0.1]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.0.1
[1.0.0]: https://github.com/Molkobain/itop-multiple-timezones-support/releases/tag/v1.0.0