# 🧬 AI Drug Discovery & Cheminformatics Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
[![Framework: RDKit](https://img.shields.io/badge/Cheminformatics-RDKit-blue)](https://www.rdkit.org/)

## 📌 Project Overview
This project steps out of traditional financial and text-based data science and enters the high-stakes domain of **Biotechnology and Computational Pharmacology**. 

It demonstrates an end-to-end Cheminformatics pipeline that ingests raw chemical identifiers (SMILES strings), translates them into computational graph objects, engineers pharmacological features based on real-world physics, and deploys Unsupervised Machine Learning to cluster and map the "Chemical Space" of various FDA-approved drugs and neurotransmitters.

## 🛠️ Core Technologies & Competencies Demonstrated
* **Domain-Specific Engineering (RDKit):** Parsing string-based chemical formulations (`SMILES`) into topological molecular objects.
* **Pharmacological Mathematics:** Programmatically calculating physical properties such as Molecular Weight, Lipophilicity (LogP), and Hydrogen Bond interactions.
* **Algorithmic Rule Checking:** Implementing conditional logic to test compounds against **Lipinski’s Rule of Five**, the industry standard heuristic for evaluating oral bioavailability in humans.
* **Dimensionality Reduction (PCA):** Utilizing Principal Component Analysis (`scikit-learn`) to compress 5-dimensional chemical feature data into an interpretable 2D graphical map.
* **Unsupervised ML (K-Means):** Automatically identifying and clustering drugs into distinct "Chemical Families" based on underlying structural similarities without prior labeling.

## 🏗️ Technical Workflow
1. **Ingestion:** A dictionary of SMILES sequences representing molecules like Aspirin, Morphine, and Fluoxetine is loaded and parsed via RDKit.
2. **Feature Extraction:** The system iterates over the molecular graphs to extract specific nodes and edge states (Rotatable Bonds, H-Acceptors) to build a structured Pandas DataFrame.
3. **AI Chemical Space Mapping:** The raw chemical properties are scaled and fed into a PCA model and K-Means algorithm, allowing us to visualize how chemically similar seemingly different drugs are to one another.
4. **Visual Rendering:** Finally, the pipeline uses RDKit's internal drawing engine to physically render high-fidelity 2D structures of the analyzed compounds directly into the output layer.

## 🚀 How to Run the Pipeline
1. Open a blank environment within **Google Colab**.
2. Run the code cell. The `!pip install rdkit` command will automatically provision the underlying C++ chemistry engine inside the Linux environment.
3. Review the outputs:
   * **The Scatter Plot:** Analyzes the AI's clustering of the drugs in reduced chemical space.
   * **The Molecular Grid:** Visually verifies the structural differences between the heaviest and lightest analyzed compounds.
  
<img width="760" height="343" alt="image" src="https://github.com/user-attachments/assets/e7c6be26-02c0-4729-855c-2029143fd167" />
