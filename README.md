# Assignment5 DA5401 (July–Nov 2025)

Author: Venkata Sai Vishwesvar SV
Roll number: BE22B042
Github username : Venkat-Shadeslayer 

## Overview
This repository contains my work for Assignment 5 of the DA5401 course. 

##Executive summary
This project explored how dimensionality reduction techniques influence both visualization and predictive performance on the **Yeast multi-label classification dataset**. The dataset’s inherent complexity—overlapping functional labels and non-linear structures—makes it an ideal testbed for studying data veracity and representation learning.

### **Part A: Data Exploration and Label Simplification**
- The dataset contained **14 overlapping labels**, making visualization difficult.  
- We created a **simplified categorical target** highlighting:
  1. The two most frequent single-label classes.  
  2. The most common multi-label combination.  
  3. Grouped all others as “Other.”  
- This allowed clearer visualization and focused analysis.

### **Part B: Visual Exploration with t-SNE**
- Applied **t-SNE** to uncover the dataset’s hidden manifold structure.  
- Experimented with **different perplexity values** to balance local and global clustering.  
- t-SNE revealed **distinct, non-linear clusters**, highlighting that the data lies on a complex manifold not captured by linear methods like PCA.

### **Part C: Comparative Visualization**
- Compared **PCA**, **Isomap**, and **t-SNE** visualizations.  
- **PCA** showed overlapping classes, while **Isomap** and **t-SNE** uncovered clearer structures—indicating that non-linear methods capture relationships PCA misses.

### **Part D: From Visualization to Prediction**
- Moved from visual interpretation to **quantitative testing** using a **k-NN classifier**.  
- For fair comparison:
  - **PCA:** Number of components chosen via explained variance (~39 components, 80% variance).  
  - **Isomap** and **t-SNE:** Optimal components found empirically.

### **The Final Showdown**
- Compared k-NN accuracy across:
  1. Original 103 features (Baseline)  
  2. PCA (39D)  
  3. Isomap (20D)  
  4. t-SNE (10D)  
- Results:
  - All methods achieved **~20% exact match accuracy**, reflecting dataset difficulty.  
  - **Isomap (20.11%)** slightly outperformed others, followed by **t-SNE (19.97%)**, baseline (**19.83%**), and **PCA (19.56%)**.  

### **Conclusions**
- The Yeast dataset is **intrinsically hard**, with no clear-cut winner among methods.  
- **PCA** proved surprisingly effective despite being linear.  
- **Isomap** and **t-SNE** offered **subtle but real predictive gains**, confirming their ability to capture meaningful non-linear structures.  
- Advanced visualization exposed data complexity, but **truly improving predictive power requires more sophisticated models** beyond dimensionality reduction.

**In essence:**  
This project bridges the gap between visualization and prediction—showing how understanding data geometry can lead to better, though modest, improvements in model performance.

## Structure
- `notebooks/` → Contains the notebooks that I have worked on. The story and the narration are a part of the assignment4.ipynb notebook
- `README.md` → Project documentation and set up
