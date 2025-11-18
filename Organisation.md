# Organisation

The **Organisation** step ensures that all experiment inputs are placed into a **clean, consistent, and lossless structure** before further processing. Since raw inputs are often fragmented, compressed, or cluttered with irrelevant files, this stage standardises everything into a well-defined format.

---

## Process

1. **Extract compressed archives**  
   All bundled files (e.g. `.tar.gz`, `.zip`) are unpacked into a working directory.  

2. **Remove unnecessary files**  
   Extraneous or temporary files are discarded, leaving only materials relevant to the experiment.  

3. **Convert spreadsheets to CSV**  
   All `.xls` and `.xlsx` files are transformed into clean, lossless `.csv` files.  

4. **Preserve supporting material**  
   If present, `.pdf` papers and `.json` metadata files are retained for documentation and reference.  

5. **Create a structured folder layout**  
   - One **parent directory** for all datasets.
   - One **sub-directory per dataset**, containing all associated files.  
   - Each dataset folder contains only `.csv`, `.pdf`, `.json`, and `.txt` files.

---

## Purpose

The goal of Organisation is to provide a **standardised input format** that eliminates inconsistencies. This ensures that subsequent steps, such as [Parsing](./Parsing), can operate smoothly and reliably.

---

## See Also

- [Core Workflow](./Workflow)  
- [Parsing](./Parsing)  
- [Visualisation](./Visualisation)  
