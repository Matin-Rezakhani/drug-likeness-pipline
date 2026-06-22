# 🧪 Drug-Likeness Pipeline

Chemoinformatics drug-likeness screening tool using RDKit. Calculates MW, LogP, TPSA, HBA, HBD, Rotatable Bonds, and Ring Count. Applies Lipinski, Veber, and Ghose rules. Includes a single-entry pipeline and a batch screening module.

---

## 📖 Overview

This project provides a computational pipeline for evaluating the drug-likeness of chemical compounds. Using the powerful RDKit library, it calculates key physicochemical descriptors and filters molecules based on well-established medicinal chemistry rules.

The main goal is to help researchers perform rapid virtual screening of large compound libraries in the early stages of drug discovery.

---

## ✨ Features

- Calculates 7 key descriptors:
  - Molecular Weight (MW)
  - Partition Coefficient (LogP)
  - Topological Polar Surface Area (TPSA)
  - Hydrogen Bond Acceptors (HBA)
  - Hydrogen Bond Donors (HBD)
  - Rotatable Bonds
  - Ring Count

- Applies 3 validated drug-likeness filters:
  - Lipinski's Rule of Five
  - Veber Rules (related to oral bioavailability)
  - Ghose Filter (based on LogP and molecular weight ranges)

- Two processing modes:
  - Single-entry mode: Test and inspect a specific molecule interactively.
  - Batch Screening mode: Import a CSV file with a SMILES column and process hundreds or thousands of molecules simultaneously.

- Structured output: Generates a clean results.xlsx file containing all calculated descriptors and pass/fail statuses for each filter.

---

## 📂 Project Structure

`plaintext
drug-likeness-pipeline/
│
├── README.md
│
├── notebooks/
│   ├── descriptors.ipynb       # Calculates the 7 descriptors for molecules
│   ├── filters.ipynb           # Implements Lipinski, Veber, and Ghose rules
│   ├── pipeline.ipynb          # Combines descriptors + filters for single input
│   ├── batch_screening.ipynb   # Main script for batch processing from CSV
│   └── test.ipynb              # Initial tests and validation
│
├── data/
│   └── molecules.csv           # Sample input file (must contain a SMILES column)
│
├── results/
   └── results.xlsx            # Final output after running batch_screening
