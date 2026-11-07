---
name: fpsot-naming
description: Naming rules for identifiers that machines read in FPSOT projects. Use when naming a repository, a Java or Kotlin package, Maven coordinates, a URL path, a JSON field or query parameter, an event type, a code list value, or a file in a specification repository.
---

# FPSOT naming

Summary of the FPSOT naming specification. It adds no rules of its own.
The spec text in `spec/` wins on any difference. Each line cites its requirement ID and keeps its strength: must, should or may.

## Every name

- Names must be in English. People see translated labels, never the name (NAM-001).
- Names must use the English term of the writing term base, in the case style of the context (NAM-002). One concept must have one name (NAM-003).
- Names must use only ASCII letters, digits and the separator of the case style, and must start with a letter (NAM-004).
- Names must not shorten words. They may use term base abbreviations and `id` (NAM-005).
- Names must use US spelling, such as `license` and `color` (NAM-006). Names from outside standards must keep their exact form, such as `CAD` or the HTTP header field `Referer` (NAM-007).
- Names should not be reserved words such as `class` or `default` (NAM-008). Names must have at most 63 characters, and should have 4 words or fewer (NAM-009).

## Case and word form

- Case style must follow the context. lowerCamelCase: JSON fields, query parameters, path variables. kebab-case: path segments, code values, event type segments, artifactIds, repositories, files, design token path segments (NAM-010).
- Abbreviations must be ordinary words: `apiKey`, `userId` (NAM-011). No word may start with a digit, except the numeric scale step of a design token path, such as `color.blue.50` (NAM-012).
- Lists and collections must be plural, one item must be singular (NAM-013). Field names and path segments should be nouns, not verbs (NAM-014).
- Booleans should drop `is` or `has` (NAM-015). Names should not contain prepositions, except the suffixes `At`, and `From` and `To` for range filters, such as `createdAtFrom` (NAM-016).
- Tools must compare names with case. Two names must not differ only by case or separators (NAM-017).

## Repositories and packages

- Repositories must be `fpsot-<kind>-<topic>`, kind `spec`, `library`, `service`, `tool` or `website` (NAM-020).
- Packages must be `org.fpsot.<topic>`, words joined, lower case, no underscores (NAM-021). The module name should be the main package (NAM-022).
- Maven: `groupId` must be `org.fpsot.<topic>`, `artifactId` must be `fpsot-…` in kebab-case (NAM-023).

## Paths, fields, events, code lists, files

- Path segments must be kebab-case, collections plural (NAM-030). Path variables must be lowerCamelCase, and should be named like the referring field (NAM-031).
- Paths must not hold a file extension, software name, person's name or status (NAM-032). Paths must identify by an opaque identifier, not by name (NAM-033).
- Language versions must share path segments; a language tag segment may mark the language (NAM-034).
- The own identifier must be `id`, references `<resource>Id`, lists `<resource>Ids` (NAM-040). Instants should end with `At`, dates with `Date`. A name that another FPSOT specification fixes in a shared type, such as `start` and `end` of an interval, keeps that name (NAM-041).
- Every field must be declared. Keys must not come from data, but may be language tags or declared code values (NAM-042). Field names should not repeat the parent name (NAM-043).
- Event types must be `org.fpsot.<domain>.<resource>.<event>`, with a singular resource and a past-tense event (NAM-050, NAM-051). Extension attributes must use lower-case letters and digits, 20 characters at most (NAM-052).
- Code values must be kebab-case English strings, never numbers. Codes from another issuer, such as `CAD` or `CA`, must keep the issuer's form (NAM-060, NAM-007). Each value must have an English and a French label (NAM-061).
- Files must be kebab-case English, with the same name in every language folder (NAM-070). Diagram output must share the base name of its source (NAM-071).

## Stability

- A published name must not change or disappear within a major version (NAM-080). Minor versions may add names, and growing code lists must say so (NAM-081).
- A removed name must not come back with a new meaning (NAM-082). Published page addresses must keep working or redirect permanently (NAM-083).
- Projects should not rename repositories. An old name must not go to another project (NAM-084).
