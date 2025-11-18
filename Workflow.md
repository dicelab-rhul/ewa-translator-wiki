# [Core Workflow](./Workflow)

The **EWA Translator** follows a structured and modular workflow designed to convert raw experimental data into clean, standardized, and analyzable formats.  
Each phase of the process focuses on a specific transformation step, from handling messy raw inputs to producing well-organized exports and visual results.

The workflow operates sequentially, but each stage is also independently testable and reusable.  
This modularity makes it easy to adapt the Translator to new experimental designs or output formats as needed.

---

## [Organisation](./Organisation)

The **Organisation** phase ingests one or more raw experiment files (`.xls`, `.xlsx`, `.csv`) or compressed archives (`zip`, `tar.gz`, etc.) and transforms them into **lossless CSVs** stored in a structured directory hierarchy.
All available information is preserved, while a structured hierarchy of directories and files is created to easily parse experiments later on, and to keep track of multiple datasets.
This step lays the groundwork for reliable downstream processing by ensuring that all input files follow a common naming convention and are of the same type.
*Key goals:*

- Standardize input formats into CSV  
- Preserve all original data without loss  
- Create a clear directory structure for multiple datasets

---

## [Identification](./Identification)

In the **Identification** phase, EWA Translator automatically detects the **type of experiment or game** represented in the data, such as matrix-based games, guessing-based games, or others.  
This classification enables the system to choose the appropriate parsing logic and translation rules.

*Key goals:*

- Recognize experiment type and structure
- Handle multiple datasets or treatments within a single input
- Map player roles, treatments, and sessions consistently

---

## [Parsing](./Parsing)

Once the game type is known, the **Parsing** phase converts the organized CSVs into a consistent **in-memory representation**.  
This data model captures the logical entities of the experiment (players, rounds, treatments, payoffs, and decisions) independently of the original file's quirks.

*Key goals:*

- Build a clean internal representation of the experiment(s)
- Detect and correct inconsistencies (e.g., mismatched player IDs, missing values)
- Ensure logical and structural coherence across sessions and treatments

---

## [Multi-Translation](./Multi-Translation)

After parsing, the **Multi-Translation** phase exports the unified representation into all **supported output formats** simultaneously.  
Each translation corresponds to a specific target format optimized for different use cases, such as human readability or automated analysis.

*Key goals:*

- Generate multiple target outputs in parallel
- Ensure all translations are fully consistent with the internal model
- Simplify downstream analyses by providing ready-to-use formats

---

## [Export](./Export)

The **Export** phase produces a main **fully processed game file per experiment**.
It also generates optional companion files such as **constants** and **payoff matrices**, which provide structured metadata for external models or simulations.

*Key goals:*

- Create one canonical output per game (e.g., `matches.csv`)
- Generate supplementary files as needed (e.g., `constants.csv`, `payoff_matrix_0.csv`, etc.)
- Preserve traceability between input files and exported results
- Facilitate automated workflows and reproducible research

---

## [Visualisation](./Visualisation)

Finally, the **Visualisation** phase offers an interactive **web-based interface** for exploring, validating, and running translations.
It allows users to visualize experiment structures, preview translations, and inspect both raw and processed data directly within the browser.

*Key goals:*

- Provide an entry point for users to interact with the system, both passively (i.e., inspecting data) and actively (i.e., running translations)
- Provide an intuitive graphical interface for exploration
- Help detect errors or inconsistencies visually
- Enable on-demand translation and inspection

---

## Summary

In short, EWA Translator transforms messy, unstructured experimental outputs into a clean, standardized ecosystem of data files ready for analysis, visualization, and sharing.  
Each stage builds on the previous one, ensuring **traceability, consistency, and reproducibility** across all transformations.
