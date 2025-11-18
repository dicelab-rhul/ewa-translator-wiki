# EWA Translator

**EWA Translator** is a framework for standardising and translating experimental data from Economics experiments. It helps researchers work with legacy data formats that are often incompatible, human-unfriendly, and unsuitable for automated analysis.

---

## [Motivation](./Motivation)

Most Economics experiment software outputs data in **obsolete, inconsistent formats**. EWA Translator addresses this by providing a unified, lossless, and machine-friendly way to **organise, translate, and visualise** such data.

---

## [Core Workflow](./Workflow)

EWA Translator processes one or more experiment files (`.xls`, `.xlsx`, `.csv`) into multiple structured outputs through the following stages:

- [Organisation](./Organisation) → Transform raw inputs into **lossless CSVs**
- [Identification](./Identification) → Detect the **type of game** (matrix-based, guessing-based, etc.)  
- [Parsing](./Parsing) → Convert data into a consistent **in-memory representation**
- [Multi-Translation](./Multi-Translation) → Export to all **supported output formats**
- [Export](./Export) → One game per file + optional **constants and payoff matrices**
- [Visualisation](./Visualisation) → Web interface to run and explore results  

---

## [Guiding Principles](./Principles)

EWA Translator is built on several key principles:

- Modularity: Each stage is independent and can be run separately.  
- Extensibility: New stages, input formats, and output types can be added easily.
- Agility concentration: Most of the user choices are made at the start, with sensible defaults thereafter.
- Output formats are **format-specific**:
  - Some optimised for **human readability**.
  - Others designed for **automated processing** with consistent indexing across files.

This ensures clarity and flexibility across different use cases.  

---

## [Technical Details](./Technical-Details)

All modules are implemented in **Python 3.13**. The Web application uses Django, Daphne, and Apache2 for the backend, and transpiled TypeScript for the frontend. The Certificate management is handled by Certbot.

---

## [Getting Started](./Getting-Started)

Learn how to:

- Install and set up the translator  
- Run the full pipeline on example datasets  
- Explore visual outputs via the web application  

---

## [Future work](./Future-Work)

Planned improvements, supported output formats, and ideas for future integration.  
