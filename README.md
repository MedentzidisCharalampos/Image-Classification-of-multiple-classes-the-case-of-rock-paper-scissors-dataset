# Image-Classification-of-multiple-classes-the-case-of-rock-paper-scissors-dataset
The dataset:

Consists of 3,000 images, all of the images have been generated using CGI with a diverse array of models, male and female and lots of different skin tones.   
The dataset can be found at this URL: http://www.laurencemoroney.com/rock-paper-scissors-dataset/. It will contain a training set and a validation set.

The Preprocessing of the dataset:

The training set:

1. The pixel values are rescaled in the [0, 1]
2. The images are:
  a. rotated by 40
  b. shifted  by 0.2 (the width and height seperately)
  d. sheared by 0.2
  e. zoomed by 0.2
  f. horizontal fliped
3. The dimesions rescaled (reduced) to 150 x 150
4. The batch size is: 126

The validation set:
1. The dimesions rescaled (reduced) to 150 x 150
2. The batch size is: 126

The architecture of the model:
1. A Convolutional Layer with 64 filters, 3 x 3 kernel size, Relu activation function and (150, 150, 3) as input size
2. A Pooling Layer with 2 x 2 window and Max Pool
3. A Convolutional Layer with 64 filters, 3 x 3 kernel size, Relu activation function
4. A Pooling Layer with 2 x 2 window and Max Pool
5. A Convolutional Layer with 128 filters, 3 x 3 kernel size, Relu activation function
6. A Pooling Layer with 2 x 2 window and Max Pool
7. A Convolutional Layer with 128 filters, 3 x 3 kernel size, Relu activation function
8. A Pooling Layer with 2 x 2 window and Max Pool
9. A Flatten Layer tha squash the the output of the previous layer into a 1D dimension
10. A Dropout Layer with 0.5 rate
11. A Dense Layer with 512-units and Relu activation function
12. A Dense Layer with 3-units and Softmax activation function

The model is compiled with categorical crossentropy as lost function and RMSProp as optimizer.
The model is trained for 25 epochs.

The outcome:

1. The accuracy is 98.10 % and the validation accuracy is 95.43 %. 
2. The training is improving and trending towards one.
3. The validation zig-zag a bit, but it is always between 0.9 and 1 after the first few epochs.




