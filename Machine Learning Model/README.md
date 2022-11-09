 # Working process

For this part of the project we used the [ChEMBL bioactivity output](https://www.ebi.ac.uk/chembl/g/#browse/activities/filter/target_chembl_id%3ACHEMBL204) for our protein. We tried 3 Machine Learning approaches to classify our molecules:

* Random Forest (RF)
* Support Vector Machine (SVM) 
* Artificial Neural Network (ANN)

The goal is to test the ability of the model to predict data which it has never seen  before in order to flag problems known as over fitting and to assess the generalization ability of the model. In particular, the model was fited on a random train-test split of the data and the algorothm returned measures such as accuracy, sensitivity, specificity and AUC evaluated on the test set. Lastluy, a function named `crossvalidation` executes a cross validation procedure and prints the statistics of the results over the folds. Typically, an MAE/RMSE below 0.6, approximately, is considered quite decent.

In the last part of the code we tested the adherence of our generated compounds and the ChEMBL compound that was used as a scuffold prototype to the Lipinski Rule of 5.

# Discussion

After seperation of the inactive compounds our training data size was 7812, while the test data included 1954 compounds.
lso plot the ROC curves

<img width="394" alt="image" src="https://user-images.githubusercontent.com/117588718/200306380-7b14d10a-d0aa-4e4f-b599-16398e79c73c.png"> 



# Disclaimer

Due to lack of time, only the Random forest classifier was used to assess the 
