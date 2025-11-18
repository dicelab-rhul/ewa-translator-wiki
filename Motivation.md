# Motivation

The **EWA Translator** project was created to address recurring issues in the way data from Economics experiments are stored and exported.  
Many legacy experiment software packages produce results in **unstructured, inconsistent, and difficult-to-use formats**, which makes data cleaning and analysis unnecessarily time-consuming.  

This document summarizes the main motivations behind the creation of EWA Translator.

---

## 1. Obsolete and Inconsistent Data Formats

Most experimental software still in use today relies on output formats that are **arbitrary and poorly documented**.  
These formats tend to:

- Produce output tables with unclear column meanings.  
- Use inconsistent or opaque naming conventions (e.g., the same player might be labeled as `"2"` in one column and `"0"` in another).  
- Contain hard-coded constants in columns instead of using a clear `key: value` structure.  

As a result, **understanding what each column represents requires manual inspection or cross-referencing with experiment notes** (i.e., consulting related papers or codebooks), which is inefficient and error-prone.

---

## 2. Excessive Noise and Redundant Data

Experimental results often contain numerous artefacts that make the data messy and confusing:

- Columns full of irrelevant or constant values that add noise rather than information.  
- Rows duplicated for the same match or observation, creating redundancy.  
- Repeated constants that could be expressed more clearly through structured metadata.  

These issues **bury the important information** in a sea of irrelevant details, slowing down analysis and increasing the likelihood of mistakes.

---

## 3. Poor Identification and Metadata

Another major issue is the **lack of standardized identifiers** and **contextual metadata**:

- Player IDs are often **reused** within a session or treatment, making it difficult to track individuals across experiments.  
- Different players often share the same ID in different treatments or sessions within the same experiment.  
- There is often **no indication** of which experiment, paper, or dataset the data correspond to.  
- Information about the **number of players**, their **subdivision across treatments**, and **session structure** is missing or implicit.  

This lack of clear metadata makes it almost impossible to automate data integration across studies.

---

## 4. Unsuitability for Further Use

Finally, the resulting files are **ill-suited for both humans and machines**:

- They cannot be easily parsed or processed by standard data analysis pipelines.  
- They are cumbersome to inspect manually because of their size, syntax, and clutter.  

In short, the current data outputs are **neither machine-readable nor human-readable**.

---

## 5. The Role of EWA Translator

The **EWA Translator** aims to provide a systematic solution to all these problems by:

- Translating raw experimental outputs into a **clean, structured, and standardized format**.  
- Preserving all relevant information while discarding artifacts and redundancies.  
- Making the data **easily interpretable**, **consistent across experiments**, and **ready for further processing or modeling**.

By doing so, EWA Translator enables researchers to focus on **analysis and interpretation** rather than endless data cleaning.
