 # Working process

For this part of the project we used the [ChEMBL bioactivity output](https://www.ebi.ac.uk/chembl/g/#browse/activities/filter/target_chembl_id%3ACHEMBL204) for our protein. We tried 3 Machine Learning approaches to classify our molecules:

* Random Forest (RF)
* Support Vector Machine (SVM) 
* Artificial Neural Network (ANN)

The goal is to test the ability of the model to predict data which it has never seen  before in order to flag problems known as over fitting and to assess the generalization ability of the model. In particular, the model was fited on a random train-test split of the data and the algorothm returned measures such as accuracy, sensitivity, specificity and AUC evaluated on the test set. Lastluy, a function named `crossvalidation` executes a cross validation procedure and prints the statistics of the results over the folds. Typically, an MAE/RMSE below 0.6, approximately, is considered quite decent.

In the last part of the code we tested the adherence of our generated compounds and the ChEMBL compound that was used as a scuffold prototype to the Lipinski Rule of 5.

# Discussion

After seperation of the inactive compounds our training data size was 7812 compounds, while the test data included 1954 compounds. The plot of the ROC curves for our models reveals a good True Positive prediction curve. Based on the Area Under the Curve(AUC) the Random Forest model had the best predictive potential.

<div align="center">
<img width="600" img align="center" alt="image" src="https://github.com/pantmarag/PEP_project/blob/5988792d606854ebd532508fe523af01afad9d16/Machine%20Learning%20Model/roc_auc.png" >
</div>

For that model we computed a MAE of 0.56 	and a std  of 0.01.
Lastly, our compounds (PEP1,2) adhere the Lipinski Rule of 5.

# Disclaimer

Due to lack of time, only the Random forest classifier was used to assess the pIC50 values for the compounds of interest and our own generated ligands. These predictions act as indicators of valid compounds to continue the Docking process with.
