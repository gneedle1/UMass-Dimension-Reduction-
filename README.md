"""
UMass-Dimension-Reduction-
PCA, t-SNE, and UMAP

Due to the high volume of tissue sample categories, it is quite difficult to use color as a representation for the tissues and see the actual components of each cluster, but the general clusters in respect to each color are still isible. In the future I would label the tissues with a different value than color, and for the timepoint I used the marker size instead of a different shaped marker just because i felt it might be easier to visualize since it is a numeric value.

In our PCA analysis we see three fairly distinct clusters of samples. Due to the distinct nature of the clusters in the PCA i think a kPCA might be a good method to use to preserve the clusters even further. A biplot of the data would also be helpful in visualizing the relationships between the distal enhancers. The overall explained variance based on the x and y axes (PC1 ad PC2) is less than 40% which is not very signifigant (ideally it would be around 95%). This lets us know that the data is not adequately represented by our scatterplot and more principal components should be found if we want to apply the reduced model to a classification or regression problem.

The t-SNE looks quite nice with more segregated clusters than the PCA and just a few mixings of tissue samples that seem to be highly correlated. The t-SNE method tends to show the local patterns of the data, so the compact clusters of multiple tissues implies several possible correlations. Timepoint does not seem to be the basis for any clusters/correlations.

The UMAP method tends to show the global architecture of a higher-dimensional space, so the fact that we had a few less clusters than the t-SNE that were more spread out makes sense. For the metric hyperparameter, I used correlation instead of any of the distance options just to keep the analysis fairly generic, but the euclidian and manhattan metrics seemed to do a good job of forming clusters as well. There can be inferred a kind of superset/subset relationship between the tissue associations in t-SNE clusters and the spacial orientation of the UMAP clusters. Several tissues were consistantly clustered together by sample type in all three methods, which seems promising for finding enhancer patterns/relations.

"""
