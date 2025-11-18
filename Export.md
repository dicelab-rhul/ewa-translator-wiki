# Export

The **Export** step writes the translated data to a **predictable directory structure** on the file system. This provides a stable and transparent way for the [Visualisation](./Visualisation) module to access results, and for researchers to navigate the outputs directly.

---

## Process

1. **Treatment-level directories**  
   - Each treatment is exported to its own sub-directory.  
   - The sub-directory name is constructed from the **first author’s name** and a **unique identifier**.  

2. **Format-specific sub-directories**  
   - Within each treatment directory, a sub-directory is created for every **output format**.  
   - Each is named after the format.  

3. **Game data exports**  
   - For **matrix-based games**, matches are exported to `matches.csv`.  
   - For **guessing-based games**, sessions are exported to `sessions.csv`.  

4. **Payoff matrices**  
   - Each payoff matrix is written to a separate file:  
     - `payoff_matrix_0.csv`  
     - `payoff_matrix_1.csv`  
     - … and so forth.  

5. **Constants**  
   - All constants are exported to `constants.csv`.  
   - This file uses a two-column structure:  
     - `name`  
     - `value`  

---

## Output

The result is a **hierarchical, predictable directory layout**:  

author_id/
├── format_name/
│ ├── matches.csv OR sessions.csv
│ ├── payoff_matrix_0.csv
│ ├── payoff_matrix_1.csv
│ └── constants.csv

---

## Purpose

Export guarantees that all translated outputs are **organised, transparent, and reproducible**, ready for both [Visualisation](./Visualisation) and further analysis or human readability.  

---

## See Also

- [Multi-Translation](./Multi-Translation)  
- [Visualisation](./Visualisation)  
- [Core Workflow](./Workflow)  
