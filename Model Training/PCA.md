## PCA Reduced Dataset

A PCA reduced dataset refers to a dataset that has been transformed using Principal Component Analysis (PCA) to reduce its dimensionality while preserving as much of the original data's variance as possible. It identifies the most important patterns in the dataset and redue the number of features (dimensions) while retraining the most critical information. 

Train data is the part of the dataset used to train the machine learning model, it refers to the training portion of a dataset that has been transformed using PCA  to reduce its dimensionality before training a ML model. The below section contains the best three models for the trained PCA:

From all the 33 models, the best performance model was Fine KNN model, it had an accuracy, recall and F1 score of 100. The below plots are the trained and validation plots for the PCA fine KNN model:
![Image](https://github.com/user-attachments/assets/3c5fdde5-a045-4fcb-866c-fd8a08e1597b)

In the above figure is the confusion matrox for the train data, it evaluates the performance of the model. It compares the predicted class labels to the class labels showing where the model is accurate. the diagonal values represent correclty classifed instances the model correctly predicted those clases, the matrix suggests that the model performs very well, within the misclassifciation.

![Image](https://github.com/user-attachments/assets/b867262d-2635-407c-8c90-27b185d5df42)

The above ROC plot is for the train PCA. This is used to evaluate the performance of the binary classification model. The curve plots the true positive rate vs false positive rate across diffeent threshold values. The blue line represents the models performance. In this case, it strats from the origin and moves to 1 and then across to 1 which suggests a perfect classifer with an AUC of 1.0. The diagonal dahsed line represents a random classifer where predictions are purely by chance. 

![Image](https://github.com/user-attachments/assets/276638f6-cebb-4dfe-9365-df8ce1b2b6ae)

The above confusion matrix is provides the insights into the classification model's performance by comparing true class labels with predicted labels. The matrix suggests strong classification accuracy, with minimal misclassifications. 

![Image](https://github.com/user-attachments/assets/9a5ac5c1-0d10-47c9-812d-09c6d1e7ab98)

The above ROC curve evaluates the classification model's ability to distinguish between classes. The blue ROC curve follows an ideal path indicating a perfect classifer. The diagonal dashed line represents a random classifier, meaning predictions are purely by chance. The model operating point shows the specifc threshold at which the model is currently evaluated. 

The second best model for PCA was the weighted KNN model, giving an accuracy of 99.9998, precision of 100,recall was 99.975 and F1 score of 99.9999. The bellow plots and the matrixes are for train and validation for PCA. 

![Image](https://github.com/user-attachments/assets/0aac44b0-2d6d-4be9-acb2-35c32ad98822)

The above matrix is is a tool used to evaluate the performance of a classification model. It shows the actual class labels compared with the predicted class labels. IT helps to distinguish different classes. Ideally, most values should fall along the diagonal, indicating correct classifcation. If off-diagonal values are significant it may suggest misclassification issues. 

![Image](https://github.com/user-attachments/assets/3803e23c-a535-4adf-ac36-3d010b45f36b)

The above ROC  curve, commonly used to asses the performance of binary classification models. It plots the TPR against the FPR , helping to evaluate how well the classifier distinguishes between positive and negative cases. As the ROC curve appears as a signle point which represents a perfect classifier it correctly classifies all instance without errors, the AUC is 1, indicating flawless model performance. 

![Image](https://github.com/user-attachments/assets/9ca111b0-bd98-4081-a1f8-f27fb4f9e788)

The above ROC curve, is used to evaluate the performance of the binary classification model. The plot shows the true positive rate vs the false positive rate. The blue line reprsents the ROC curve, starting from (0,0) and moving sharply to (0,1) then to (1,1) which suggests a perfect classifer with an AUC of 1.

![Image](https://github.com/user-attachments/assets/43115efa-19f4-44d4-8786-711617474184)

The above ROC curve, a fundamental tool for assessing the performance of a binary classification model.It plots the TPR against the FPR to illustrates how well the model distinguishes between classes. The dashed diagonal line represents random gussing ACU 0.5, showinh the baseline performance of a non-discriminating model. 

The next best model was the Ensemble subspace KNN model, it has an accuracy of 99.9973, precision of 100, recall of 99.95 and the F1 score of 99.9986. The bellow plots and the matrixes are for train and validation for PCA. 

![Image](https://github.com/user-attachments/assets/079aec06-f755-4e02-b643-4f46b6375c81)



![Image](https://github.com/user-attachments/assets/a7a37cd5-2eb7-4723-9df4-e269710d2683)

![Image](https://github.com/user-attachments/assets/5db3e12b-bf64-4b92-9f19-da1eceb7a834)
