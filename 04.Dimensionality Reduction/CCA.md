## Curvilinear Component Analysis
> Curvilinear component analysis is a statistical method used to analyze data that is organized in a curved or non-linear manner, often applied in fields like psychology and social sciences to identify patterns and relationships among variables. It helps in understanding complex data structures by transforming them into a more manageable form.

### Applying CCA to our Dataset
Since, our dataset is very large approximately 206,421 rows and 16 columns applying CCA to the entire dataset is very difficult. So, for this demostration only the sensor from state one will be used. Meaning, faulty sesnor data from state 1, normal sensor data from state 1, and unknown sensor data from state 1 all combined in one file. 

For this case: the total number of rows was reduced to 8761 rows and 16 columns. Using this section of data CCA was applied and the following are the results that was obtained. The data was stored in the s.mat file
```
load s.mat
data = table2array(state1(:,5:20));
datal = state1(:,21);
x = rmmissing(data);
z = zscore(x);
[coeff,score,latent,tsquared,explained,mu] = pca(z)
```
In the codes above, PCA is applied to the dataset to reduce the total number of the features by finding the variance of 95%.

```
figure(1);
pareto(explained, 0.95)
```
![image](https://github.com/user-attachments/assets/d3e48240-3b94-448d-841f-c1b1a08939b9)

Using the dy-dx plot function file, the plot was constructed as follows. 
```
figure(2);
p = score(:,1:10);
dydxplot(p,squareform(pdist(z)))
```
The result obtained is as follows:

![image](https://github.com/user-attachments/assets/8a866600-a567-4ba0-9602-ea090e238060)

Applying CCA to the reduced dataset. 
```
P = score(:,1:10);
D = z;
k = 4;
epochs = 10;
Mdist = squareform(pdist(z));
alpha0 = 0.5;
lambda0 = 1;
Post = cca(D, P, epochs, Mdist, alpha0, lambda0)
```


