# Parsing

The **Parsing** step transforms raw experiment data into a **custom in-memory representation**, guided by the results of [Identification](./Identification). This ensures that the data are **predictably structured** and ready for subsequent [Translation](./Translation).

---

## Process

1. **Guided by Identification metadata**  
   - The parsing logic uses the identifiers and hints produced during Identification to interpret the data correctly.  

2. **Structured representation**  
   - Raw `.csv` files are converted into a consistent in-memory structure, ensuring predictable layout and indexing.  

3. **Metadata enrichment**  
   - Identification metadata are preserved.  
   - Additional metadata are added where possible (e.g. number of treatments per `.csv` file).  

4. **Per-treatment separation**  
   - Each treatment is stored in its own dedicated structure.  
   - This design allows every treatment to be **translated individually** in the next step.  

---

## Purpose

The aim of Parsing is to provide a **well-structured, extensible representation** of the input data. By combining Identification metadata with new insights, this step creates the foundation for accurate and flexible translation.  

---

## Output

The output is:

- A set of **treatment-specific structures** containing the parsed data.
- An updated metadata set, ready to inform the [Multi-Translation](./Translation) stage.

---

## See Also

- [Identification](./Identification)  
- [Multi-Translation](./Translation)  
- [Organisation](./Organisation)  
- [Core Workflow](./Workflow)  
