---
title: 'Data Transfer'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are common methods to transfer large datasets between systems?
- How do you ensure data integrity and security during transfer?
- When is a synchronisation tool preferred over simple copy commands?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Describe common file transfer protocols and tools and their use-cases.
- Demonstrate strategies to resume interrupted transfers and to verify integrity.
- Recommend secure transfer practices for sensitive data.

::::::::::::::::::::::::::::::::::::::::::::::::

## How to transfer your data

Data transfer between systems must account for size, bandwidth, reliability, endpoints and cost. Choose tools that match those constraints.

## Data transfer considerations

- Size: very large datasets may be best transferred via specialised services or physical shipment of storage (when permitted).
- Bandwidth & reliability: unreliable networks require resumable transfers or synchronisation tools.
- Endpoints: ensure both ends support the same protocols and authentication methods.
- Cost: data egress charges can influence whether cloud-to-cloud or local transfers are appropriate.

## File transfer protocols

- SCP (Secure Copy Protocol): simple, secure for many use cases and scriptable for small-to-moderate transfers.
- FTP/FTPS: legacy; FTPS adds TLS but FTP lacks modern security defaults.
- HTTP/HTTPS: useful for downloads or APIs; may not be ideal for bulk transfers.
- Rsync: excellent for synchronisation and resuming interrupted transfers; supports delta transfers to reduce bandwidth.
- Globus: designed for reliable, high-performance transfers between research endpoints (where available).

## Data mirroring and synchronisation

- Use rsync with the `-P` flag to get progress and resume capability for interrupted transfers.
- For two-way synchronisation across independent copies, consider Unison or dedicated synchronisation services.
- Maintain an audit trail for what was transferred, by whom and when.

## Data integrity

- Use cryptographic hashes (for example MD5, SHA-256) to fingerprint files and verify integrity after transfer.
- Store checksums alongside files and validate them after transit and on archival storage.
- For very large archives, consider manifest files that list filenames, sizes and checksums.

## Security

- Use secure protocols (SCP, SFTP, HTTPS) rather than unauthenticated FTP.
- Encrypt sensitive data prior to transfer if endpoints do not provide end-to-end encryption.
- Use institutional authentication (SSH keys, federated logins) and least-privilege access.

::::::::::::::::::::::::::::::::::::: keypoints 

- Choose rsync or Globus for large or unreliable transfers; use SCP for simple secure copies.
- Always verify transfers with checksums (MD5 or SHA-256); keep manifests for auditability.
- Prefer encrypted and authenticated transfer methods for sensitive data.
- Automate recurring transfers with scripts and logging to reduce human error.
- Consider cost and data egress when transferring between cloud providers.

::::::::::::::::::::::::::::::::::::::::::::::::
