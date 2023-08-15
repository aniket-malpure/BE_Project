# BE_Project

Environment: Jupyter Notebook
Python version: 3.11

Procedure to train the model:
1. Installing dependencies and setup
	a. Importing tensorflow, os, numpy, matplotlib, keras
	b. Configuring GPU and CPU
2. Loading the data
	a. Converting images to numerical matrix
	b. Transform the data into 0 to 1 to speed up computation
3. Splitting the dataset into train, valiadtion and test dataset
4. Building the sequential CNN model	
	a. Input image size (256, 256, 3)
	b. Convolutional layer (No. of filters = 32, filter size = 3x3, stride = 1, activation = relu
	c. Max Pooling layer (Size = 2x2)
	d. Convolutional layer (No. of filters = 64, filter size = 3x3, stride = 1, activation = relu
	e. Max Pooling layer (Size = 2x2)
	f. Convolutional layer (No. of filters = 128, filter size = 3x3, stride = 1, activation = relu
	g. Max Pooling layer (Size = 2x2)
	h. Convolutional layer (No. of filters = 256, filter size = 3x3, stride = 1, activation = relu
	i. Max Pooling layer (Size = 2x2)
	j. Convolutional layer (No. of filters = 512, filter size = 3x3, stride = 1, activation = relu
	k. Max Pooling layer (Size = 2x2)
	l. Flatten layer
	m. Dense layer (No. of paramters = 512, activation = relu)
	n. Dropout layer (0.25)
	o. Dense layer (No. of paramters = 256, activation = relu)
	p. Dropout layer (0.25)
	q. Dense layer (No. of paramters = 4, softmax layer)
5. Adam optimizer is used to update training weights
	a. Learning rate = 0.0001
	b. Loss = Sparse categorical entropy
	c. metric = accuracy
6. Training the model with 100 epochs and early stopping with patience 3
7. Plotting loss and accuracy plot
8. Saving the model in a h5 file

Procedure to run the saved model:
1. Load the model (With the h5 file)
2. Resize the input image into 256 by 256
3. Transform the image into 0 to 1
4. Get the predicted class of the image
 
