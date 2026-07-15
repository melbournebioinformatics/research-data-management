---
title: 'Standardised language'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are ontologies and controlled vocabularies, and how do they help data interoperability?
- When should you adopt existing standards rather than invent your own terms?
- How should you capture dates and missing values in metadata?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Define ontologies, taxonomies, and controlled vocabularies and explain their purpose.
- Identify common resources (examples) and when to apply them to domain data.
- Apply best practices for dates, missing values and sample aliasing in metadata.

::::::::::::::::::::::::::::::::::::::::::::::::

## Ontologies and standardised language

Ontologies and controlled vocabularies define and categorise classes of entities and the relationships between them. Using standardised language makes data interoperable, eases automation, and improves discoverability.

Examples:

- Taxonomies for organisms (taxonomy IDs).
- Enzyme Commission (EC) numbers for enzymatic activities.
- Gene Ontology (GO) terms for molecular function, biological process and cellular component.

Standardised language facilitates data mining, integration between datasets and reuse across tools.

## Importance of standardised language

When fields use the same controlled terms and IDs, datasets can be joined reliably and processed by pipelines that expect those terms. Communities and repositories often recommend or require particular vocabularies; use community standards where available rather than inventing new labels.

Reference: GeneCards and similar resources provide centralised gene identifiers and annotations.

## Metadata Dates

Dates must be unambiguous. For example, 04/03/2024 can be read as 4 March or 3 April depending on locale. Use:

- ISO 8601: YYYY-MM-DD (preferred for filenames and metadata).
- Or explicit formats like 04-Mar-2024 when readability matters.

Record in dataset headers which date format you are using.

## Metadata pointers

- Include a field for sample aliases and track any synonyms or previous IDs with a consistent separator (for example `;` or `,`).
- Avoid single-letter codes when descriptive labels are feasible.
- Use meaningful column headings and indicate units (for example `Height_m` or `Concentration_mg_per_L`).

## More metadata pointers

- Be explicit about missing data — avoid blank cells. Use a consistent token such as `NA`, `None`, or `Null`, and document the chosen token in your metadata README.
- Link filenames to metadata sample names by including a `filename` column in your metadata table.
- Once a spreadsheet is finalised, lock or freeze it to control writes and record who made changes.
- Avoid using non-standard markers (for example emoticons) to indicate values like "Yes" — use explicit textual or coded values.

## Deposit data in a public repository?

Plan ahead: collect required metadata from the start to meet repository and journal requirements. Some repositories mandate specific fields and formats (for example accession numbers, licences, or structured dates).

Think about keywords and tags (organism, study type, instrument) to improve searchability.



::::::::::::::::::::::::::::::::::::: keypoints 

- Use community ontologies and controlled vocabularies where possible to improve interoperability.
- Always document formats (especially dates) and tokens used for missing data.
- Keep a column mapping sample identifiers to filenames to avoid ambiguity.
- Collect repository-required metadata early to avoid rework at deposit time.

::::::::::::::::::::::::::::::::::::::::::::::::
