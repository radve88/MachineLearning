# Practical Machine Learning
Assignment Submission Practical Machine Learning
In this analysis we use data from accelerometers on the belt, forearm, arm, and dumbell of 6 participants to predict the manner in which praticipants did the exercise.During collection of data devices such as Jawbone Up, Nike FuelBand, and Fitbit were used.It has now become possible to collect a large amount of data about personal activity relatively inexpensively. These type of devices are part of the quantified self movement A group of enthusiasts who take measurements about themselves regularly to improve their health, to find patterns in their behavior, or because they are tech geeks.people regularly do is quantify how much of a particular activity they do, but they rarely quantify how well they do it. In this data set, the participants were asked to perform barbell lifts correctly and incorrectly in 5 different ways. More information is available from the website here: http://groupware.les.inf.puc-rio.br/har (see the section on the Weight Lifting Exercise Dataset).
The dependent variable or response is the “classe” variable in the training set.
We download the data and clean it. We remove variables that have too many NA values, variables that have low varience or highly co-related variables. We also removed variables which are irrevelant to the dependent variable.Finally data is split into train and test.
The Model Fitting was done by fitting a tree to the data we used the tree package first as this is faster in execution than caret which is slower in execution time. A cross validation was done between test and train data it was found to be a less accurate. Pruning did not have effect with respect to misclassification errors, and gave us a simpler tree. We use less predictors to get almost the same result. By pruning, we got a shallower tree, which is easier to interpret. number of terminal nodes were taken to 18. To get even better fit Random Forest model and obtained a very close fit using 6 predictors randomly from the predictors which were included in the study.

Citations and References
Citation for data used in the study is given below:
Velloso, E.; Bulling, A.; Gellersen, H.; Ugulino, W.; Fuks, H. Qualitative Activity Recognition of Weight Lifting Exercises. Proceedings of 4th International Conference in Cooperation with SIGCHI (Augmented Human ’13) . Stuttgart, Germany: ACM SIGCHI, 2013.
Read more: http://groupware.les.inf.puc-rio.br/har#wle_paper_section#ixzz4M6ImjOce