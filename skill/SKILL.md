---
name: fpsot-naming
description: Naming rules for identifiers that machines read in FPSOT projects. Use when naming a repository, a Java or Kotlin package, Maven coordinates, a URL path, a JSON field or query parameter, an event type, a code list value, or a file in a specification repository.
---

# FPSOT naming

Summary of the FPSOT naming specification. It adds no rules of its own.
The spec text in `spec/` wins on any difference. Each line cites its requirement ID.

## Every name

- Names are in English. People see translated labels, never the name (NAM-001).
- Use the English term of the writing term base, in the case style of the context (NAM-002). One concept, one name (NAM-003).
- Only ASCII letters, digits and the separator of the case style. Start with a letter (NAM-004).
- No shortened words. Only term base abbreviations and `id` (NAM-005).
- Canadian spelling, such as `licence` and `colour` (NAM-006). Names from outside standards keep their exact form, such as `CAD` or `license` in `publiccode.yml` (NAM-007).
- Avoid reserved words such as `class` or `default` (NAM-008). At most 63 characters, ideally 4 words or fewer (NAM-009).

## Case and word form

- lowerCamelCase: JSON fields, query parameters, path variables. kebab-case: path segments, code values, event type segments, artifactIds, repositories, files (NAM-010).
- Abbreviations are ordinary words: `apiKey`, `userId` (NAM-011). No word starts with a digit (NAM-012).
- Plural for lists and collections, singular for one item (NAM-013). Nouns, not verbs (NAM-014).
- Booleans without `is` or `has` (NAM-015). No prepositions, except the `At` suffix (NAM-016).
- Compare names with case. No two names that differ only by case or separators (NAM-017).

## Repositories and packages

- Repositories: `fpsot-<kind>-<topic>`, kind `spec`, `library`, `service`, `tool` or `website` (NAM-020).
- Packages: `org.fpsot.<topic>`, words joined, lower case, no underscores (NAM-021). Module name = main package (NAM-022).
- Maven: `groupId` `org.fpsot.<topic>`, `artifactId` `fpsot-…` in kebab-case (NAM-023).

## Paths, fields, events, code lists, files

- Path segments in kebab-case, collections plural (NAM-030). Path variables in lowerCamelCase, named like the referring field (NAM-031).
- No file extension, software name, person's name or status in a path (NAM-032). Identify by an opaque identifier, not by name (NAM-033).
- Language versions share path segments; a language tag segment may mark the language (NAM-034).
- Own identifier `id`, references `<resource>Id`, lists `<resource>Ids` (NAM-040). Instants end with `At`, dates with `Date` (NAM-041).
- Declare every field. No keys taken from data, except language tags or declared code values (NAM-042). Do not repeat the parent name (NAM-043).
- Event types: `org.fpsot.<domain>.<resource>.<event>`, singular resource, past-tense event (NAM-050, NAM-051). Extension attributes: lower-case letters and digits, 20 characters at most (NAM-052).
- Code values in kebab-case English, always strings, never numbers. Codes from another issuer, such as `CAD` or `CA`, keep the issuer's form (NAM-060). Each value has an English and a French label (NAM-061).
- Files in kebab-case English, same name in every language folder (NAM-070). Diagram output shares the base name of its source (NAM-071).

## Stability

- No published name changes or disappears within a major version (NAM-080). Minor versions may add names, and growing code lists say so (NAM-081).
- Never reuse a removed name with a new meaning (NAM-082). Published page addresses keep working or redirect permanently (NAM-083).
- Do not rename repositories, and never give an old name to another project (NAM-084).
