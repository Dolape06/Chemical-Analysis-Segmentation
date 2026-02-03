# Wine Variety Intelligence: Chemical Profiling & Clustering

##  Problem Statement: Quality Control & Market Transparency
In the global wine industry, identifying the exact variety (cultivar) of a wine based purely on its chemical composition is vital for **Quality Assurance** and **Counterfeit Prevention**. 

Market information asymmetry often leaves distributors and consumers unable to verify if a wine's chemical profile truly matches its premium label. Without a transparent tool, mislabeling can lead to significant financial losses and a lack of consumer trust.

## The Solution: A Multi-Model Clustering Approach
This project solves the identification problem by analyzing 13 chemical features (Alcohol, Phenols, Magnesium, etc.) using a two-step Machine Learning workflow:

1. **Dimensionality Reduction (PCA):** Since humans cannot visualize 13 dimensions, I used **Principal Component Analysis** to condense the data into two principal components ($PC1$ and $PC2$) while retaining maximum variance.
2. **Cluster Validation:** * **K-Means Clustering:** Successfully segmented the wines into 3 distinct groups.
    * **Hierarchical Clustering (Dendrogram):** Used as a "Family Tree" visualization to mathematically confirm that 3 is the natural number of wine varieties in the dataset.



## Global Impact
Why does this project matter for the industry?
* **Fraud Detection:** Regulators can use this model to detect if a wine's chemical "fingerprint" matches its declared origin.
* **Automated Classification:** Wineries can automate the sorting of different grape varieties during the production process, reducing human error.
* **Scientific Transparency:** Provides an objective, mathematical standard for wine grading that is not dependent on subjective human tasting.

---

## Results & Technical Interpretation

### Chemical Profiles Identified:
* **Cluster 0 (Light Blue):** Lighter, aromatic wines with high hue and total phenols.
* **Cluster 1 (Dark Blue):** Intense, high-alcohol wines with high Proline and color intensity.
* **Cluster 2 (Light Green):** Balanced table wines with mid-range chemical markers.

### Validation via Dendrogram:
The Dendrogram shows three primary vertical branches before a significant increase in distance (dissimilarity). This validates that our $K=3$ selection for K-Means was the optimal choice for the natural structure of Italian wines.

---

## Technical Stack
* **Language:** Python
* **Libraries:** Pandas, Seaborn, Matplotlib, Scikit-learn (K-Means, PCA), Scipy (Linkage, Dendrogram)
