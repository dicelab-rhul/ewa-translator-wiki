# Visualisation

The **Visualisation** step is delivered through a **web application** that provides a user-friendly interface to run the full workflow and interact with the outputs. It ensures that researchers can manage datasets, configure outputs, and directly inspect results.

---

## Features

1. **Dataset upload**  
   - Users can upload one or more datasets for processing.  

2. **Workflow execution**  
   - Users can start the [Core Workflow](./Workflow) on any number of datasets.  
   - Output formats can be specified before execution.  

3. **Inspection and download**  
   - Once processing is complete, users can browse translated data.  
   - Individual files or whole outputs can be downloaded.  

---

## Implementation

The web application is built with the following stack:  

- **Backend**: Django + Daphne, served with Apache2.
- **Frontend**: Transpiled TypeScript.
- **Certificate management**: Certbot for automated X.509 certificate management.

The web application was built to support by default all modern security standards (e.g., HTTPS, HSTS, CSP, etc.).

See [Technical Details](./Technical-Details) for a full description of the deployment.  

---

## Purpose

Visualisation provides an **accessible, interactive layer** on top of the automated workflow, ensuring that outputs are not only standardised and reproducible but also easy to explore and distribute.  

---

## See Also

- [Export](./Export)  
- [Technical Details](./Technical-Details)  
- [Core Workflow](./Workflow)  
