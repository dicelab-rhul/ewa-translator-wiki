# Identification

The **Identification** step determines the **type of experiment** represented in the organised dataset. This classification is essential for deciding which [Parsing](./Parsing) and [Translation](./Multi-Translation) modules should be applied next.

---

## Process

1. **Column name fingerprints**  
   - Subsets of column names in the main `.csv` file are matched against known **fingerprints**.
   - These fingerprints act as signatures for common experiment types (e.g. raw matrix-based, raw guessing-based, already matching one of the supported output formats).

2. **Metadata inspection**  
   - If a `metadata.json` file is available, it is scanned for additional **hints** about the experiment structure or type.

---

## Purpose

The goal of Identification is to establish a clear mapping between the input data and the appropriate downstream modules. This allows the framework to:

- Select the correct [Parsing](./Parsing) procedure.
- Choose suitable [Translation](./Multi-Translation) formats.
- Pass along any relevant **non-data inputs** (such as constants or parameters).

---

## Output

The output of Identification is a set of **identifiers** that specify:

- Which parsing module to call next.
- Which translation modules to invoke afterwards.
- Any additional inputs required that are not embedded in the dataset itself.

---

## See Also

- [Organisation](./Organisation)  
- [Parsing](./Parsing)  
- [Multi-Translation](./Translation)  
- [Core Workflow](./Workflow)  
