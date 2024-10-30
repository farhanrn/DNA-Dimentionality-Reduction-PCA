
# DNA Dimentionality Reduction Using Principal Component Analysis (PCA)

## Project Goal
This project aims to analyze gene expression data using Principal Component Analysis (PCA). The gene expression data have 100 genes across 24 samples belonging to four different groups: 
- wt (wild type)
- ko (knock out) 
- mg (mutated)
- ofa (orbit).

## What Code Does
1. Data Generation:
- Creates a dataset of gene expression values. The values are randomly generated using a Poisson distribution but are designed to have different average expression levels between 'wt' and 'ko' groups. The 'mg' and 'ofa' groups also have different distributions but were added later.

2. Data Preparation:
- Transposes the data to have samples as rows and genes as columns.
- Scales the data using preprocessing.scale() to center it around zero and give it unit variance. This is important for PCA.
3. PCA:
- Applies PCA using sklearn.decomposition.PCA to reduce the dimensionality of the data.
- Extracts the principal components and the explained variance ratio.

4. Visualization:
- Creates a scree plot to show the percentage of variance explained by each principal component.
- Creates a PCA plot to visualize the samples in the reduced dimensional space (using PC1 and PC2).

5. Interpretation:
- Identifies the genes that have the biggest influence on the first principal component (PC1).

## Insights and Inferences
Here's what we can gather from the analysis:

- Clustering: The PCA plot shows a clear separation between 'wt' and 'ko' samples along PC1, indicating these groups have distinct gene expression profiles. It supports the initial design where these groups were generated from different populations.

- Variance Explained: PC1 captures a significant portion of the total variance (likely above 90% based on your code), meaning it represents the most important source of variation in the data. PC2 captures a much smaller proportion.

- Gene Influence: By examining the loading scores, you can identify genes that contribute most to PC1 (and therefore, to the separation between groups). High loading scores indicate a strong correlation between a gene's expression and the principal component.

- Biological Interpretation: If this were real biological data, the next step would be to research the functions of the top contributing genes to understand the biological processes that drive the differences between the groups (e.g., 'wt' vs. 'ko').

In summary, this project demonstrates how PCA can be used to:

> Reduce the dimensionality of gene expression data to make it more manageable for analysis, visualization, Identify patterns and clusters in the data that may reflect biological differences. Highlight genes that are important for driving these differences.




