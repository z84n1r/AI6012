java c
AI6012: Machine Learning Methodologies  Applications Assignment (25 points)
Question 1 (10 marks): Consider a multi-class classification problem of C classes. Based on the parametric forms of the conditional probabilities of each class introduced on the 39th Page (“Extension to Multiple Classes”) of the lecture notes of L4, derive the learning procedure of regularized logistic regression for multi-class classification problems.
Hint: define a loss function by borrowing an idea from binary classification, and derive the gradient descent rules to update {w(c)}’s.
Question 2 (5 marks): This is a hands-on exercise to use the SVC API of scikit-learn to train a SVM with the linear kernel and the rbf kernel, respectively, on a binary classification dataset. The details of instructions are described as follows.
1. Download the a9a dataset from the LIBSVM Dataset page.
This is a preprocessed dataset of the Adult dataset in the UCI Irvine Machine Learning Repository, which consists of a training set (available here) and a test set (available here).
Each file (the train set or the test set) is a text format in which each line represents a labeled data instance as follows:
label index1:value1 index2:value2 ...
where “label” denotes the class label of each instance, “indexT” denotes the T-th feature, and valueT denotes the value of the T-th feature of the instance.
This is a sparse format, where only non-zero feature values are stored for each instance. For example, suppose given a data set, where each data instance has 5 dimensions (features). If a data instance whose label is “+1” and the input data instance vector is [2 0 2.5 4.3 0], then it is presented in a line as
+1   1:2   3:2.5   4:4.3
Hint: sciki-learn provides an API (“sklearn.datasets.load svmlight file”) to load such a sparse data format. Detailed information is available here.
2. Regarding the linear kernel, show 3-fold cross-validation results in terms of clas-sification accuracy on the training set with different values of the parameter C in {0.01, 0.05, 0.1, 0.5, 1}, respectively, in the following table. Note that for all the other parameters, you can simply use the default values or specify the specific values you used in your submitted PDF file.代 写AI6012: Machine Learning Methodologies & Applications AssignmentJava
代做程序编程语言
Table 1: The 3-fold cross-validation results of varying values of C in SVC with linear kernel on the a9a training set (in accuracy).
C = 0.01C = 0.05C = 0.1C = 0.5C = 1
?
?
?
?
?

3. Regarding the rbf kernel, show 3-fold cross-validation results in terms of classifi-cation accuracy on the training set with different values of the parameter gamma (i.e., σ2 on the lecture notes) in {0.01, 0.05, 0.1, 0.5, 1} and different values of the parameter C in {0.01, 0.05, 0.1, 0.5, 1}, respectively, in the following table. Note that for all the other parameters, you can simply use the default values or specify the specific values you used in your submitted PDF file.
Table 2: The 3-fold cross-validation results of varying values of gamma and C in SVC with rbf kernel on the a9a training set (in accuracy).
g = 0.01g = 0.05g = 0.1g = 0.5g = 1C = 0.01
?
?
?
?
?C = 0.05
?
?
?
?
?C = 0.1
?
?
?
?
?C = 0.5
?
?
?
?
?C = 1
?
?
?
?
?

Hint: there are no specific APIs that integrates cross-validation into SVMs in sciki-learn. However, you can use some APIs under the category “Model Selec-tion → Model validation” to implement it. Some examples can be found here.
4. Based on the results shown in Tables 1-2, determine the best kernel and the best parameter setting. Use the best kernel with the best parameter setting to train a SVM using the whole training set and make predictions on test set to generate the following table:
Table 3: Test results of SVC on the a9a test set (in accuracy).

Specify which kernel with what parameter setting
Accuracy of SVMs
?

Question 3 (5 marks): The optimization problem of linear soft-margin SVMs can be re-formulated as an instance of empirical structural risk minimization (refer to Page 37 on L5 notes). Show how to reformulate it. Hint: search reference about the hinge loss.
Question 4 (5 marks): Using the kernel trick introduced in L5 to extend the regu-larized linear regression model (L3) to solve nonlinear regression problems. Derive a closed-form. solution (i.e., to derive a kernelized version of the closed-form. solution on Page 50 of L3).



         
加QQ：99515681  WX：codinghelp
