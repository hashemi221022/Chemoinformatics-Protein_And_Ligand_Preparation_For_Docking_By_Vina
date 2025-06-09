# What is this project? 
<span><img src="https://img.shields.io/badge/Chemoinformatics-316192?style=flat&logo=bioinformatic&logoColor=white%22" /></span>

# Description of the Notebook Workflow

This notebook provides a step-by-step workflow for preparing protein and ligand structures for molecular docking, specifically targeting the Renin protease and its ligands. The process is designed for users interested in computational drug discovery and molecular modeling using Python-based tools and open-source libraries.

---

## 1. **Library Installation and Imports**
The notebook begins by ensuring all required Python libraries are installed, including OpenMM, RDKit, MDAnalysis, nglview, and others. These libraries are essential for structure manipulation, visualization, and file format conversion.

---

## 2. **Querying the RCSB PDB Database**
The code uses the `rcsbapi` package to search the RCSB Protein Data Bank for Renin structures (EC number 3.4.23.15) that contain ligands with a molecular weight between 300 and 600 Da. It prints out the number of matching structures and ligands, and checks for the presence of specific entries (e.g., "2V0Z" for the protein and "C41" for the ligand).

---

## 3. **Downloading Ligand Files**
For each ligand found in the search, the notebook downloads the corresponding SDF file from the RCSB PDB REST API and saves it to a local directory. This ensures all relevant ligand structures are available for further processing.

---

## 4. **Ligand Preparation with RDKit**
The notebook uses RDKit to load ligand structures, visualize them, and add explicit hydrogens. The modified ligand (with hydrogens) is saved as a new SDF file, which is necessary for accurate docking simulations.

---

## 5. **Protein Structure Preparation**
The code retrieves the PDB file for the selected protein structure and saves it locally. It then uses MDAnalysis to analyze the structure, print statistics (number of atoms, residues, segments), and select specific chains, ligands, and water molecules for further processing.

---

## 6. **Structure Visualization**
Using nglview, the notebook provides interactive 3D visualizations of the protein, ligand, and water molecules. Different representations (cartoon, surface, ball-and-stick, spacefill) are used to highlight various structural features.

---

## 7. **Protein Structure Cleaning**
The notebook isolates the protein atoms in a specific chain (e.g., chain C) and saves the cleaned structure as a new PDB file. This step removes unwanted molecules and focuses the docking on the relevant protein region.

---

## 8. **Fixing Protein Structure with PDBFixer**
To address missing residues, atoms, or hydrogens, the notebook uses PDBFixer to repair the protein structure. The fixed structure is saved as a new PDB file, ready for docking.

---

## 9. **File Format Conversion with Open Babel/ Meeko / Pdb2pqr**
The notebook converts both the fixed protein PDB file and the prepared ligand SDF file to PDBQT format using Open Babel / Meeko / Pdb2pqr. The PDBQT format is required for docking with AutoDock Vina and similar tools. The conversion process includes adding hydrogens and computing atomic charges.

---

## 10. **Summary**
By the end of the notebook, both the protein and ligand are fully prepared in the correct formats for molecular docking simulations. The workflow is modular and can be adapted for other targets or ligands as needed.

---

**Note:**  
- Each code cell is accompanied by comments explaining its purpose and the rationale behind each step.
- The workflow is designed to be reproducible and user-friendly for researchers in computational chemistry and structural biology.

# How to use?

<strong>If you want to get notified about future changes, follow my GitHub account.</strong>

You can clone the project and work on it.

```bash
https://github.com/hashemi221022/Chemoinformatics-Protein_And_Ligand_Preparation_For_Docking_By_Vina.git
```
