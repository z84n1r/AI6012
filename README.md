java cAI6012: Machine Learning Methodologies 
Applications Assignment (25 points)
Important notes: to ffnish this assignment, you are allowed to look up textbooks or
search materials via Google for reference. NO plagiarism from classmates is allowed.
The submission deadline is by 11:59 pm, Sept. 30, 2022. The ffle to be submitted
is a single PDF (no source codes are required to be submitted). Multiple submission
attempts are allowed, and the last one will be graded. A submission link is available
under “Assignments” of the course website in NTULearn.
Question 1 (10 marks): Consider a multi-class classiffcation problem of C classes.
Based on the parametric forms of the conditional probabilities of each class introduced
on the 39th Page (“Extension to Multiple Classes”) of the lecture notes of L4, derive
the learning procedure of regularized logistic regression for multi-class classiffcation
problems.
Hint: deffne a loss function by borrowing an idea from binary classiffcation, and
derive the gradient descent rules to update {w(c)}’s.
Question 2 (5 marks): This is a hands-on exercise to use the SVC API of scikitlearn
1
to
 train a SVM with the linear kernel and the rbf kernel, respectively, on a binary
classiffcation dataset. The details of instructions are described as follows.
1. Download the a9a dataset from the LIBSVM Dataset page.
This is a preprocessed dataset of the Adult dataset in the UCI Irvine Machine
Learning Repository
2
, which consists of a training set (available here) and a test
set (available here).
Each ffle (the train set or the test set) is a text format in which each line represents
a labeled data instance as follows:
label index1:value1 index2:value2 ...
where “label” denotes the class label of each instance, “indexT” denotes the
T-th feature, and valueT denotes the value of the T-th feature of the instance.
1Read Pages 63-64 of the lecture notes of L5 for reference
2The details of the original Adult dataset can be found here.
1This is a sparse format, where only non-zero feature values are stored for each
instance. For example, suppose given a data set, where each data instance has 5
dimensions (features). If a data instance whose label is “+1” and the input data
instance vector is [2 0 2.5 4.3 0], then it is presented in a line as
+1 1:2 3:2.5 4:4.3
Hint: sciki-learn provides an API (“sklearn.datasets.load svmlight ffle”) to load
such a sparse data format. Deta代 写AI6012、Java/c++
代做程序编程语言iled information is available here.
2. Regarding the linear kernel, show 3-fold cross-validation results in terms of classiffcation
 accuracy on the training set with different values of the parameter C in
{0.01, 0.05, 0.1, 0.5, 1}, respectively, in the following table. Note that for all the
other parameters, you can simply use the default values or specify the speciffc
values you used in your submitted PDF ffle.
Table 1: The 3-fold cross-validation results of varying values of C in SVC with linear
kernel on the a9a training set (in accuracy).
C = 0.01 C = 0.05 C = 0.1 C = 0.5 C = 1
? ? ? ? ?
3. Regarding the rbf kernel, show 3-fold cross-validation results in terms of classiffcation
 accuracy on the training set with different values of the parameter gamma
(i.e., σ
2 on the lecture notes) in {0.01, 0.05, 0.1, 0.5, 1} and different values of
the parameter C in {0.01, 0.05, 0.1, 0.5, 1}, respectively, in the following table.
Note that for all the other parameters, you can simply use the default values or
specify the speciffc values you used in your submitted PDF ffle.
Table 2: The 3-fold cross-validation results of varying values of gamma and C in SVC
with rbf kernel on the a9a training set (in accuracy).
Hint: there are no speciffc APIs that integrates cross-validation into SVMs in
sciki-learn. However, you can use some APIs under the category “Model Selection
→ Model validation” to implement it. Some examples can be found here.
4. Based on the results shown in Tables 1-2, determine the best kernel and the best
parameter setting. Use the best kernel with the best parameter setting to train a
SVM using the whole training set and make predictions on test set to generate
the following table:
2Table 3: Test results of SVC on the a9a test set (in accuracy).
Specify which kernel with what parameter setting
Accuracy of SVMs ?
Question 3 (5 marks): The optimization problem of linear soft-margin SVMs can
be re-formulated as an instance of empirical structural risk minimization (refer to Page
37 on L5 notes). Show how to reformulate it. Hint: search reference about the hinge
loss.
Question 4 (5 marks): Using the kernel trick introduced in L5 to extend the regularized
linear regression model (L3) to solve nonlinear regression problems. Derive a
closed-form solution (i.e., to derive a kernelized version of the closed-form solution on
Page 50 of L3).
3

         
加QQ：99515681  WX：codinghelp
