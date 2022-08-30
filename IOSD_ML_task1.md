#Initially in the data preprocessing stage 
following libraries are imported 
1.numpy for working with arrays if required
2.matplotlib ro plot graphs 
3.pandas to import the dataset and to create matrix of features & dependent variable vector

X->matrix of features include columns C to I i.e. column index 2 to 9(or -1)

column G and H are 1 hot encoded which makes them column 0th and 1st in the new matrix of features. Since not more than 2 variables are present in each column ('Earth' and 'False 'is present mostly)they are encoded as a single column 1.0 .Also matrix of features needs to be numpy array so after applying the fit_transform method it's converted back to it. 

since the dependent varaiable exists in binary form(true or false) it's label encoded->0=false 1=true

Data is splitted in Training and test set in 7:3 ratio

Standardisation of data is done in feature scaling. Scalar is fitted only to X_train so that X_test seems like a new dataset on which our ML model will be tested at and transformation to both X_train and X_test.

#Implementing kernel
SVC model is imported to implement svm kernels which are applied on training set
random state is set to 0 to every SVM kernel to fix the seed there

predict medthod is used to find predicted variable vector for ecah type of kernel

precision and f1-scores are found of each model

data plots of actual test results and predicted test results are plotted with each of the independent variables against dependent var.

