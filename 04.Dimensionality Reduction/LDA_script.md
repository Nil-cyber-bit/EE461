
# <span style="color:rgb(213,80,0)">Linear Discriminant Analysis</span>
<a name="beginToc"></a>

## Table of Contents
&emsp;[Sensor Data](#sensor-data)
 
&emsp;&emsp;[Loading the data](#loading-the-data)
 
&emsp;&emsp;[Strcuturing the Data](#strcuturing-the-data)
 
&emsp;[Computing FDA](#computing-fda)
 
&emsp;&emsp;[Class Identification](#class-identification)
 
&emsp;&emsp;[Overall Mean  of Features](#overall-mean-of-features)
 
&emsp;&emsp;[Scatter Matrices Calculation](#scatter-matrices-calculation)
 
&emsp;&emsp;&emsp;[Eigen Vlaues and Eigen Vector Computation](#eigen-vlaues-and-eigen-vector-computation)
 
&emsp;&emsp;[Sort Eigen Values in Desending Order](#sort-eigen-values-in-desending-order)
 
&emsp;&emsp;[Reduced Feature Set](#reduced-feature-set)
 
&emsp;[Graphical Visulisation of reduced Dimension](#graphical-visulisation-of-reduced-dimension)
 
&emsp;[Feature Set Validation](#feature-set-validation)
 
&emsp;&emsp;[Explained Discriminative Power](#explained-discriminative-power)
 
&emsp;&emsp;[Visual Represenation of Discriminative Power](#visual-represenation-of-discriminative-power)
 
<a name="endToc"></a>

# Sensor Data
## Loading the data
```matlab
load nor_data.mat
```

## Strcuturing the Data
```matlab
nor_data = table2array(nor_data);
% Extract features (X) and labels (y)
X = nor_data(:, 1:16);       % Features: 1000 x 4
y = nor_data(:, 17);         % Labels: 1000 x 1
```

# Computing FDA
## Class Identification
```matlab
classes = unique(y);
nClasses = length(classes);
nFeatures = size(X,2);
```

## Overall Mean  of Features
```matlab
meanOverall = mean(X);
```

## Scatter Matrices Calculation

this section will initialise and then compute for within\-class (S\_W) and between\-class scatter (S\_B) matrices

```matlab
S_W = zeros(nFeatures, nFeatures);
S_B = zeros(nFeatures, nFeatures);

% Loop over each class to accumulate the scatter matrices
for i = 1:nClasses
    % Get the samples for the current class
    classData = X(y == classes(i), :);
    
    % Compute the mean of the current class
    meanClass = mean(classData);
    
    % Compute the within-class scatter matrix:
    % Multiply the covariance of the class by (n_i - 1) to get the scatter matrix.
    S_W = S_W + cov(classData) * (size(classData, 1) - 1);
    
    % Compute the between-class scatter matrix:
    % This captures how far the class mean is from the overall mean.
    diff = (meanClass - meanOverall)';
    S_B = S_B + size(classData, 1) * (diff * diff');
end
```

### Eigen Vlaues and Eigen Vector Computation
```matlab
%   S_B * v = lambda * S_W * v
% This will compute the discriminant directions v.
[V, D] = eig(S_B, S_W);
```

## Sort Eigen Values in Desending Order
```matlab
eigenValues = diag(D)
```

```matlabTextOutput
eigenValues = 16x1
1.0e-25 *

   -0.0000
   -0.0000
   -0.0000
   -0.0000
   -0.0000
   -0.0000
    0.0000
    0.0000
    0.0000
    0.0000

```

```matlab
[~, idx] = sort(eigenValues, 'descend');
V = V(:, idx);
```

## Reduced Feature Set

Determine the number of discriminant directions to keep.

```matlab
% The maximum possible is (nClasses - 1). For example, if you have 3 classes, you get 2.
k = min(nClasses - 1, nFeatures);

% Form the projection matrix using the first 'k' eigenvectors.
projectionMatrix = V(:, 1:k);

% Project the original features onto the new LDA subspace
X_lda = X * projectionMatrix;
```

Saving Features

```matlab
% Define folder name
folderName = 'C:\Users\User\OneDrive\Documents\MATLAB\PEMFC\4.Features\FDAcoeffs';
if ~exist(folderName, 'dir')
    mkdir(folderName);
end
```

```matlab
% Save each variable separately
save(fullfile(folderName, 'FDA_Features.mat'), 'X_lda');
save(fullfile(folderName, 'labels.mat'), 'y');
```

# Graphical Visulisation of reduced Dimension
```matlab
% (Optional) Visualize the projection if reduced to 2 dimensions.
if k == 2
    gscatter(X_lda(:,1), X_lda(:,2), y);
    xlabel('LD1');
    ylabel('LD2');
    title('2D LDA Projection');
end
colormap(jet)
grid on
```



```matlab
% Display the size of the reduced data matrix
disp(['Reduced data dimensions: ', num2str(size(X_lda,2))]);
```

```matlabTextOutput
Reduced data dimensions: 2
```

# Feature Set Validation
## Explained Discriminative Power
```matlab
% Extract and sort eigenvalues (discriminative powers)
eigvals = diag(D);                     % All eigenvalues
[eigvals_sorted, order] = sort(eigvals, 'descend');

% Calculate total discriminative power
total_power = sum(eigvals_sorted);

% Calculate cumulative discriminative power of top axes
top_k = 2;  % Number of FDA axes used (e.g., 2 for 3-class data)
explained_power = sum(eigvals_sorted(1:top_k)) / total_power;

explained_power_components = eigvals_sorted(1:top_k) / total_power;  % This gives a vector

% Display individual explained powers
for i = 1:top_k
    fprintf('FDA Component %d explained power: %.2f%%\n', i, explained_power_components(i) * 100);
end
```

```matlabTextOutput
FDA Component 1 explained power: 99.79%
FDA Component 2 explained power: 0.14%
```

