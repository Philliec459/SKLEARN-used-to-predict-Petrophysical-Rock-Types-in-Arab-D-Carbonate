# Petrophysical Rock Type (PRT) Estimations for an Arab D complex carbonate reservoir.

This Workbook started with with the work from Brendon Hall, [Enthought](https://www.enthought.com/)(1)

The dataset we will use is log data from eight carbonate wells that have been labeled with Petrophysical Rock Types (PRT) called facies in this instance based on Ed Clerke's Rosetta Stone data(2).  We will use the log data to train a support vector machine to classify these PRT facies types.  Support vector machines (or SVMs) are a type of supervised learning model that can be trained on data to perform classification and regression tasks.  The SVM algorithm uses the training data to fit an optimal hyperplane between the different classes (or facies, in our case).  We will use the SVM implementation in [scikit-learn](http://scikit-learn.org/stable/modules/svm.html).

![Notebook_Image](prt.png)

As mentioned above, we are employing python’s Sklearn as published by Hall(1) to estimate our PRTs. We could have estimated Depositions of Environment or other types of categoric geologic facies used in this Sklearn prediction process.

The initial process is evaluating the data. Seaborn is used to create the matrix cross plots and histograms. Throughout the process we generate numerous Confusion Matrix type plots, and the plot at the bottom right is used to select the optimum C and gamma to tune our models based on the heatmap giving us the highest accuracy for our predictions. 

### Evaluate the data and select optimum model values for C and gamma:

![Notebook_Image](evaluate.png)

In the plot below we show a histgrams of all of the PRTs, and to better understand the quality of our estimations we have left out the AMMY137 well from our training set to be used as a blind test as shown below. the color bar on the left are the PRT facies from this well and the color bar on the right are our predictions.

### The following is a blind test results:
 
![Notebook_Image](blindtest.png)


1.	Hall, Brendon, “Facies classification using Machine Learning”, The Leading Edge, 2016, Volume 35, Issue 10
2.	Clerke, E. A., Mueller III, H. W., Phillips, E. C., Eyvazzadeh, R. Y., Jones, D. H., Ramamoorthy, R., Srivastava, A., (2008) “Application of Thomeer Hyperbolas to decode the pore systems, facies and reservoir properties of the Upper Jurassic Arab D Limestone, Ghawar field, Saudi Arabia: A Rosetta Stone approach”, GeoArabia, Vol. 13, No. 4, p. 113-160, October, 2008. 
