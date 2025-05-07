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
```
coeff = 16×16    
    0.2794    0.1242   -0.1731   -0.0698    0.0021   -0.0646   -0.0072    0.5943    0.0993   -0.0683   -0.0198    0.0201   -0.0115   -0.0042   -0.0049   -0.7062
    0.2795    0.1242   -0.1729   -0.0691    0.0029   -0.0649   -0.0072    0.5922    0.0895   -0.0752   -0.0341    0.0270   -0.0166   -0.0017   -0.0018    0.7078
    0.2451   -0.0223    0.5095   -0.3493    0.2104   -0.0637   -0.0989   -0.0117    0.0083    0.0057    0.0163   -0.0139   -0.1552    0.6892   -0.0046   -0.0015
    0.2452   -0.0239    0.5087   -0.3485    0.2121   -0.0621   -0.0906   -0.0164   -0.0028   -0.0161   -0.0691    0.0069    0.1523   -0.6881    0.0051    0.0009
    0.2866    0.0602   -0.0633    0.1019   -0.0017   -0.1360    0.0004   -0.0030   -0.4404    0.4488    0.2649   -0.5183    0.3782    0.0563   -0.0295    0.0056
    0.2863    0.0636   -0.0732    0.0956   -0.0078   -0.1389    0.0256   -0.1002   -0.3323    0.4601   -0.0440    0.6852   -0.2689   -0.0510    0.0315   -0.0050
    0.1544   -0.3478    0.4946    0.7227   -0.1819    0.0115    0.0398    0.2146    0.0503   -0.0668    0.0015    0.0148   -0.0113   -0.0019   -0.0010   -0.0001
    0.2817   -0.0115   -0.1143    0.0878    0.1382    0.6176   -0.1115   -0.0875   -0.0954    0.0722   -0.6638   -0.1452    0.0301    0.0460    0.0009   -0.0064
   -0.0791    0.5905    0.1788    0.1314   -0.3621    0.0121   -0.6808   -0.0270    0.0062   -0.0087   -0.0067    0.0033   -0.0085   -0.0065    0.0010    0.0000
    0.2828    0.0072   -0.0909    0.0531    0.1733    0.5774   -0.1206   -0.1045    0.1397   -0.1050    0.6835    0.1383   -0.0324   -0.0464   -0.0001    0.0065

score = 8761×16    
    2.4751    0.5480   -0.0229    0.0164   -0.0599    0.0855    0.1678    0.0031   -0.0045    0.0053   -0.0103   -0.0046   -0.0039    0.0008    0.0001   -0.0013
    2.4759    0.5461   -0.0202    0.0201   -0.0608    0.0858    0.1678    0.0053   -0.0057    0.0092   -0.0088   -0.0062    0.0002    0.0015    0.0036   -0.0012
    2.4759    0.5461   -0.0202    0.0201   -0.0608    0.0858    0.1678    0.0053   -0.0057    0.0092   -0.0088   -0.0062    0.0002    0.0015    0.0036   -0.0012
    2.4705    0.5465   -0.0213    0.0149   -0.0600    0.0885    0.1670    0.0065   -0.0022    0.0110   -0.0102   -0.0014    0.0013    0.0018   -0.0041   -0.0012
    2.4642    0.5504   -0.0329    0.0102   -0.0602    0.0906    0.1675    0.0099    0.0014    0.0078   -0.0117    0.0000   -0.0119    0.0079    0.0005    0.0041
    2.4592    0.5477   -0.0212    0.0189   -0.0712    0.0519    0.1748    0.0160   -0.0013    0.0091    0.0303    0.0004    0.0000    0.0079   -0.0006    0.0045
    2.4578    0.5481   -0.0160    0.0110   -0.0676    0.0520    0.1738    0.0091    0.0017    0.0031    0.0269    0.0045   -0.0035   -0.0014    0.0037   -0.0009
    2.4557    0.5475   -0.0154    0.0100   -0.0681    0.0533    0.1737    0.0093    0.0060    0.0014    0.0247    0.0123    0.0035    0.0004   -0.0044   -0.0009
    2.4632    0.5477   -0.0149    0.0161   -0.0685    0.0493    0.1745    0.0080   -0.0019    0.0013    0.0282   -0.0003   -0.0046   -0.0017    0.0113   -0.0009
    2.4728    0.5450   -0.0192    0.0191   -0.0609    0.0879    0.1672    0.0075   -0.0042    0.0130   -0.0088   -0.0041    0.0032    0.0021   -0.0043   -0.0012

latent = 16×1    
   11.9506
    2.3777
    0.8409
    0.4063
    0.2750
    0.0805
    0.0563
    0.0073
    0.0029
    0.0010

tsquared = 8761×1    
1.0e+03 *

    0.0019
    0.0022
    0.0022
    0.0023
    0.0060
    0.0074
    0.0031
    0.0034
    0.0058
    0.0024

explained = 16×1    
   74.6913
   14.8608
    5.2558
    2.5394
    1.7190
    0.5031
    0.3519
    0.0456
    0.0183
    0.0063

mu = 1×16    
1.0e-13 *

   -0.0301   -0.0283   -0.0055    0.0242   -0.0214    0.0564    0.1245    0.0900    0.0065   -0.0762    0.0438   -0.0182   -0.0576    0.0416    0.0885   -0.0070

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
The results are obtained is follows:
```
iterating: 0 / 10 epochs
iterating: 1 / 10 epochs
iterating: 2 / 10 epochs
iterating: 3 / 10 epochs
iterating: 4 / 10 epochs
iterating: 5 / 10 epochs
iterating: 6 / 10 epochs
iterating: 7 / 10 epochs
iterating: 8 / 10 epochs
iterating: 9 / 10 epochs
iterating: 10 / 10 epochs
10 iterations, error 0.139958          
Post = 8761×10    
    2.4752    0.5504   -0.0234    0.0189   -0.0575    0.0904    0.1657    0.0019    0.0011    0.0086
    2.4785    0.5474   -0.0208    0.0214   -0.0632    0.0899    0.1651    0.0047   -0.0003    0.0109
    2.4785    0.5474   -0.0208    0.0214   -0.0632    0.0899    0.1651    0.0047   -0.0003    0.0109
    2.4723    0.5484   -0.0220    0.0148   -0.0619    0.0929    0.1637    0.0030    0.0051    0.0168
    2.4601    0.5479   -0.0372    0.0146   -0.0585    0.0932    0.1692   -0.0046   -0.0004    0.0133
    2.4528    0.5486   -0.0132    0.0209   -0.0757    0.0419    0.1736    0.0120    0.0079    0.0117
    2.4560    0.5493   -0.0127    0.0055   -0.0712    0.0439    0.1737    0.0086    0.0044    0.0032
    2.4536    0.5547   -0.0124    0.0012   -0.0715    0.0448    0.1684    0.0052    0.0137    0.0090
    2.4622    0.5481   -0.0113    0.0122   -0.0722    0.0408    0.1753    0.0099   -0.0013   -0.0028
    2.4746    0.5468   -0.0186    0.0193   -0.0632    0.0920    0.1636    0.0054    0.0049    0.0183
```
Now plotting the graph based on the class separation.
```
figure (3);
% Extract first 3 principal components
PC1 = Post(:, 1);
PC2 = Post(:, 2);
PC3 = Post(:, 3);

% Get class labels (ensure they align with cleaned data)
classLabels = state1.normal(~any(ismissing(data), 2));
classLabels = categorical(classLabels);% 1. Define colors for each class
classes = unique(classLabels);
colors = lines(length(classes));  % MATLAB's 'lines' colormap (or use 'jet', 'parula')

% 2. Create figure
figure;
hold on;

% 3. Plot each class with its color and label
for i = 1:length(classes)
    idx = (classLabels == classes(i));
    scatter3(PC1(idx), PC2(idx), PC3(idx), 50, colors(i,:), 'filled', ...
        'DisplayName', char(classes(i)));
end

% 4. Add labels and legend
xlabel('Post 1');
ylabel('Post 2');
zlabel('Post 3');
title('3D CCA Scatter Plot (Colored by Class)');
legend('show', 'Location', 'best');  % Show legend with class names
grid on;
view(3);  % Default 3D view
hold off;
```
The following is the graph obtained for code above: 

![image](https://github.com/user-attachments/assets/3e4d1696-d643-4108-ad96-c9aed06c2ce1)

Now that CCA has been performed, we can plot the dy-dx plot of the CCA and compare with the dy-dx plot of the PCA.
```
figure(4);
p1 = Post(:,1:10);
dydxplot(p1,squareform(pdist(z)))
```
The following is the result obtained:

![image](https://github.com/user-attachments/assets/5da59245-3595-49e2-8511-74fe1528f577)


### Conclusion

Due to the large amount of data applying CCA to the entire dataset is very difficult therefore, one section of the dataset was selected for CCA to be performed. The sensor state 1 operation was selected to visualize the impact of CCA on the dataset. 



