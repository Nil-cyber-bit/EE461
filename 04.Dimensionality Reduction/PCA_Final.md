Applying PCA for the total dataset table (normal, faulty, and unknown data): 

Plotting the pareto chart for the PCA values. 

![pareto]("C:\Users\HP\Downloads\Picture1.png")



 Figure 1: The pareto chart for the total normalized data.

The above figure is an illustration of the variance of each principal component in the dataset after PCA. The blue bar represents the variance for each principal component and the orange line represents the cumulative variance explained. As observed, the largest variance is around 35%. Moreover, the variance explained decreases as the PC gets higher, where it contributes less to the overall variation in data. This chart is helpful to understand which components are most important in capturing the patterns of the data.





Plotting the Bi-plot for the PCA score values. 



Figure 2: The Bi-plot for the normalized data.

The above figure represents the PCA bi-plot that illustrates the relationship between PCA1 and PCA2. The red points represent the observations in the reduced PCA space and the blue lines reflect the influence of the original variables on the two PCs. Longer vectors indicate that it contributes stronger compared to other variables. This plot is useful to understand the pattern relationships, and the variance contributions in the high-dimensional data after applying PCA.

































Plotting the Scatter plot for the PCA score values. 





 Figure 3: The Scatter plot for normalized data.

The above figure represents the data points in a 2D space defined by PCA1 and PCA2. This plot shows how the data points are distributed along the axes of PCA1 and PCA2. These axes represent the directions of the maximum variance in the dataset. Moreover, the points that are isolated from the main cluster of data can be identified as outliers. This plot is helpful to reduce the complexity of the dataset while retaining the meaningful information.





















Plotting the Scatter3 plot for the PCA score values. 



Figure 4:The Scatter3 plot for normalized data.



 Figure 5: The closer view of the Scatter3 plot for normalized data.

The above Figure 4 and Figure 5 are the scatter3 plot for the normalized data, the first plot is the original view and the second plot is a closer view of the plot. It visualizes the data in 3D. This highlights the distribution across PCA1, PCA2 and PCA3, where the high-dimensional data are reduced to three dimensions. Each color of points is a cluster of the data. This plot is helpful to visualize the insight od the data structure, identify the cluster and outliers and the key patterns for modeling. 



Plotting the Gscatter plot for the PCA score values. 



Figure 6: The Gscatter plot for normalized data.



 Figure 7: The closer view of the Gscatter plot for normalized data.

The above figure 6 and Figure 7 are the Gscatter plots for the normalized data , the first plot is the original view and the second plot is a closer view. The graph represents how the data points are distributed across PCA1 and PCA2. As observed, blue and red points are overlapping can provide insight into the potential correlations and similarities among the data groups. The spread among the PAC space indicates the behavior of the variance in the dataset by the three components. This graph is used to identify the clusters, patterns of the normalized data. 



Plotting the Dy-Dx plot for the PCA score values. 















Appendix 



