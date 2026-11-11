# Changelog

All notable changes to this specification are listed here.
The format follows [Keep a Changelog 1.1.0](https://keepachangelog.com/en/1.1.0/),
and versions follow [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.5.0] - 2026-11-11

### Added

- NAM-053: a product should use an attribute of the OpenTelemetry semantic conventions 1.45.0 when one has the meaning it needs, and may define its own when that attribute is not Stable.
- NAM-054: a telemetry attribute that the project defines starts with `org.fpsot.`. An attribute of another organization, such as an agency, starts with that organization's reversed domain name. No new name starts with a namespace of the conventions.
- NAM-055: after its prefix, a telemetry attribute name has segments joined by dots, each in snake_case, with a dot between an object and its property.
- NAM-056: each segment meets the character, abbreviation, spelling, length and case rules as one name, and the last segment follows the word form rules.
- NAM-057: the identifier of an object is the segment `id`, and an attribute that carries a field keeps the words of that field.
- NAM-058: a published telemetry attribute name does not change or disappear within a major version.

### Changed

- NAM-010 now gives the case style of a telemetry attribute name: snake_case segments joined by dots.
- NAM-080 now names telemetry attributes among the published names it covers.
- The events page has sections for event types, extension attributes and telemetry attributes.
- The skill lists telemetry attributes under NAM-010 and NAM-053 to NAM-058.

## [0.4.0] - 2026-11-08

### Added

- NAM-072: a Gherkin feature file in any repository has a kebab-case English name ending in `.feature`, the same in English and French.

### Changed

- NAM-010 now gives the case style of Gherkin tags (kebab-case after the `@`) and of Gherkin feature file names.
- The skill lists Gherkin tags and feature files under NAM-010 and NAM-072.

## [0.3.0] - 2026-11-07

### Changed

- NAM-020: the repository kinds `psc` (Public Sector Capability) and `template` are added.
- NAM-010 now gives the case style of a design token path: kebab-case segments joined by dots, as in the W3C Design Tokens format.
- NAM-012 now lets the scale step of a design token path be a numeric segment, as in `color.blue.50`.
- The skill lists design token paths under NAM-010 and NAM-012.

### Fixed

- The reference to the Maven naming guide is now not dated, because the page shows only the site's daily publishing stamp.

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
