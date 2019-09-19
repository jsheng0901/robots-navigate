# Learning Algorithm 

Random forests or random decision forests are an ensemble learning method for classification, regression 
and other tasks that operates by constructing a multitude of decision trees at training time and outputting the class 
that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.
Random decision forests correct for decision trees' habit of overfitting to their training set.


Light GBM is a fast, distributed, high-performance gradient boosting framework based on decision tree algorithm, used for ranking, classification and many other machine learning tasks.
Since it is based on decision tree algorithms, it splits the tree leaf wise with the best fit whereas other boosting algorithms split the tree depth wise or level wise rather than leaf-wise. 
So when growing on the same leaf in Light GBM, the leaf-wise algorithm can reduce more loss than the level-wise algorithm and hence results in much better accuracy which can rarely be achieved by any of the existing boosting algorithms. 
Also, it is surprisingly very fast, hence the word ‘Light’.

Fully Connected Neural Network is a basic deep learning model. 
A fully connected neural network consists of a series of fully connected layers. A fully connected layer is a function from ℝ m to ℝ n. 
Each output dimension depends on each input dimension. In here I just try this FC-NN model for fun, thus I just build 5 layer. 


# Model summary

*  Baseline Model

   The baseline model is RandomForest model base on default parameters with only 100 number of estimators. 
   The validation dataset accuracy is around 0.982 which is not bad and the accuracy report you could find in output file. 
   
*  RandomForest Model with adjust parameters

   This model I just increase to 200 number of estimators and use 5 cross-validation results ensembling as final average accuracy.
   The average validation dataset acccuracy is around 0.989 which increas 0.9% accuracy nearly increase 90 correct classification.
   I also do some feature importance plot. The feature importance could find in output file.
   However, this model it takes kind of longer, each fold takes near 7 minutes. 
   
*  Light Gradient Boosting Model
 
   This model I use previous training experience parameters and also use 5 cross-validation results ensembling as final average accuracy.
   The average validation dataset acccuracy is around 0.967 which decrease 2% accuracy.
   I also do some feature importance plot. The feature importance could find in output file.
   Even this model don't have higher accuracy than RandomForest model, LGB takes only 6.5 minutes for each fold. 
   
*  Fully Connect Neural Network Model

   This model is just for fun. Try to use keras build 5 layers neural network. Each layer is relu activaion and last one is softmax.
   The validation dataset acccuracy only near 0.743 and after 50 epochs, it becomes overfitting. 
   
   
# Future Improvements and Plans

*  Fine Tune Parameters --- according to the second RandomForest model, adjusting number of estimators, max features and max leaf node
   maybe will keep increase validation accuracy. However, the running time will also increase.
   
*  Adding some metdata --- according to some others example, adding some metdata like mean, variance, median as features 
   maybe will fix overfiting and also improve accuracy. 

   
