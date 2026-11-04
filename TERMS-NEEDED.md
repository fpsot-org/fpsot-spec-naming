# Terms needed

Entries that this specification uses and that the writing term base does not hold yet.
They use the format of `termbase/terms.yaml` in fpsot-spec-writing, and go into that file before the release.

```yaml
  - id: ascii
    kind: abbreviation
    en: {short: "ASCII", full: "American Standard Code for Information Interchange", definition: "A 7-bit character code for the letters, digits and signs of English text."}
    fr: {short: "ASCII", full: "code ASCII (American Standard Code for Information Interchange)", definition: "Code de caractères sur 7 bits pour les lettres, les chiffres et les signes de l'anglais."}
    source: {name: "Grand dictionnaire terminologique", url: "https://vitrinelinguistique.oqlf.gouv.qc.ca/fiche-gdt/fiche/8358861/code-ascii", checked: "2026-11-04"}
  - id: http
    kind: abbreviation
    en: {short: "HTTP", full: "Hypertext Transfer Protocol", definition: "The protocol that web clients and servers use to exchange documents and data."}
    fr: {short: "HTTP", full: "protocole de transfert hypertexte", definition: "Protocole que les clients et les serveurs Web emploient pour échanger des documents et des données."}
    source: {name: "Grand dictionnaire terminologique", url: "https://vitrinelinguistique.oqlf.gouv.qc.ca/fiche-gdt/fiche/2075739/protocole-http", checked: "2026-11-04"}
  - id: json
    kind: abbreviation
    en: {short: "JSON", full: "JavaScript Object Notation", definition: "A text format for structured data, made of objects, arrays, strings, numbers, booleans and null."}
    fr: {short: "JSON", full: "JavaScript Object Notation", definition: "Format texte pour les données structurées, fait d'objets, de tableaux, de chaînes, de nombres, de booléens et de la valeur null."}
    source: {name: "RFC 8259", url: "https://www.rfc-editor.org/rfc/rfc8259", checked: "2026-11-04"}
  - id: uri
    kind: abbreviation
    en: {short: "URI", full: "uniform resource identifier", definition: "A standard character string that names a resource by its location or by its name."}
    fr: {short: "URI", full: "adresse URI (uniform resource identifier)", definition: "Chaîne de caractères normalisée qui désigne une ressource par son emplacement ou par son nom."}
    source: {name: "Grand dictionnaire terminologique", url: "https://vitrinelinguistique.oqlf.gouv.qc.ca/fiche-gdt/fiche/26520166/adresse-uri", checked: "2026-11-04"}
```

Notes for the review of the French terms:

- `json`: the Grand dictionnaire terminologique has no record for JSON. The French full form keeps the English name of the format, as the term base does for BCP and CLDR. The source is the IETF standard that defines the format.
- `uri`: the record prefers "adresse URI", "identifiant URI" and "URI". The full form follows the pattern of the existing `url` entry.
- `http`: the record prefers "protocole HTTP" and "protocole de transfert hypertexte".
- `ascii`: the record prefers "code ASCII". It glosses the English name as "Code américain normalisé pour l'échange d'information", which is not a term.
