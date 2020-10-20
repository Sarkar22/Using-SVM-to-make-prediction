# Using-SVM-to-make-prediction
In machine learning, support-vector machines are supervised learning models with associated learning algorithms that analyze data used for classification and regression analysis.
The objective of the support vector machine algorithm is to find a hyperplane in an N-dimensional space(N — the number of features) that distinctly classifies the data points.

Here, SVM has been used to predict whether or not a person is going to buy a luxurious car. The dataset that has been used can be found [here](https://github.com/Sarkar22/Using-SVM-to-make-prediction/blob/main/SVMdataset.csv)

The entire project can be divided into various sub-section. They are as follows:

* **Import and explore the dataset and libraries:** numpy, pandas and matplotlib
* **Import the dataset and perform training/testing set splits:** The SVMdataset.csv was imported. But the 'user ID' & 'Gender' column had no impact on the prediction. So they were ignored. The 'Age','EstimatedSalary' has the useful information. The 'Purchased' was column was used as a label for supervised learning model, where '0' means the person didn't buy a luxurious car, and '1' for otherwise.
* **Apply feature scaling for normalization:** This portion has the most vital impact on the overall project.The features come in very different ranges (Age & EstimatedSalary), so they have to be normalize or standardize first. This can be done with sklearn.preprocessing.StandardScaler functions of scikit-learn.
* **Build an SVM classifier and make Predictions:** Finally, let's build the SVM. Here the SVC class from scikit-learn has been used. For now, we are not using kernels, so we should set the kernel argument of SVC to 'linear'. There is no need to specify any other parameters for now. You can find the documentation for SVC here: https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html
* **Fit the SVM classifier to the dataset and making predictions:** To fit the dataset .fit() method & to make prediction .predict() has been used. 
* **Visualize training and testing sets results:**

![training_set](https://github.com/Sarkar22/Using-SVM-to-make-prediction/blob/main/training_set.PNG)
![testing_set](https://github.com/Sarkar22/Using-SVM-to-make-prediction/blob/main/testing_set.PNG)
* **Calculate the accuracy score:** The accuracy score has been found to be 0.88, which can be futher improved by selecting different form of kernels, such as: ploy, rbf.
