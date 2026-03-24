# 🧬 GWAS Pipeline for Diabetic Kidney Disease (DKD)

## 📖 Overview
This project implements a complete **Genome-Wide Association Study (GWAS)** pipeline using a simulated dataset to identify genetic variants associated with **Diabetic Kidney Disease (DKD)**.

The pipeline follows a structured workflow including data simulation, preprocessing, SNP filtering, statistical association testing, multiple testing correction, visualization, and biological interpretation.

---

## 🎯 Objectives
- Simulate a realistic SNP dataset with DKD-associated variants  
- Perform GWAS using logistic regression  
- Apply Minor Allele Frequency (MAF) filtering  
- Correct for multiple hypothesis testing  
- Visualize results using a Manhattan plot  
- Curate and interpret significant SNPs  

---

## 🧪 Dataset Description
- **Samples:** 200 individuals  
  - 100 Healthy  
  - 100 DKD  
- **SNPs:** ~1000 simulated variants  
- **Genotype Encoding:**
  - `0` → Homozygous reference  
  - `1` → Heterozygous  
  - `2` → Homozygous alternate  
- **Alleles:** Randomized (A/T/C/G) per SNP  
- **Signal Design:** Subset of SNPs simulated with different allele frequencies between healthy and DKD groups  

---

## ⚙️ Pipeline Steps

### 1. Data Generation
- Simulated SNP positions (chromosome + genomic location)
- Assigned random allele pairs (A/T/C/G)
- Introduced DKD-associated SNPs via allele frequency differences

---

### 2. Data Preprocessing
- Loaded CSV dataset  
- Separated SNP metadata and genotype matrix  
- Converted data into NumPy arrays  
- Extracted labels from sample names (`healthy` / `dkd`)  
- Encoded labels:
  - `0` → Healthy  
  - `1` → DKD  

---

### 3. Minor Allele Frequency (MAF) Filtering
- Computed MAF for each SNP  
- Removed low-frequency SNPs:
MAF < 0.05
- Retained SNPs with sufficient variation  

---

### 4. GWAS Analysis
- Performed logistic regression for each SNP:

- Extracted p-values for association  

---

### 5. Multiple Testing Correction
- Applied Bonferroni correction:
- Extracted p-values for association  

---

### 5. Multiple Testing Correction
- Applied Bonferroni correction:

- Identified statistically significant SNPs  

---

### 6. Manhattan Plot
- Transformed p-values:
- - Plotted SNPs across genome  
- Highlighted significant SNPs above threshold  

---

### 7. SNP Curation & Interpretation
- Extracted significant SNPs  
- Created structured results table  
- Analyzed genotype-wise disease proportions  
- Identified risk vs protective variants  

---

## 📊 Outputs
- ✅ Significant SNP list  
- ✅ Manhattan plot visualization  
- ✅ Curated SNP table (`.csv`)  
- ✅ Genotype–phenotype interpretation  

---

## 🧠 Key Concepts Used
- Logistic Regression (Machine Learning)  
- Minor Allele Frequency (MAF)  
- Multiple Testing Correction (Bonferroni)  
- Genome-wide association analysis  
- Genotype–phenotype mapping  

---

## 🚀 How to Run

1. Open the notebook in Google Colab or Jupyter  
2. Run cells sequentially:
 - Data generation  
 - Preprocessing  
 - GWAS analysis  
 - Visualization  

---

## 📌 Applications
- Understanding GWAS methodology  
- Disease variant discovery  
- Bioinformatics + ML integration  
- Simulation-based research workflows  

---

## ⚠️ Disclaimer
This project uses **simulated data for educational purposes only**.  
Real GWAS studies require large-scale datasets and specialized tools like **PLINK**.

---

## 👩‍🔬 Author
Dharshini  

---

## 🌟 Future Work
- Add clinical covariates (e.g., BMI, HbA1c)  
- Implement polygenic risk scoring  
- Integrate real genomic datasets  
- Perform functional annotation of SNPs  

---
