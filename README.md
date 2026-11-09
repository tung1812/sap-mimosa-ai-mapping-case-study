# SAP–MIMOSA AI Mapping — Capstone Case Study

> **Publication status:** Draft for review. The original team repository is private under university rules. Publish this summary only after confirming that the project description and technical details are approved for public disclosure.

## Overview

**SAP–MIMOSA AI Mapping** was a final-year university team project investigating whether generative AI could help identify corresponding data fields between **SAP Plant Maintenance (PM)** and **MIMOSA CCOM**. The broader aim was to explore ways to reduce manual effort when interpreting and aligning different industrial data models.

The application combined an AI-assisted mapping workflow with a separate validation process. Suggestions produced by an AI model were intended to be **reviewed and assessed**, not treated as automatically correct.

## Team solution at a glance

The project involved:

1. A web interface for viewing and managing mapping records.
2. A backend API for mapping-related operations and AI-assisted suggestions.
3. Structured mapping records containing information about fields on both sides.
4. Validation components for assessing whether suggested field relationships were plausible.

**Technology context:** Python, FastAPI, C# / ASP.NET Core MVC, JSON-based data handling, and OpenAI API integration. These technologies describe the **team's application**, not an assertion that I independently built every component.

## My contribution: mapping validation

I worked on components of the **Python-based validation system** and helped connect the validation functionality to the application's API workflow.

My work included:

- **Data type comparison:** normalizing type labels before checking whether two mapped fields had compatible base types.
- **Field-length comparison:** evaluating how closely field-length attributes matched when that information was available.
- **Mapping data structures:** working with structured representations of the SAP and MIMOSA sides of a mapping.
- **Validation integration:** contributing to how validation components were combined with the FastAPI application.

Other parts of the final validation solution, including additional schema checks, coverage measures, and semantic description comparisons, were developed as part of the **wider team effort**. They should not be attributed solely to me.

## Engineering considerations

### AI output needs independent checks

An AI-generated field mapping may appear plausible without being correct. The project therefore separated **suggestion generation** from **validation** so that output could be evaluated against explicit criteria.

### Different data models need normalization

The two models may use different names or representations for similar concepts. Comparing raw type strings alone can produce misleading results, so a normalization step was useful before scoring.

### Integration is a team challenge

The project was organised through team sprints. One of my biggest learning experiences was coordinating my component with others' work in a largely self-managed development process, including working through unfamiliar requirements and keeping contributions aligned with the shared application.

## What I learned

- Why generative AI outputs require validation and human review.
- How to break an evaluation problem into smaller, understandable checks.
- How structured data and API boundaries help separate system responsibilities.
- How communication and ownership matter when implementing one component of a larger team solution.

## Code availability and attribution

This page is a **personal contribution case study**, not a source-code release or a runnable reproduction of the application.

- The original application was developed collaboratively as university coursework.
- The team's source repository is private and is **not mirrored here**.
- No private source code, project datasets, internal diagrams, or screenshots are included.
- The descriptions above distinguish my contribution from the team's overall implementation.

If public disclosure of further technical details is permitted, this case study may be expanded with an independently created, synthetic demonstration.

