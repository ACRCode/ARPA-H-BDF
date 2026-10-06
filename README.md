# Federated Biomedical Computation Reference Architecture
 
> This project provides both a **contract-driven reference architecture for federated biomedical computation** and a set of **open-source reference components** that demonstrate key parts of that architecture.
---
## Overview
The architecture defines the roles, boundaries, and contracts needed for discovering biomedical data and coordinating computational workflows across distributed organizations. The open-source components provide reusable libraries and tools that organizations can adopt, extend, replace, or use as examples when building systems that conform to this architectural pattern.
 
In this architectural pattern, participating sites retain source imaging and clinical data within their governed environments while a central service defines federated jobs, coordinates site-level execution, monitors progress, and receives authorized results.
 
Interoperability is established through **shared, versioned contracts** for metadata, jobs, status, results, errors, and algorithm packages—not through dependence on a particular product, repository, runtime, or technology stack.
 
## Repository Components
 
The repository and associated public assets include:
 
- **DICOM Metadata Index Creator** — reads DICOM files and produces JSON metadata conforming to the ARPA-H Biomedical Data Fabric metadata specification.
 
- **BDF Metadata Index and Examples** — publishes the BDF index definition with example clinical, imaging-study, and image-series submissions to illustrate the metadata structure and support implementation and validation.
 
- **Metadata Index Ingestion Pipeline** — parses a conformant JSON index and prepares records for a searchable JSON repository such as Elasticsearch or MongoDB.
 
- **Federated Orchestration Core** — provides representative central business logic for federated job creation, generation of site-specific work, status tracking, and result receipt.
 
- **Federated Job Contracts** — defines the shared data structures exchanged between central orchestration and local site orchestration.
 
- **Federated Site Agent** — demonstrates job polling or retrieval, local execution initiation, status updates, and final payload return.
 
- **Radiology Report De-identification Utility** — provides an optional local privacy transformation for CSV, XLSX, and JSON report inputs, with container and Windows executable packaging.
 
## Architectural Approach
 
The architectural pattern separates **central coordination** from **site-level data access and execution**. Participating organizations retain control over local data, workload authorization, execution policies, and permitted outputs.
 
Contract boundaries allow central and local components to evolve independently while preserving interoperability.
 
**ACR Connect, ACR AI-LAB, and ACR DART** are presented as illustrative implementations showing how the architecture pattern and open-source libraries can be assembled into an end-to-end production workflow. These platforms and particular tools are **not required for conformance**.
 
The ACR platforms utilized to demonstrate the architecture may incorporate both open-source and proprietary components but are not themselves represented as open-source platforms. **All of the components that were created under this project are provided as open-source code and materials.**
 
Organizations may adopt the architecture by:
 
- Reusing one or more reference components

- Extending the components with local adapters or services

- Replacing components with conformant alternatives

- Implementing the architecture independently using the defined roles and contracts
 
---
 
*This work was supported in part by The Medical Imaging and Data Resource Center (MIDRC), funded by the National Institute of Biomedical Imaging and Bioengineering (NIBIB) of the National Institutes of Health and through the Advanced Research Projects Agency for Health (ARPA-H).*
 
 
