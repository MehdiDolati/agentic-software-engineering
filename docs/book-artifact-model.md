# Book Artifact Model

## Purpose

This document defines the artifact structure used to manage the Agentic Software Engineering book.

The book is managed as a collection of structured artifacts rather than a collection of documents.

---

# Core Principle

Every chapter is a versioned artifact with:

- Identity
- Metadata
- Content
- Review history
- Dependencies

---

# Chapter Artifact Structure

Each chapter follows this structure:

chapter-id/
|
├── chapter.md
├── metadata.yaml
└── review.md

---

# Chapter Components

## chapter.md

Contains the actual chapter content.

Responsibilities:

- Explanations
- Examples
- Diagrams
- Exercises
- References

---

## metadata.yaml

Contains machine-readable information about the chapter.

Example:

```yaml
id: CH-001

title:
  en: Introduction
  fa: مقدمه

part: foundations

order: 1

status: draft

version: 0.1.0

dependencies: []

tags:
  - foundation

toc:
  include: true
  
review.md

Contains review information.

Example:

# Review History

## Version 0.1.0

Date:
2026-07-26

Status:
Initial draft

Notes:
First version created.

Artifact Lifecycle

A chapter moves through these states:

Idea

↓

Draft

↓

Review

↓

Revised

↓

Approved

↓

Published

Versioning

Chapters follow semantic versioning.

Example:

1.0.0

Meaning:

Major:
Structural changes

Minor:
New content

Patch:
Corrections and improvements

Relationships

Chapters may depend on other artifacts.

Example:

Chapter 7
Context Engineering

depends on:

Chapter 4
Specification
Validation Rules

A valid chapter must have:

chapter.md
metadata.yaml
review.md
valid title
valid order
glossary consistency