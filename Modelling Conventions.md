# Enterprise Architecture Modelling Conventions

## Purpose

These conventions establish a consistent approach to creating, naming and maintaining architecture models.

The purpose of these conventions is to improve:

- Consistency
- Discoverability
- Repository navigation
- Reporting
- Analysis
- Collaboration

Conventions are subordinate to the Modelling Principles. Where a convention conflicts with utility, simplicity or architectural value, the modeller should apply judgement and document the rationale.

---

# 1. Model Browser Structure

## Hierarchies

Where a meaningful hierarchical relationship exists, entities should be organised hierarchically within the repository.

Hierarchies should improve:

- Navigation
- Discoverability
- Reporting
- Understanding

Repository organisation should reflect architectural understanding rather than ownership or organisational structure.

---

# 2. Composition Preferred for Hierarchical Relationships

Composition should be the default relationship for representing hierarchy.

Aggregation may be used when the relationship is clearly optional and composition would be misleading.

Alternative relationships may be used where they create a more useful model and the rationale is documented.

### Preferred

```text
Capability A
    └── Capability B
```

represented through composition.

### Avoid

Using aggregation solely to avoid modelling hierarchy.

---

# 3. Capability Naming Convention

Capabilities should use a concise noun–verb form where practical.

The capability name should express:

```text
Something being done to Something
```

Examples:

✅ Requirements Management

✅ Service Management

✅ Asset Management

✅ Risk Assessment

✅ Design Assurance

Examples to avoid:

❌ Requirements

❌ Manage Requirements

❌ Managing Enterprise Requirements Throughout Delivery

Capability names should describe *what* the organisation is able to do, not *how* it does it.

---

# 4. Business and Technology Capability Naming

Where the same concept exists at both business and technology layers, naming should clearly distinguish between them.

Preferred approach:

```text
Identity Management
Identity Operations
```

or

```text
Security Management
Security Operations
```

Where this creates ambiguity, explicit tags may be used.

Example:

```text
Security [B]
Security [T]
```

If one capability is tagged, the corresponding capability must also be tagged.

---

# 5. Technology Products Belong in the Technology Layer

Commercial products and services should normally be modelled within the technology layer.

Examples:

✅ Microsoft 365

✅ Oracle Fusion

✅ Autodesk Construction Cloud

✅ Azure Active Directory

Application architecture should describe the service provided rather than the specific product selected.

### Preferred

```text
Application Service
      ↓
Technology Service
      ↓
Product
```

### Avoid

Embedding vendor-specific products directly into application architecture when a technology-agnostic service abstraction is practical.

---

# 6. Direct Relationships May Be Used When Valuable

Where ArchiMate permits a direct relationship between two entities, intermediate entities are not mandatory.

Additional elements should only be created when they provide architectural value.

Examples may include:

- Early-stage architecture
- SaaS implementations
- High-level strategic models
- Simple standalone solutions

Where a simplified relationship is used, rationale should be documented.

---

# 7. Model Change Explicitly

Architectural change should be represented using recognised roadmap and transition mechanisms.

Where states change over time, models should support:

- Current State
- Interim States
- Target State

Relevant roadmap properties and plateau relationships should be maintained to enable transition analysis.

---

# 8. Prefer Existing Relationships for Work Packages

Where a work package affects an existing relationship, connect the work package to the relationship rather than creating additional direct relationships wherever practical.

Preferred order:

1. Associate to an existing relationship.
2. Associate directly to relevant architectural elements.
3. Use direct associations only when no architectural relationship already exists.

This reduces repository complexity while preserving meaning.

---

# 9. Work Packages Normally Realise Change

Work packages generally deliver:

- New services
- Enhanced services
- New capabilities
- Improved capabilities
- New technology

Therefore realisation should normally be the preferred relationship.

Association should only be used when the nature of the relationship is genuinely unclear.

---

# 10. Business Objects Preferred to Reports, Systems and Documents

Where information is being modelled, the enduring business object should be represented before the mechanism used to store or present it.

Examples:

| Prefer | Instead Of |
|----------|----------|
| Requirement | Requirements Register |
| Asset | Asset Database |
| Contract | Contract Portal |
| Technical Standard | Standards Repository |
| Design Submission | Design Management Tool |

Applications, reports and repositories should relate to business objects rather than replace them.

---

# 11. Technology Capabilities Should Be Created Sparingly

Technology capabilities should represent genuine technology capabilities.

They should not duplicate business capability structures.

Before creating a technology capability, ask:

- Does it represent something computers do?
- Does it exist independently of a business capability?
- Does it add analytical value?

If the answer is no, a capability may not be required.

Mapping directly to a business capability may be more appropriate.

---

# 12. Incomplete Knowledge Should Be Explicit

Where the purpose, scope or meaning of an element is unclear, this should be explicitly identified.

Elements requiring further investigation should include the marker:

```text
[NTKM]
```

(Need To Know More)

This allows reporting and remediation of incomplete repository content.

---

# 13. Optionality Should Be Modelled Explicitly

Where multiple implementation choices exist, optionality should be visible within the model.

Use recognised modelling constructs such as:

- OR junctions
- AND junctions
- Alternative realisation paths

Avoid embedding alternatives in documentation where they cannot be analysed.

---

# 14. Documentation Is Part of the Model

Architectural decisions that are not obvious from the notation should be recorded within the documentation properties of the relevant element or relationship.

Documentation should explain:

- Why a modelling choice was made.
- Why an apparent rule has been broken.
- Why a simplification was accepted.
- What assumptions exist.

Future readers should not need access to the original modeller to understand intent.

---

# 15. Every Element Should Answer a Question

Before creating any model element, ask:

- What question does this help answer?
- What decision does this support?
- What uncertainty does this remove?

If no clear answer exists, the element should probably not be created.

Repository size is not a measure of architectural quality.

Model usefulness is.

---

# Summary

Modelling conventions exist to maximise:

- Consistency
- Simplicity
- Traceability
- Maintainability

When in doubt:

1. Prefer simpler models.
2. Prefer fewer elements.
3. Prefer enduring concepts.
4. Prefer business concepts over technology products.
5. Prefer architectural usefulness over mechanical compliance.
