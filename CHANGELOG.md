# Changelog

All notable changes to this specification are listed here.
The format follows [Keep a Changelog 1.1.0](https://keepachangelog.com/en/1.1.0/),
and versions follow [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0] - 2026-11-04

### Changed

- NAM-006 now requires US spelling, such as `license` and `color`, instead of Canadian spelling.
- Every identifier example in the specification, the guides and the skill now uses US spelling.
- NAM-007 now gives the HTTP header field `Referer` as its example of a kept spelling, because `license` already follows NAM-006.
- Each outside standard links to its source where it is named, and each page that cites one has a References section.
- English text uses US spelling.

### Migration

- Names built under 0.1 with Canadian spelling, such as `licence` or `colour`, change to the US form, such as `license` or `color`.
- This change breaks code that uses those names. In the 0.x series, a minor version may break, so this is version 0.2.0.

## [0.1.0] - 2026-11-04

### Added

- Principles NAM-001 to NAM-009: English names with translated labels, term base words, characters, abbreviations, spelling, outside names, reserved words and length.
- Case and word form NAM-010 to NAM-017.
- Repositories, packages and Maven coordinates NAM-020 to NAM-023.
- Paths NAM-030 to NAM-034, fields NAM-040 to NAM-043 and events NAM-050 to NAM-052.
- Code lists NAM-060 and NAM-061, and files NAM-070 and NAM-071.
- Stability NAM-080 to NAM-084.
- Comparison with the international baseline and Canada.
- An explanation guide and a how-to guide in each language.
