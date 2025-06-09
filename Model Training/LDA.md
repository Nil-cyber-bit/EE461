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

**Train/Validation confusion matrix**

![image](https://github.com/user-attachments/assets/3c8f6e96-6c75-4232-9744-6f5ef313195f)








