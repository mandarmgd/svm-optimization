# svm-optimization

Data set - [https://archive.ics.uci.edu/dataset/602/dry+bean+dataset](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset)

## Optimizing Nu-Support Vector Machine Classifier and plotting convergence graph. This was done by 
- Taking 10 samples of the data set through random sampling (with replacement) and ensuring that each sample is preprocessed
- Training Nu-SVM classifier along with Randomized Search optimization on parameters like 'kernel', 'nu' and 'gamma'
- Tabulating the results: This contains the best accuracy obtained in case of each sample and the parameter values the accuracy was obtained on
- The results were then stored in a csv file, and the sample used for the model providing the best overall accuracy was chosen to plot the convergence graph

## How was the convergence graph obtained ? 
- Splitting Data : Splitting the dataset into training and test sets
- Setting up iteration simulation : Looping over 1000 steps, each representing a simulated "iteration" of training with increasing amount of training data. This emulates the model learning more as it's exposed to more data.
- Training the Model at Each Iteration: Using the classifiation model providing the best overall accuracy
- Computing accuracy: Evaluating both training accuracy on the subset of data used to train, and test accuracy on the full unseen test set

## Plot interpretation 
- The training accuracy steadily increases as more data is used
- The test accuracy improves initially and then starts to stabilize, indicating convergence
- Since the two plots are converging towards each other, the model has likely learned well and generalized 
