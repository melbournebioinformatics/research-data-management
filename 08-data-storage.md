---
title: 'Data Storage'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- Where should you store data during active analysis versus for long-term preservation?
- What are the pros and cons of institutional versus commercial storage services?
- How should sensitive data be stored and shared securely?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Compare storage options for short-term (compute-attached) and long-term (archive) needs.
- Describe backup, encryption and access-control strategies for research data.
- Identify institutional services and best-practice selection criteria.

::::::::::::::::::::::::::::::::::::::::::::::::

## Where to store your data

Choosing storage depends on access patterns, performance needs and retention requirements. Consider an integrated approach:

- Fast, compute-attached storage for active analyses.
- Durable, backed-up storage for long-term preservation.
- Secure storage with controlled access for sensitive data.

## Compute-attached storage

- Usually local to HPC or cloud compute nodes; optimised for performance and short-term use.
- Examples: distributed parallel filesystems (Lustre, GPFS) on HPC and local instance storage on cloud VMs.
- Typically not backed up indefinitely and may be tied to project duration.

## Data home (longer-term)

When not actively analysing data, store it in locations with:

- Regular backups and redundancy.
- Access controls and auditability.
- Reasonable cost and long lifespan.
- Clear documentation and discoverability.

Avoid relying solely on single external hard drives — hardware fails.

## Institutional storage options (examples)

- University-managed services (for example OneDrive for students, research data services such as Mediaflux, DaRIS, institutional figshare, object storage).
- Institutional repositories often integrate with identity management and provide retention policies.

Note: Check access and retention terms (for example student OneDrive quotas and deletion policies upon leaving the institution).

## Commercial and archival options

- Commercial cold storage (for example Glacier-style services) can be cost-effective for long-term archiving.
- Zenodo and other community repositories provide minting of DOIs for datasets and are suitable for publication-level deposits.

## Backup strategies and encryption

- Follow the 3-2-1 rule: at least three copies of your data, on two different media, with one copy off-site.
- Use checksums to verify integrity after transfers and during backups.
- Encrypt sensitive data at rest and in transit; manage keys or access through institutional identity systems where possible.

## Data retention and access

- Define retention periods that match funder, legal and institutional requirements.
- Document who can access which datasets and how access requests are handled.
- Keep a lifecycle plan for when data should be archived, deleted or migrated.

::::::::::::::::::::::::::::::::::::: keypoints 

- Use compute-attached storage for active work, but plan for migration to institutional or archival storage for preservation.
- Implement regular backups and keep at least one off-site copy.
- Encrypt sensitive data and manage access control explicitly.
- Choose institutional repositories when possible for long-term stability and DOI assignment.
- Document storage locations, retention policies and responsible contacts in project metadata.

::::::::::::::::::::::::::::::::::::::::::::::::
