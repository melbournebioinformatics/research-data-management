---
title: 'The Data Lifecycle'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are the main stages of the research data lifecycle?
- At which lifecycle stages should you plan metadata, storage and sharing?
- How does lifecycle thinking improve reproducibility and data stewardship?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Describe the typical stages of the research data lifecycle.
- Identify decisions to make at each stage (planning, collecting, processing, preserving, sharing).
- Create a simple checklist to guide RDM activities across the lifecycle.

::::::::::::::::::::::::::::::::::::::::::::::::

## Research Data Lifecycle

The research data lifecycle is a conceptual model that describes how research data are created, processed, used, stored and preserved. Thinking in terms of a lifecycle helps you plan for reproducible, secure and shareable data from the start.

Typical lifecycle stages:
- Plan: Define data types, formats, storage, metadata, ethical and legal constraints, and assign responsibilities. Create a data management plan (DMP).
- Collect / Acquire: Capture data with standardised procedures, record provenance, and collect metadata contemporaneously.
- Process / Analyse: Clean and transform data, log processing steps, use version control for code and scripts, and store intermediate and final outputs with clear names.
- Preserve: Choose a repository or archival storage for long-term preservation; include metadata, licences and persistent identifiers.
- Share / Publish: Deposit data and code in appropriate repositories, document how others can access and reuse your resources.
- Reuse / Repurpose: Facilitate reuse by offering clear documentation and machine-readable metadata.

Practical tips:
- Integrate metadata capture into the data collection workflow to avoid loss of context.
- Keep raw (unchanged) copies of primary data; perform analyses on copies with explicit versioning.
- Ensure backup strategies are in place throughout the lifecycle; iterative backups reduce risk.
- Use automation where possible (scripts, pipelines) to capture reproducible processing steps.


![Reference: LMA Research Data Management Working Group and related RDM lifecycle diagrams illustrate how different roles and systems interact across these stages https://datamanagement.hms.harvard.edu/plan-design/biomedical-data-lifecycle](fig/RDM-lifecycle-2tier-v5.png)



::::::::::::::::::::::::::::::::::::: keypoints 

- Plan first: a clear plan reduces risk and streamlines later stages.
- Capture metadata early and often — context gets lost quickly.
- Preserve raw data and version analysed outputs and code.
- Use repositories and persistent identifiers to enable discoverability and reuse.
- Lifecycle thinking helps allocate responsibility and resources across a project.

::::::::::::::::::::::::::::::::::::::::::::::::
