Applying PCA for the total dataset table (normal, faulty, and unknown data): 

01. Plotting the pareto chart for the PCA values.
  
  ![Picture1](https://github.com/user-attachments/assets/7dcbe494-94f6-4e9c-aa2c-9641e8b660eb)

 Figure 1: The pareto chart for the total normalized data.

The above figure is an illustration of the variance of each principal component in the dataset after PCA. The blue bar represents the variance for each principal component and the orange line represents the cumulative variance explained. As observed, the largest variance is around 35%. Moreover, the variance explained decreases as the PC gets higher, where it contributes less to the overall variation in data. This chart is helpful to understand which components are most important in capturing the patterns of the data.


02. Plotting the Bi-plot for the PCA score values. 

![Picture2](https://github.com/user-attachments/assets/3b3dbbb7-2861-4950-9722-6650563c81ba)

Figure 2: The Bi-plot for the normalized data.

The above figure represents the PCA bi-plot that illustrates the relationship between PCA1 and PCA2. The red points represent the observations in the reduced PCA space and the blue lines reflect the influence of the original variables on the two PCs. Longer vectors indicate that it contributes stronger compared to other variables. This plot is useful to understand the pattern relationships, and the variance contributions in the high-dimensional data after applying PCA.


03. Plotting the Scatter plot for the PCA score values. 

![Picture3](https://github.com/user-attachments/assets/785006b3-ca92-4b39-b7f6-15e32763d82f)

Figure 3: The Scatter plot for normalized data.

The above figure represents the data points in a 2D space defined by PCA1 and PCA2. This plot shows how the data points are distributed along the axes of PCA1 and PCA2. These axes represent the directions of the maximum variance in the dataset. Moreover, the points that are isolated from the main cluster of data can be identified as outliers. This plot is helpful to reduce the complexity of the dataset while retaining the meaningful information.


04. Plotting the Scatter3 plot for the PCA score values. 

![Picture4](https://github.com/user-attachments/assets/8f697a12-e739-479e-acc6-00248a8f86a9)

Figure 4:The Scatter3 plot for normalized data.

![Picture5](https://github.com/user-attachments/assets/182c4c42-b50f-4e85-afec-54c0640db3d1)

 Figure 5: The closer view of the Scatter3 plot for normalized data.

The above Figure 4 and Figure 5 are the scatter3 plot for the normalized data, the first plot is the original view and the second plot is a closer view of the plot. It visualizes the data in 3D. This highlights the distribution across PCA1, PCA2 and PCA3, where the high-dimensional data are reduced to three dimensions. Each color of points is a cluster of the data. This plot is helpful to visualize the insight od the data structure, identify the cluster and outliers and the key patterns for modeling. 


05. Plotting the Gscatter plot for the PCA score values. 

![Picture6](https://github.com/user-attachments/assets/f6a8f317-a56a-4b61-be24-e773f320cabe)

Figure 6: The Gscatter plot for normalized data.

![picture9](https://github.com/user-attachments/assets/b3c43d3e-73dd-45a0-8a14-d73af4e509b3)

 Figure 7: The closer view of the Gscatter plot for normalized data.

The above figure 6 and Figure 7 are the Gscatter plots for the normalized data , the first plot is the original view and the second plot is a closer view. The graph represents how the data points are distributed across PCA1 and PCA2. As observed, blue and red points are overlapping can provide insight into the potential correlations and similarities among the data groups. The spread among the PAC space indicates the behavior of the variance in the dataset by the three components. This graph is used to identify the clusters, patterns of the normalized data. 




















