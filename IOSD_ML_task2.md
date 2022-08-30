#Initially in the data preprocessing stage 
following libraries are imported 
1.numpy for working with arrays if required
2.pandas to import the dataset and to create matrix of features & dependent variable vector
3.tensorflow to help build and train the neural network 

X->matrix of features include columns C to I i.e. column index 2 to 9(or -1)

column G is 1 hot encoded which makes it column 0th new matrix of features. Since not more than 2 variables are present in the column ('Earth') it is encoded as a single column 1.0 .Also matrix of features needs to be numpy array so after applying the fit_transform method it's converted back to it. 

since the dependent varaiable and the H column exists in binary form(true or false) it's label encoded->0=false 1=true

Data is splitted in Training and test set in 7:3 ratio

Standardisation of data is done in feature scaling. Scalar is fitted only to X_train so that X_test seems like a new dataset on which our ML model will be tested at and transformation to both X_train and X_test.

#Building and training the neural network
for initailizing ,instance of sequential class of models module from keras is created
2 hidden layers are added with 4 neurons in each with rectifier function as its activation function 
finally for output layer single neuron and sigmoid function for probabilty of output
In compile method 'adam' optimizer is used as a stochastic gradient optimizer but instead of entire batch, batch of 32 rows(also the default value) is chosen. Loss is kept binary_crossentropy since the output result is binary( in case of non-binary o/p categorial_crossentropy and activation='softmax' will be used). Only most essential metrics of 'accuracy' is used. 

100 epochs are performed for training the nn

while predicting the test set results a threshold of 0.5 is chose so every predicted probabilty of >50% will be considered true 