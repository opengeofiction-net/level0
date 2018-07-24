# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).
This project does NOT adhere to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Add `console_auth.php` for interacting with [pyLevel0](https://github.com/Zverik/pyLevel0).
- Add a logo.

### Fixed
- Fixed user names with quotes.

### Changed
- All links are now HTTPS.
- Stop using Content Delivery Networks to serve Leaflet.

## [1.2] - 2016-09-02
### Added
- Added support for obsolete `/browse` osm.org links.
- Relations are visualized, with referenced members highlighed. [#15](https://github.com/Zverik/Level0/issues/15)  (by @tyrasd)

### Fixed
- Fixed deletion order, so no conflicts occur. [#27](https://github.com/Zverik/Level0/issues/27)
- Deletion and addition of relation members did not register as changes. [#22](https://github.com/Zverik/Level0/issues/22)

### Changed
- Changeset comment is preserved when using other buttons. [#18](https://github.com/Zverik/Level0/pull/18) (by @jgpacker)
- Pressing "Enter" in the changeset comment field now uploads changes. [#20](https://github.com/Zverik/Level0/issues/20)
- Changeset number is now a link. [#14](https://github.com/Zverik/Level0/issues/14)
- Map state is kept between sessions. [#16](https://github.com/Zverik/Level0/issues/16)
- Made messages a bit smaller.

### Removed
- Removed "follow cursor" and "text2coord" buttons.

## [1.1] - 2014-05-20
### Added
- Overpass API links are now allowed. [#1](https://github.com/Zverik/Level0/issues/1)
- "Show osmChange" button. [#11](https://github.com/Zverik/Level0/issues/11)
- Editing changeset tags is now possible. [#12](https://github.com/Zverik/Level0/issues/12), [#7](https://github.com/Zverik/Level0/issues/7)

### Changed
- Enforced object limit for downloading.
- Tabs and newlines are now replaced with spaces on download. [#9](https://github.com/Zverik/Level0/issues/9)
- Now skipping some messages when there are more than 10.
- Ways are now drawn in the map view even when the cursor is not on a node reference. [#2](https://github.com/Zverik/Level0/issues/2)
- Language strings for nodes containing identifiers were rewritten to use `%s` instead of `%d`.

### Fixed
- Fixed parsing object links with hashes from osm.org. [#4](https://github.com/Zverik/Level0/issues/4)
- When displayed key / value differs from downloaded, the object is marked as modified. [#10](https://github.com/Zverik/Level0/issues/10)
- Fixed processing `\=` in Level0l. [#8](https://github.com/Zverik/Level0/issues/8)
- Stream opening errors are now properly reported.

## [1.0] - [2014-04-27]

Initial release
