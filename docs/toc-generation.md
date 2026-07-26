# TOC Generation Design

## Goal

Automatically generate Table of Contents files from chapter metadata.

---

# Input

Chapter metadata files:

chapters/*/metadata.yaml

---

# Output

Generated files:

editions/persian/toc.md

editions/english/toc.md


---

# Generation Rules

Chapters are ordered by:


part
+
order


---

# Example

Metadata:

```yaml
order: 3
title:
  fa: Constitution

Generates:

Chapter 3 — Constitution

Future Automation

Possible implementation:

Python script
GitHub Action
Aegis validator
Validation

The generator should detect:

Missing chapters
Duplicate orders
Broken references
Missing translations
