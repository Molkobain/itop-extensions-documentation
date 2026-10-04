# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

## [1.6.0] - 2026-10-04
### Changed
  * Fix rendering of HTML attributes (edited with the rich text editor) which were rendered on a single line
  * Fix security issue (XSS): HTML generated from the Markdown is now sanitized with DOMPurify, following the rules of the HTML sanitizer configured in iTop (`html_sanitizer` parameter)
  * Fix preview of HTML attributes not showing the last changes when opened right after typing
  * Fix paragraphs of plain text attributes being merged when their line endings are not CRLF (eg. value set through the REST API or an import)
  * Fix invalid classes / attributes in the `markdown_attributes` parameter breaking the display, they are now ignored

## [1.5.0] - 2026-08-03
### Changed
  * Add compatibility with iTop 3.3+
  * Change iTop min. version 3.2.0

## [1.4.0] - 2022-09-25
### Changed
  * Add compatibility with iTop 3.0+
  * Change iTop min. version 2.7.0

## [1.3.0] - 2020-08-18
### Added
  * Add possibility to choose Mardown converter options

## [1.2.0] - 2019-12-31
### Changed
  * Fix display in the admin. console
  * Add compatibility with iTop 2.7+

### Added
  * Add dutch translations (Thanks to @jbostoen!)

## [1.1.3] - 2019-11-30
### Changed
  * Fix display in the end-user portal

## [1.1.2] - 2019-07-24
### Changed
  * Update dependencies to include their fixes

## [1.1.1] - 2019-07-23
### Changed
  * Fix rendering of line breaks on read-only attributes (preview was ok)

## [1.1.0] - 2019-07-23
### Added
  * Include "Molkobain's newsroom provider" module to keep administrators informed on new extensions and updates (can be disabled in the conf. file) (iTop 2.6+ only)

## [1.0.0] - 2019-04-05
### Added
  * First version

[Unreleased]: https://github.com/Molkobain/itop-markdown-viewer/compare/v1.6.0...HEAD
[1.6.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.6.0
[1.5.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.5.0
[1.4.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.4.0
[1.3.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.3.0
[1.2.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.2.0
[1.1.3]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.1.3
[1.1.2]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.1.2
[1.1.1]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.1.1
[1.1.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.1.0
[1.0.0]: https://github.com/Molkobain/itop-markdown-viewer/releases/tag/v1.0.0