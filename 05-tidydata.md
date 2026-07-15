---
title: 'Tidy data'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are the principal rules of tidy data and why do they matter?
- How do messy data patterns (wide tables, headers as values) impede analysis?
- What are common Excel behaviours that cause reproducibility problems?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- State Hadley Wickham’s four tidy data rules and apply them to example datasets.
- Identify common messy layouts and describe how to tidy them.
- Recognise Excel pitfalls and outline safeguards to prevent data corruption.

::::::::::::::::::::::::::::::::::::::::::::::::



"Happy families are all alike; every unhappy family is unhappy in its own way." — Leo Tolstoy  
"Tidy datasets are all alike, but every messy dataset is messy in its own way." — Hadley Wickham

## Tidy data

A substantial portion of data analysis time is spent cleaning and preparing data. Applying consistent organisation conventions reduces repeated work and makes downstream analysis, modelling and visualisation straightforward.

## Tidy Data in a nutshell

Tidy data provide a standard way to organise values within a dataset so tools can work predictably.

Reference: https://vita.had.co.nz/papers/tidy-data.pdf

## Tidy data rules

1) Every row is an observation (or case).  
2) Every column is a variable (or attribute).  
3) Every cell contains a single value.  
4) Each type of observational unit forms a table.

## Examples

Tidy example:

| Name | Age | Height_m | Eye_Colour |
|------|-----|----------|------------|
| John | 34  | 1.78     | Blue       |
| Joe  | 29  | 1.82     | Brown      |
| Mary | 45  | 1.65     | Other      |


Messy example:

- Columns named Blue, Brown, Other with 1/0 entries for eye colour (these headers are values, not variables).
- Height in a column without units; leading zeroes lost in sample IDs; merged cells used for titles.

## Excel pitfalls

Excel can be "helpful" in ways that corrupt scientific data:

- Automatic type conversion (e.g. gene symbols to dates, or long numeric identifiers to scientific notation).
- Dropping leading zeros in sample IDs.
- Removing trailing zeroes in decimal data.
- Merging cells or using colour/highlighting instead of an explicit column value.

Practical safeguards:

- Store identifiers as text (e.g. prefix with single quote or specify column type when importing).
- Use underscores `_` instead of spaces in sample names.
- Add explicit columns for status or comments rather than highlight cells.
- Export and store tabular data as plain text (CSV or TSV) with well-documented column names.

## Common "shenanigans" explained

- Gene identifiers like "2310009E13" may be interpreted by Excel as scientific notation (2.310009E+19) — leading to irreversible changes.
- Symbols such as "DEC1" or "OCT4" can be auto-interpreted as dates (December 1, October 4) in some locales.

## Practical exercise suggestions

- Present a messy spreadsheet and convert it to tidy format using a scripting language (R or Python) or a reproducible sequence of steps.
- Inspect a sample metadata table for inconsistent date formats and normalise to ISO 8601.

::::::::::::::::::::::::::::::::::::: keypoints 

- Tidy data principles enable predictable and reusable analysis workflows.
- Avoid manual spreadsheet operations that are hard to reproduce; script data cleaning where possible.
- Protect against Excel automatic conversions by setting column types and using plain-text exports.
- Keep units and variable descriptions explicit in column headings or a metadata file.

::::::::::::::::::::::::::::::::::::::::::::::::
