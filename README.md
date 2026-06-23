🧪 Drug-Likeness Pipeline

A chemoinformatics pipeline for drug-likeness screening using RDKit.

This project calculates key physicochemical descriptors and evaluates compounds using widely accepted medicinal chemistry filters, including Lipinski, Veber, and Ghose rules.

---

📖 Overview

This project provides a computational workflow for evaluating the drug-likeness of chemical compounds. Using RDKit, it calculates molecular descriptors and applies established medicinal chemistry rules to identify compounds with favorable drug-like properties.

The pipeline can analyze individual molecules or perform batch screening on large compound libraries, making it useful for early-stage virtual screening and drug discovery workflows.

---

✨ Features

Descriptor Calculation

Calculates key physicochemical descriptors:

- Molecular Weight (MW)
- LogP
- Topological Polar Surface Area (TPSA)
- Hydrogen Bond Acceptors (HBA)
- Hydrogen Bond Donors (HBD)
- Rotatable Bonds
- Ring Count

Drug-Likeness Filters

Implements three commonly used medicinal chemistry filters:

- Lipinski's Rule of Five
- Veber Rules
- Ghose Filter

Processing Modes

- Single-molecule analysis
- Batch screening from CSV files
- Automated descriptor calculation
- Excel export of results

---

🛠 Technologies

- Python
- RDKit
- Pandas
- OpenPyXL
- Jupyter Notebook

---

📂 Project Structure

drug-likeness-pipeline/
│
├── README.md
│
├── notebooks/
│   ├── descriptors.ipynb
│   ├── filters.ipynb
│   ├── pipeline.ipynb
│   ├── batch_screening.ipynb
│   └── test.ipynb
│
├── data/
│   └── molecules.csv
│
├── results/
│   └── results.xlsx

---

🚀 Usage

1. Prepare Input Data

Create a CSV file containing a column named:

smiles

Example:

smiles
CC(=O)OC1=CC=CC=C1C(=O)O
Cn1cnc2n(C)c(=O)n(C)c(=O)c12

Save the file as:

molecules.csv

inside the "data/" directory.

2. Run Batch Screening

Open:

batch_screening.ipynb

and execute all cells.

3. Output

The pipeline generates:

results.xlsx

containing:

- Calculated descriptors
- Lipinski results
- Veber results
- Ghose results
- Overall drug-likeness assessment

---

🚀 Future Development

Planned features:

- Morgan Fingerprints
- Molecular Similarity Search
- Descriptor Visualization
- QSAR Modeling
- ADMET Screening
- Synthetic Accessibility Scoring

---

👨‍🔬 Author

Developed as a chemoinformatics learning and research project using RDKit
