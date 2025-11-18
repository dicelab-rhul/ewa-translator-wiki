# Multi-Translation

The **Multi-Translation** step converts each parsed treatment into all compatible output formats, as determined by the [Parsing](./Parsing) metadata. Every translation is guided by a consistent set of rules to ensure that outputs are both accurate and fit for their intended purpose.

---

## Process

1. **Core ID extraction**  
   - Essential columns (e.g. player IDs, treatment IDs, session IDs, round IDs) are identified as **Core IDs**.  
   - Core IDs are used to **deduplicate** data (e.g. removing duplicate rows when matches are represented from multiple player perspectives).
   - Core IDs are extracted by means of equivalence classes, allowing for flexible naming conventions across different datasets (e.g., `Treatment`, `Game`, and `Paper` columns are all treated as `Treatment`)

2. **Game data extraction**  
   - For **matrix-based games**, data are structured as `matches`.  
   - For **guessing-based games**, data are structured as `sessions`.  

3. **Choice and action data**  
   - Player choices and other essential data are extracted and aligned with the Core IDs.
   - Equivalence classes are used in this step as well.

4. **Payoff matrices**  
   - When relevant, all payoff matrices are extracted and stored as a list (`[payoff_matrix]`), one per matrix.  

5. **Constants**  
   - Any constant columns not used in the above structures are collected in a `constants` dictionary (`key: value` pairs).  

6. **Noise removal**  
   - Remaining fields that are not required are treated as **software-generated noise** and discarded.  

---

## Parallel Translations

Each translation into a different output format happens **in parallel**. This ensures efficiency and guarantees that all supported outputs are generated consistently from the same source data.

---

## Output

For each translation, the outputs are:

- A core data structure containing **matches** or **sessions**.
- An optional list of **payoff matrices**, if applicable.
- A dictionary of **constants**.

---

## Purpose

The aim of Multi-Translation is to provide **fit-for-purpose outputs**, each optimised for a particular use case (human readability, automated processing, archival storage, etc.), while preserving consistency across formats.  

---

## See Also

- [Parsing](./Parsing)  
- [Export](./Export)  
- [Core Workflow](./Workflow)  
