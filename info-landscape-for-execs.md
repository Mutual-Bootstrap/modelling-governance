# Information Landscape Views for Executive Audiences

## Purpose

To capture durable principles and patterns for creating executive-level information landscape views from imperfect architecture repositories.

This document describes how to present systems, information and organisational responsibilities in a way that supports understanding and decision-making, even when underlying repository data is incomplete, inconsistent or modelled at different levels of abstraction.

---

## Context

Enterprise repositories often contain:

- Multiple generations of models.
- Mixed modelling styles.
- Partial relationship coverage.
- Inconsistent capability hierarchies.
- Strong system information but weak usage information.

Executives rarely require complete architectural fidelity. More commonly, they need to understand:

- Which systems are important.
- Which organisational areas depend on them.
- What information they contain.
- Where responsibilities overlap.
- Where fragmentation exists.

The challenge is therefore not merely repository extraction but translation of architectural content into a form appropriate for strategic decision-making.

---

## Key Concepts

### Information Landscape

A representation of:

- organisational actors or communities;
- information domains;
- systems and repositories;

and the relationships between them.

The purpose is understanding and governance rather than technical design.

---

### Information Domain

A logical grouping of information that represents a coherent business concern.

Information domains should remain stable even when systems change.

Examples include:

- Design & Engineering Information
- Commercial & Contract Information
- Planning & Controls Information
- Requirements & Integration Information
- Assurance & Governance Information
- Permissions & Environmental Information

---

### Information Community

A grouping of stakeholders who create, manage or consume information.

Information communities should align with organisational structures familiar to the intended audience.

Examples include:

- Commercial
- Programme Management
- Engineering & Design
- Technical Assurance & Quality

---

### Information Platform

A system that provides storage, workflow, collaboration, governance or reporting capabilities.

An information platform may support multiple information domains and multiple communities simultaneously.

---

### Information Hub

A platform used by multiple communities and supporting multiple information domains.

Information hubs are often more significant than specialist systems because they represent operational integration points.

---

## Relationships

### Community → Information Domain

Communities create, consume or govern information domains.

Examples:

- Commercial → Commercial & Contract Information
- Engineering & Design → Design & Engineering Information
- Programme Management → Planning & Controls Information

---

### Information Domain → Platform

Information domains are managed using one or more platforms.

Examples:

- Commercial & Contract Information → Contract Management Platform
- Design & Engineering Information → Design Collaboration Platform
- Planning & Controls Information → Scheduling, Cost and Risk Platforms

---

### Community → Platform

Communities operate within platforms as part of their daily work.

The relationship demonstrates dependency rather than ownership.

---

### Platform ↔ Platform

Information domains frequently span multiple platforms.

The presence of the same information domain in multiple systems is not necessarily duplication; it may indicate lifecycle progression, collaboration requirements or federated management.

---

### Platform → Information Hub

Some platforms emerge as hubs due to breadth of use.

Indicators include:

- multiple communities;
- multiple information domains;
- cross-functional workflows;
- programme-wide visibility.

---

## Architecture Implications

### Model Information Separately from Systems

Information domains should not be derived solely from application names.

Systems change faster than information.

Information models provide greater long-term stability.

---

### Use Audience Language

Executive-facing views should prioritise terminology familiar to the audience.

Capability names, organisational structures and responsibility boundaries often provide more recognisable labels than formal architecture constructs.

---

### Prefer Information Domains to Data Objects

Large collections of individual artefacts rapidly become unreadable.

Grouping into information domains provides a more durable and understandable representation.

---

### Focus on Relationships

Executive information views derive value from showing connections.

Useful questions include:

- Who uses this system?
- What information does it contain?
- What organisational areas depend on it?
- Where does information cross boundaries?

Inventories alone rarely provide sufficient insight.

---

### Information Hubs Merit Special Attention

Platforms supporting many information communities create systemic dependencies.

They may require:

- enhanced governance;
- availability controls;
- data quality monitoring;
- architectural oversight.

---

### Repository Extraction Requires Interpretation

Architecture repositories seldom contain every relationship required for executive reporting.

Translation, grouping and normalisation are expected activities rather than modelling failures.

---

## Risks and Limitations

### Over-Reliance on Repository Structure

Capability hierarchies, application mappings and ownership structures frequently reflect modelling conventions rather than operational reality.

Repository outputs should be validated against organisational understanding.

---

### Taxonomy Drift

Different models often use different capability structures.

Views anchored directly to repository taxonomies may become unstable over time.

Stable information domains reduce this risk.

---

### Inventory Bias

Architects frequently produce lists of systems rather than views of relationships.

This creates diagrams that are technically accurate but strategically unhelpful.

---

### Over-Classification

Too many categories reduce comprehension.

Executive audiences typically benefit from five to seven major information groupings.

---

### False Precision

Incomplete repositories
