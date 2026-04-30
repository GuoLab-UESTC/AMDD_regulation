## Code for *"Whole-Brain Modeling Reveals Subtype-Specific Regulation for Adolescent Major Depressive Disorder"*.

---

### Project Structure 📁


```text
├── datas/              # input datasets
│   ├── dep1/
│   └── dep2/
├── modeling/           # modeling code
│   └── functions/
├── regulation/         # regulation analysis
│   └── dataSave/       # intermediate outputs (provided via GitHub Releases)
├── spm/                # SPM-related scripts
└── subtyping/          # subtype analysis
```

---

### Quick Start 🚀

This section provides a minimal pipeline to reproduce the main results.

**1. Subtyping**

The scripts in the *subtyping* folder can be used to obtain two AMDD subtypes.

⚠️ Notes

Due to data access restrictions, the original data used for subtype classification cannot be publicly shared. This repository provides the complete analysis code along with group-level summary data for the two identified subtypes. The original data requires formal application and approval for access.

**2. Run Whole-Brain Modeling**

To perform large-scale whole-brain modeling for the two identified subtypes, run:

```
modeling/Modeling_dep1.m
modeling/Modeling_dep2.m
```

These scripts will generate the core modeling results for each subtype.

**3. Run Regulation Analysis**

After modeling, run the scripts in the *regulation* folder with the prefix:

```
fic_*.m
```

These scripts implement different regulatory strategies and will produce the corresponding intervention results.



---

### Data Availability & Usage Notes

Some files are excluded via `.gitignore` due to GitHub size limitations. 

They are provided via GitHub Releases:

https://github.com/xinzeng1996/AMDD_regulation/releases

* The excluded files mainly correspond to **intermediate outputs from the `regulation` module**.

---

### BANDA Dataset Restrictions ⚠️

This project is based on the **BANDA dataset**, which requires a formal application for access.

* To comply with data usage regulations, **raw BANDA data is NOT included** in this repository.
* Instead, we provide:

  * Average **Functional Connectivity (FC)** matrices
  * Average **Structural Connectivity (SC)** matrices
    for:

    * Healthy controls
    * Two identified subtypes

---

### Reproducibility Notes

* Due to the absence of raw data, **some scripts may not run end-to-end**.
* If you want to test the pipeline:

  * You can generate **synthetic data with matching dimensions**
  * This allows the code structure to run correctly

⚠️ However, results obtained from synthetic data **will NOT reflect real findings**.

