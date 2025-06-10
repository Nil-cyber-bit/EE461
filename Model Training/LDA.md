## Linear Discriminant Analysis reduced dataset

The process of applying LDA is given below:

![image](https://github.com/user-attachments/assets/124f8544-c268-4108-9a62-cd07def451cb)

Based on the figure the normalized data is used in the LDA process where the scatter matrix between and within the class is calculated, from which the eigen values are computed and then inserted into the CV partition for data splitting. 

The LDA reduced dataset was used in the classification learner app in MATLAB and the following are the model evaluation matrix:

### **TRAIN RESULTS**

![image](https://github.com/user-attachments/assets/2ab4bc06-6a5f-4f20-9fde-8558f7e89914)

The figure above shows the evaluation matrix for the LDA reduced dataset, it consist of the true positive, true negative, false positive, and false negative which is used in the calculation for accuracy, precision, recall/sensitivity, and F1-score. 

### **TEST RESULTS**

![image](https://github.com/user-attachments/assets/31c6a12f-3d23-4d1c-8042-ee01bdb318a2)

The highlighted rows shows the best model in terms of F1-score, we are using F1 score as our matrix due to the data imbalance in our dataset. 

Based on this we can select coarse tree model as the best LDA model and below are the results for that model.

**Train Confusion Matrix using the optimizable TREE model** (In python)

![image](https://github.com/user-attachments/assets/9ef5cd65-aae2-46c8-b87c-6d485d218290)

**Test Confusion Matrix using the optimizable TREE model** (In python)

![image](https://github.com/user-attachments/assets/b6d77252-767b-4ede-b4ce-0356eebffb3f)

**ROC Curve for train**

![image](https://github.com/user-attachments/assets/684a8133-b637-408f-a18a-6f2378c470fe)

**ROC Curve for test**

![image](https://github.com/user-attachments/assets/b45dfb23-1ed0-4fd8-af56-f46912e834c6)

**Evaluation matrix for train**

![image](https://github.com/user-attachments/assets/ebe6b5be-c68a-4879-ac2d-2126d86f39c2)


**Evaluation matrix for test**

![image](https://github.com/user-attachments/assets/0e556e6d-67a8-4fb5-8ee9-042f3c20326a)












