---
title: 'Data analysis and computing'
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- Where should different types of computations be run (local laptop, HPC, cloud)?
- What factors determine whether to use HPC, cloud or local machines?
- How can you make analyses reproducible across computing environments?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Compare computing environments and identify suitable use-cases for each.
- Explain batch job management basics and the role of resource requests.
- Describe reproducibility practices (containers, environment specs, code versioning).

::::::::::::::::::::::::::::::::::::::::::::::::

## Data Analysis

Data analysis requires choices about where computations run, where data are stored, and how data are transferred. Clear decisions improve reproducibility and reduce interruptions in workflows.

## Where to run your computations

Key considerations when choosing an environment:

- Data size: small datasets may be analysed locally; very large datasets often require HPC or cloud.
- CPU and memory requirements: large memory or many cores may need specialised nodes.
- Software dependencies: containerised environments or managed cloud images help maintain consistent software stacks.
- Cost and access: cloud resources incur costs; HPC access may be limited by allocations or institutional rules.
- Data locality: running analyses close to where data are stored reduces transfer overhead.

## Large-scale computing in bioinformatics

Some analyses are resource intensive due to:

- Very large raw data (for example whole genome sequencing).
- Computational complexity (for example molecular dynamics).
- High-throughput workflows across many samples (for example population genomics).
- High RAM requirements (for example de novo assembly).

## Supercomputing, HPC and campus resources

- Supercomputing centres (national) provide very large-scale resources and often operate merit-based access.
- HPC clusters (including campus clusters) are suitable for many research workflows and often provide special file systems and batch schedulers (for example SLURM).
- Local or university cloud resources offer flexible VM-based compute that can be sized to tasks.

## Batch job management

Batch systems queue and schedule jobs. Typical workflow:
- Create a job script that requests resources (cores, memory, walltime).
- Submit to the scheduler (for example SLURM).
- Monitor job status and retrieve outputs from job-specific working directories.

Always request resources conservatively and test with small jobs before scaling up.

## Reproducibility and environments

- Containerisation (Docker, Singularity/Apptainer) packages software and dependencies for reproducible execution.
- Capture environment specifications (for example `renv` for R, `requirements.txt` or `conda` environments for Python).
- Version-control analysis code (Git) and tag releases corresponding to manuscript results.

## Cloud computing

Clouds provide on-demand, scalable resources:

* Useful for bursty workloads, large-scale parallel jobs or when you need specialised hardware (for example GPUs).
* Consider cost management (spot instances, appropriate sizing) and data egress charges.

## Galaxy

Galaxy is a web-based platform that enables many bioinformatics analyses without command-line experience.

* Useful for reproducible, shareable workflows and training.

::::::::::::::::::::::::::::::::::::: keypoints 

- Choose compute based on data size, memory/CPU needs, software dependencies and cost.
- Use containers and environment specifications to ensure reproducibility.
- Test workflows on small data or with reduced resource requests before full runs.
- Use batch systems correctly: request resources, monitor jobs and preserve logs and outputs.
- Document where and how analyses were run in project metadata or README files.

::::::::::::::::::::::::::::::::::::::::::::::::
