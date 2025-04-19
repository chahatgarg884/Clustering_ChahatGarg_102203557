

#  Clustering Analysis on the Iris Dataset

This project explores how different clustering algorithms and preprocessing techniques affect clustering quality on the Iris dataset. The goal is to evaluate *KMeans, **Hierarchical, and **MeanShift* clustering using combinations of transformations, normalization, and PCA.

---

##  Objective

To compare how preprocessing methods influence the performance of clustering algorithms and to determine which combination yields the most meaningful clusters.

---

##  Dataset

- *Iris Dataset*  
  - 150 samples, 4 features  
  - 3 actual species of Iris flowers (used here only for evaluation, not for supervised learning)

---

##  Preprocessing Methods

1. *No Processing*  
2. *Normalization* (MinMaxScaler)  
3. *Transformation* (Square root)  
4. *PCA* (2 components)  
5. *Transform + Normalize*  
6. *Transform + Normalize + PCA*

---

##  Clustering Algorithms

| Algorithm       | Notes                                |
|-----------------|--------------------------------------|
| *KMeans*       | Requires predefined number of clusters |
| *Hierarchical* | Agglomerative method (no training phase) |
| *MeanShift*    | Finds number of clusters automatically |

---

##  Evaluation Metrics

All models were evaluated using:

- *Silhouette Score* — How well points fit within their cluster  
- *Calinski-Harabasz Index* — Ratio of between- to within-cluster dispersion  
- *Davies-Bouldin Score* — Lower is better (less intra-cluster variance)

---

##  Sample Results Snapshot

| Algorithm  | Method     | Clusters | Silhouette | CH Index | DB Score |
|------------|------------|----------|------------|----------|----------|
| KMeans     | T+N+PCA    | 3        | 0.73       | 5601     | 0.58     |
| Hierarchical | Normalize | 4      | 0.67       | 4103     | 0.63     |
| MeanShift  | T+N        | 3        | 0.72       | 4982     | 0.59     |

Full results can be found in the [Jupyter notebook].

---

##  Conclusion

- Preprocessing plays a significant role in cluster separation.
- PCA reduces dimensionality for better visualization.
- MeanShift is flexible but computationally heavier.
- A combination of *Transformation + Normalization + PCA* with *KMeans* often gives consistent results.

