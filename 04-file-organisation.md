---
title: 'File Organisation'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What makes a folder structure and file naming scheme effective?
- How do you balance human-readability with machine-parsability?
- When should you rename original data files (and when should you avoid it)?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Define principles for organising project folders and naming files.
- Create a simple, reproducible file naming convention for a sample project.
- Identify strategies for linking filenames to metadata and preserving originals.

::::::::::::::::::::::::::::::::::::::::::::::::

## File Organisation

One of the most essential aspects of data management is organising your data. This includes naming, folder structure and documenting relationships between files. Before you start collecting or processing data, decide how you will structure and name files and folders so that team members can follow a standard approach.

Document your file directory structure and describe the kinds of records that should be maintained in those folders.

### Organised Folder Structure

- Keep a consistent top-level layout for projects (for example: data_raw, data_processed, code, docs, results, notebooks).
- Separate raw data (never modified) from processed data and analysis outputs.
- Include README files in key folders to explain contents and conventions.

Reference: http://nikola.me/folder_structure.html

### File Naming Convention

A file naming convention is a framework for naming your files so filenames convey what a file contains and how it relates to others. Good names let you scan directories and understand contents without opening files.

Guidelines:

- Identify 3–5 key metadata elements to encode in filenames (e.g. date, project, sampleID, experiment, replicate).
- Use consistent delimiters (underscores `_` or hyphens `-`) and avoid spaces and punctuation.
- Keep names as short as practical while remaining informative.
- Use ISO 8601 dates (YYYY-MM-DD) when including dates.
- Left-pad numbers (e.g. 01, 02) to ensure correct lexical sorting.

XKCD on file names (https://xkcd.com/1459/), Jennifer Bryan’s guidance on naming.

### Three Principles of Naming Files

1) Machine readable
- Avoid spaces, non-ASCII characters, and punctuation that can be interpreted by shells.
- Use delimiters to make parsing simple via regular expressions or simple split operations.

2) Human readable
- Ensure filenames contain meaningful content descriptors so humans can infer purpose quickly.

3) Plays well with default ordering
- Put sortable elements (date or numeric sequence) near the start of the name.

### Examples

Good:

- 2024-01-30_anemone-filtered_stats.csv
- 01_experimentA_sampleA_rep01.fastq.gz

Bad:

- My-arbitrary filename has punctuation&spaces.xls

### Sequencing and Version Control

- Preserve original instrument or sequencing files untouched in a raw folder.
- If re-sequencing or reprocessing, add explicit versioning (e.g. _v01, _v02) or sequencing suffixes (_001, _002).
- Avoid renaming original files unless absolutely necessary; if you must, keep an audit table that maps original names to new names.

### Metadata Linkage

- Ensure filenames link clearly to metadata records: include a unique sample identifier used both in the filename and in a metadata table.
- Maintain a separate column in metadata spreadsheets with the precise filename for each sample.
- Lock or protect final metadata spreadsheets to prevent accidental overwrites; keep a controlled edit history.

::::::::::::::::::::::::::::::::::::: keypoints 

- Choose a concise, consistent naming scheme and document it in a project README.
- Use ISO dates and zero-padded numbers for reliable sorting.
- Keep raw and processed data in separate folders and never overwrite raw files.
- Link filenames to metadata via a shared unique identifier.
- Document any renaming actions and use versioning for processed outputs.

::::::::::::::::::::::::::::::::::::::::::::::::
